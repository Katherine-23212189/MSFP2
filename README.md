[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=Katherine-23212189/MSFP2)

# Práctica 2. Modelado y control cardiovascular con el modelo de Windkessel

## Datos académicos

- **Estudiante:** Angelica Ashia Haro Najar
- **Número de control:** 23210708
- **Correo institucional:** l23210708@tectijuana.edu.mx
- **Carrera:** Ingeniería Biomédica
- **Asignatura:** Modelado de Sistemas Fisiológicos
- **Docente:** Dr. Paul Antonio Valle Trujillo
- **Institución:** Tecnológico Nacional de México, Instituto Tecnológico de Tijuana

## Introducción

El modelado matemático permite estudiar el comportamiento de los sistemas fisiológicos a través de representaciones que facilitan su análisis y simulación. En el área cardiovascular, el modelo de Windkessel constituye una herramienta para representar la relación entre la presión arterial y el flujo sanguíneo mediante elementos que describen las propiedades resistivas, elásticas e inerciales del sistema circulatorio.

En esta práctica se utiliza el modelo de Windkessel de cuatro elementos para analizar tres condiciones cardiovasculares: normotensión, hipotensión e hipertensión. A partir de sus parámetros se obtienen las funciones de transferencia correspondientes y se estudia la respuesta dinámica de cada sistema.

También se emplean herramientas de simulación y programación para evaluar el comportamiento en lazo abierto y lazo cerrado, así como el desempeño de controladores PID orientados a reducir las diferencias entre las respuestas de los sistemas hipotenso e hipertenso y la respuesta normotensa de referencia.

## Objetivos de la práctica

1. Obtener las funciones de transferencia de los modelos cardiovascular normotenso, hipotenso e hipertenso.
2. Formular las ecuaciones integro-diferenciales que describen la dinámica del sistema.
3. Determinar el error en estado estacionario y evaluar la estabilidad en lazo abierto.
4. Implementar el modelo en Simulink/Simscape y simular su respuesta ante una señal aleatoria uniforme con mínimo de -0.2 V, máximo de 1 V, semilla de 106 y tiempo de muestreo de 0.5 s.
5. Ajustar las ganancias de controladores PID para aproximar las respuestas hipotensa e hipertensa al comportamiento normotenso de referencia.
6. Comparar las respuestas en lazo abierto y en lazo cerrado mediante simulaciones en Python, utilizando Visual Studio Code como entorno de desarrollo.

## Fundamento del modelo fisiológico

El modelo de Windkessel de cuatro elementos representa determinadas propiedades del sistema vascular mediante una analogía con un circuito eléctrico. Sus parámetros son:

| Parámetro | Significado fisiológico |
|---|---|
| `Z` | Impedancia característica del sistema vascular |
| `C` | Distensibilidad arterial |
| `R` | Resistencia vascular periférica |
| `L` | Inertancia arterial |

La combinación de estos elementos permite describir la dinámica de la presión y el flujo sanguíneo. En la representación de espacio de estados se consideran dos variables principales: el flujo a través de la inertancia arterial y la presión asociada a la distensibilidad arterial.

A partir del modelo matemático se analiza el comportamiento de las siguientes condiciones:

- **Normotenso:** se utiliza como referencia para evaluar las demás respuestas.
- **Hipotenso:** representa el comportamiento del modelo bajo los parámetros asociados a una condición de presión arterial reducida.
- **Hipertenso:** representa el comportamiento del modelo bajo los parámetros asociados a una condición de presión arterial elevada.

Las funciones de transferencia obtenidas permiten estudiar la relación entre la entrada y la salida de cada modelo, así como comparar sus respuestas dinámicas. Posteriormente, se incorporan controladores PID para evaluar la reducción del error respecto al sistema normotenso.

## Metodología computacional

El desarrollo de la práctica se divide en tres etapas:

1. **Análisis matemático:** formulación del modelo, obtención de las funciones de transferencia y evaluación de la estabilidad y el error en estado estacionario.
2. **Simulación del sistema:** implementación del modelo cardiovascular en MATLAB y Simulink/Simscape para observar su respuesta ante la señal de entrada establecida.
3. **Diseño y evaluación del control:** implementación en Python de las funciones de transferencia y de los controladores PID, con comparación de las respuestas en lazo abierto y en lazo cerrado mediante Visual Studio Code.

Esta metodología permite relacionar el modelo matemático con los resultados de simulación y analizar el efecto del control sobre las condiciones hipotensas e hipertensas.

## Contenido del repositorio

Los archivos del repositorio reúnen el desarrollo matemático, las simulaciones y la implementación computacional de la práctica:

- **MATLAB (`.mlx`):** desarrollo y documentación de los cálculos realizados.
- **Simulink (`.slx`):** modelo utilizado para simular el comportamiento cardiovascular.
- **Python (`.py`):** scripts para el análisis de las funciones de transferencia y la simulación de los controladores PID en Visual Studio Code.
- **Parámetros de control:** valores de las ganancias PID utilizadas en las simulaciones.
- **Resultados gráficos:** representaciones de las respuestas de los modelos y comparación entre lazo abierto y lazo cerrado.
- **Análisis matemático:** documentación de las ecuaciones integro-diferenciales, las funciones de transferencia, el error en estado estacionario y la estabilidad.
- **Modelo fisiológico ilustrativo:** representación gráfica del sistema cardiovascular, si se incluye como parte de la entrega.

**Palabras clave:** 
Sistema cardiovascular; modelo de Windkessel; presión arterial; función de transferencia; control PID.

## Referencias

[1] P. A. Valle, *Syllabus para Modelado de Sistemas Fisiológicos*. Tecnológico Nacional de México, Instituto Tecnológico de Tijuana, 2025. Disponible en: https://biomath.xyz/course/

[2] M. C. Khoo, *Physiological Control Systems: Analysis, Simulation, and Estimation*, 2.ª ed. IEEE Press, 2018, sección 4, p. 93.

[3] N. S. Nise, *Control Systems Engineering*, 8.ª ed. John Wiley & Sons, 2020.

[4] T. Kind, T. J. Faes, J. W. Lankhaar, A. Vonk-Noordegraaf y M. Verhaegen, "Estimation of three-and four-element Windkessel parameters using subspace model identification", *IEEE Transactions on Biomedical Engineering*, vol. 57, núm. 7, pp. 1531-1538, julio de 2010. https://doi.org/10.1109/TBME.2010.2041351
