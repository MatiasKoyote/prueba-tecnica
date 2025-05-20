# Prueba Técnica: Desarrollador RPA UiPath - Debugging y Solución de Problemas

¡Bienvenido/a a la prueba técnica para Desarrollador RPA UiPath!

## Objetivo de la Prueba
El objetivo de esta prueba es evaluar tu capacidad para:
* Identificar y diagnosticar errores en flujos de trabajo existentes de UiPath.
* Analizar la causa raíz de los problemas.
* Proponer e implementar soluciones robustas y eficientes.
* Aplicar buenas prácticas de desarrollo RPA, incluyendo el manejo de errores y logging.
* Estimar tiempos de diagnóstico y resolución en un contexto realista.

## Escenario del Proceso
El proyecto de UiPath (`ProyectoUiPathConError`) tiene como objetivo automatizar el siguiente proceso:
1.  Leer una lista de empleados desde un archivo Excel (`Empleados.xlsx`). Cada empleado tiene un nombre y un departamento asociado.
2.  Para cada empleado, buscar el "Código de Proyecto" que corresponde a su departamento. Esta información se encuentra en un archivo Excel de referencia (`Departamentos_CodigosProyecto.xlsx`).
3.  Registrar el nombre del empleado y el "Código de Proyecto" encontrado en un nuevo archivo Excel de resultados (`Resultados.xlsx`).

## Configuración Inicial y Archivos del Repositorio

**Prerrequisitos:**
* UiPath Studio instalado (versión 2021.10 o posterior recomendada para compatibilidad con el proyecto base, aunque debería funcionar en versiones más recientes).
* Microsoft Excel o una aplicación compatible para visualizar los archivos `.xlsx`.

**Archivos Incluidos en este Repositorio:**
* **`ProyectoUiPathConError/`** (Carpeta del proyecto UiPath)
    * `Main.xaml`: El flujo de trabajo principal que contiene el error.
    * `project.json`: El archivo de configuración del proyecto UiPath.
    * (Otras carpetas y archivos generados por UiPath como `.local/`, `.objects/` pueden estar presentes o serán generados por Studio).
* **`Empleados.xlsx`**: Archivo de entrada con la lista de empleados y sus departamentos.
* **`Departamentos_CodigosProyecto.xlsx`**: Archivo de referencia que mapea departamentos a códigos de proyecto.

**Instrucciones de Configuración:**
1.  Clona o descarga este repositorio a tu máquina local.
2.  Asegúrate de que los archivos `Empleados.xlsx` y `Departamentos_CodigosProyecto.xlsx` estén ubicados **dentro** de la carpeta `ProyectoUiPathConError/` (es decir, al mismo nivel que el archivo `Main.xaml` y `project.json`). El proyecto está configurado para buscarlos con rutas relativas.
3.  Abre UiPath Studio.
4.  Desde Studio, abre el proyecto navegando a la carpeta `ProyectoUiPathConError/` y seleccionando el archivo `project.json` (o `Main.xaml`).

## El Problema
El proceso, en su estado actual, contiene uno o más errores que impiden su correcta finalización o producen resultados incorrectos para todos los registros de empleados. Tu misión es encontrar y solucionar estos problemas.

## Tu Tarea: Instrucciones Detalladas
Por favor, realiza los siguientes pasos:

1.  **Ejecutar y Analizar:**
    * Ejecuta el flujo de trabajo `Main.xaml` tal como está para observar su comportamiento y los errores que se presenten.
    * Utiliza las herramientas de debugging de UiPath Studio para entender el flujo de ejecución y el estado de las variables.

2.  **Identificar el Problema:**
    * ¿Cuál es el error exacto que se produce (mensaje de error, tipo de excepción)?
    * ¿En qué actividad específica del flujo de trabajo ocurre el error?

3.  **Análisis de Causa Raíz:**
    * Explica detalladamente cuál es la causa raíz del/los error(es). No te limites a describir el síntoma; profundiza en el porqué fundamental del fallo.
    * ¿Qué datos de entrada o condiciones específicas están provocando el problema?

4.  **Propuesta de Solución:**
    * Describe los cambios específicos que realizarías en el flujo de trabajo de UiPath para corregir el error y asegurar que el proceso maneje correctamente todos los casos (incluyendo datos faltantes, departamentos no encontrados, etc.).
    * Considera las buenas prácticas de desarrollo RPA:
        * Uso adecuado de bloques `Try-Catch`.
        * Validaciones de datos.
        * Mensajes de log claros y útiles.
        * Manejo de selectores (si aplicara, aunque en este caso es más de lógica y datos).
    * Puedes describir los cambios textualmente, usar pseudocódigo, o diagramas si ayudan a clarificar tu propuesta.

5.  **(Opcional pero Recomendado) Implementación de la Solución:**
    * Modifica directamente el proyecto `ProyectoUiPathConError` en tu UiPath Studio para implementar la solución que has propuesto.
    * Asegúrate de que el proceso se ejecute sin errores para todos los datos de prueba y genere el archivo `Resultados.xlsx` correctamente.

6.  **Medidas Preventivas y Mejora Continua:**
    * ¿Cómo se podría haber evitado este tipo de error durante la fase de desarrollo inicial?
    * ¿Qué estrategias de logging o monitoreo implementarías para detectar y diagnosticar problemas similares más rápidamente en un entorno de producción?

7.  **Estimación de Tiempo (Simulación Real):**
    * **Tiempo de Diagnóstico:** En un escenario real, ¿cuánto tiempo estimas que te tomaría identificar la causa raíz de este problema específico si te lo encontraras por primera vez en un proyecto desconocido?
    * **Tiempo de Implementación de la Solución:** ¿Cuánto tiempo estimas que te tomaría implementar y probar la solución que has propuesto (incluyendo la implementación opcional del punto 5)?

## Entregables
Prepara y envía lo siguiente:

1.  **Un documento** (preferiblemente en formato Markdown, Word o PDF) que contenga tus respuestas detalladas a los puntos 2, 3, 4, 6 y 7 de la sección "Tu Tarea".
2.  **Si realizaste la implementación opcional (punto 5):** Un archivo `.zip` que contenga la carpeta completa del proyecto UiPath `ProyectoUiPathConError` con tu solución implementada. Asegúrate de que el archivo `Resultados.xlsx` generado por tu solución NO esté incluido en el zip, ya que el proceso debe generarlo.

## Tiempo Sugerido
Te sugerimos dedicar entre **1.5 y 2 horas** para completar esta prueba.

## Consideraciones Adicionales
* Céntrate en la claridad de tus explicaciones y la robustez de tu solución.
* Si necesitas hacer alguna suposición razonable debido a información no explícitamente detallada, por favor, documéntala en tus respuestas.
* El objetivo no es solo que el robot "funcione", sino también demostrar tu comprensión de los principios de un desarrollo RPA de calidad.

---

¡Mucha suerte! Esperamos ver tu solución.