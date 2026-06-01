# 🧮 Paquete Final - Métodos Numéricos en Python

> **Importante:** El ejecutable puede tardar varios segundos en arrancar.

Este repositorio contiene la implementación final de algoritmos de análisis numérico desarrollados como proyecto académico. El programa integra soluciones robustas para la resolución de sistemas de ecuaciones no lineales, interpolación, ajuste de curvas e integración numérica.

## 🚀 Instrucciones de Ejecución (¡Importante!)

Para cumplir con las especificaciones de evaluación, este programa ha sido compilado como un **archivo ejecutable independiente (`.exe`)**. 

**No es necesario instalar Python, compiladores, ni librerías adicionales.**

1. Ve a la sección de archivos de este repositorio.
2. Da click en **`paquete_final.exe`**, si no se descarga automaticamente, da click en **`view raw`**.
3. Haz doble clic sobre el archivo en cualquier computadora con sistema operativo Windows.
4. El menú interactivo se abrirá automáticamente en la consola del sistema.

> **Nota:** Si Windows Defender muestra un aviso de seguridad de "Windows protegió su PC" (común en ejecutables compilados localmente), haz clic en **"Más información"** y luego en **"Ejecutar de todas formas"**.

---

# Casos de prueba

A continuación se muestran algunos conjuntos de datos de prueba recomendados para verificar el funcionamiento de los distintos métodos implementados en el programa. Estos valores tienen fines demostrativos y permiten validar que los algoritmos produzcan resultados correctos.

## Opción 1: Sistemas de ecuaciones no lineales (Método de Broyden)

### Sintaxis de las funciones

Las ecuaciones deben escribirse utilizando la siguiente notación:

* `x[0]` → primera variable.
* `x[1]` → segunda variable.
* `**` → operador de potencia en Python.

Ejemplo para el sistema de prueba:

```python
x[0]**2 + x[1]**2 - 4
x[0]*x[1] - 1
```

Este sistema corresponde a la intersección entre una circunferencia y una hipérbola.

### Valores de prueba

```text
Número de ecuaciones: 2

f1(x) = x[0]**2 + x[1]**2 - 4
f2(x) = x[0]*x[1] - 1

x[0] = 1.5
x[1] = 0.5

Dígitos de precisión: 5
```

---

## Opción 2: Interpolación y ajuste de curvas

### 2.1 y 2.2 Interpolación de Newton

Para este método los datos deben ser equidistantes. Se recomienda utilizar puntos pertenecientes a la función:

```text
y = x²
```

con paso `h = 1`.

#### Datos de prueba

```text
Número de puntos: 5

x[0] = 1   y[0] = 1
x[1] = 2   y[1] = 4
x[2] = 3   y[2] = 9
x[3] = 4   y[3] = 16
x[4] = 5   y[4] = 25

¿Son correctos los datos? (s/n): s
```

#### Interpolación

```text
Punto a interpolar: 2.5
Grado: 2
```

---

### 2.3 Ajuste por Spline Cúbico

Para los splines cúbicos no es necesario que los puntos sean equidistantes.

#### Datos de prueba

```text
¿Leer desde archivo CSV? (s/n): n

Número de puntos: 4

x[0] = 0     y[0] = 0
x[1] = 1.5   y[1] = 2.5
x[2] = 2     y[2] = 1
x[3] = 3.2   y[3] = 4

¿Son correctos los datos? (s/n): s
```

Al confirmar los datos, el programa calculará la matriz del sistema, los coeficientes del spline y mostrará la gráfica correspondiente.

---

## Opción 3: Integración numérica (Trapecio y Romberg)

El programa incluye funciones predefinidas para realizar pruebas rápidas.

### Datos de prueba

```text
Selecciona la opción 1 (Elegir la función)
Elige (1 o 2): 1

Selecciona la opción 2 (Leer intervalo)

Límite inferior (a): 0
Límite superior (b): 2

Dígitos de precisión: 6
```

Posteriormente, selecciona la opción **Calcular integral**. El programa generará automáticamente la tabla de extrapolación de Romberg y mostrará el resultado final de la integración.


## 🛠️ Estructura y Módulos del Programa

El sistema se opera a través de un menú interactivo en consola que da acceso a las siguientes herramientas matemáticas:

### 1. Sistemas de Ecuaciones No Lineales
* **Método de Broyden:** Solución de sistemas de *n* ecuaciones con *n* variables. Implementa la aproximación Cuasi-Newton actualizando la matriz inversa Jacobiana mediante el teorema de Sherman-Morrison para optimizar el costo computacional.

### 2. Interpolación y Ajuste de Curvas
* **Interpolación de Newton:** Construcción automática de tablas de diferencias divididas. El algoritmo selecciona de manera inteligente si aplicar el método progresivo o regresivo dependiendo del punto a evaluar.
* **Splines Cúbicos Naturales:** Ajuste de curvas mediante polinomios de grado 3 por tramos. Imprime el sistema matricial, los coeficientes $a_i, b_i, c_i, d_i$, las funciones algebraicas por segmento y despliega una gráfica completa con la curva resultante.

### 3. Integración Numérica
* **Extrapolación de Romberg:** Cálculo de integrales definidas para funciones continuas en intervalos dados. Se combina la Regla del Trapecio con la extrapolación de Richardson, generando la matriz triangular completa y evaluando el error con una tolerancia definida por el usuario.

---

## 💻 Entorno de Desarrollo (Para fines de revisión)

Si se desea auditar el código fuente original (`.py`), las dependencias utilizadas para su desarrollo fueron:
* `numpy` (Manejo matricial y álgebra lineal)
* `pandas` (Estructuración de datos tabulares)
* `matplotlib` (Renderizado de gráficos)
* `sympy` (Álgebra simbólica para impresión de polinomios)
* `tabulate` (Estética y legibilidad de tablas en consola)

---

## 👨‍💻 Desarrollador

* **Torres Miranda Diego de Jesus** * Número de Cuenta: 425040364
* UNAM FES Acatlán
