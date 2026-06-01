# 🧮 Paquete Final - Métodos Numéricos en Python

Este repositorio contiene la implementación final de algoritmos de análisis numérico desarrollados como proyecto académico. El programa integra soluciones robustas para la resolución de sistemas de ecuaciones no lineales, interpolación, ajuste de curvas e integración numérica.

## 🚀 Instrucciones de Ejecución (¡Importante!)

Para cumplir con las especificaciones de evaluación, este programa ha sido compilado como un **archivo ejecutable independiente (`.exe`)**. 

**No es necesario instalar Python, compiladores, ni librerías adicionales.**

1. Ve a la sección de archivos de este repositorio.
2. Descarga el archivo **`paquete_final.exe`**.
3. Haz doble clic sobre el archivo en cualquier computadora con sistema operativo Windows.
4. El menú interactivo se abrirá automáticamente en la consola del sistema.

> **Nota:** Si Windows Defender muestra un aviso de seguridad de "Windows protegió su PC" (común en ejecutables compilados localmente), haz clic en **"Más información"** y luego en **"Ejecutar de todas formas"**.

---

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
