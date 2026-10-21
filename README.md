[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=Katherine-23212189/MSFP2)

# Práctica 2: Modelo y control del sistema cardiovascular mediante el modelo Windkessel

## Información de la estudiante

Katherine Coria Camacho [23212189]; l23212189@tijuana.tecnm.mx

Modelado de Sistemas Fisiológicos

Ingeniería Biomédica

## Docente

Dr. Paul Antonio Valle Trujillo; paul.valle@tectijuana.edu.mx

Departamento de Ingeniería Eléctrica y Electrónica, Tecnológico Nacional de México/IT Tijuana, Blvd. Alberto Limón Padilla s/n, Tijuana, C.P. 22454, B.C., México.

## Descripción de la asignatura

El modelizado de sistemas fisiológicos es una herramienta importante en Ingeniería Biomédica, permite comprender el funcionamiento del cuerpo humano, así como diseñar y evaluar terapias y dispositivos médicos; se define como el proceso de formular modelos matemáticos o computacionales que representan el comportamiento y la interacción de los sistemas biológicos y fisiológicos. Esta asignatura pretende aportar al perfil del Ingeniero Biomédico la capacidad de realizar investigación científica en el área de Biología de Sistemas con la finalidad de dirigir y participar en equipos de trabajo interdisciplinarios en contextos nacionales e internacionales, así como de proporcionar soluciones informáticas para resolver problemas en el campo de la Ingeniería Biomédica con ética profesional; lo anterior al proporcionar al estudiante bases sólidas para modelizar sistemas y diseñar controladores para la solución de problemas en las áreas de atención médica y del sector industrial médico. La construcción de analogías entre circuitos eléctricos y sistemas fisiológicos para la formulación de modelos matemáticos y el diseño de controladores mediante la experimentación in silico brindan herramientas de gran aplicación en el quehacer profesional del Ingeniero Biomédico.

La asignatura de Modelado de Sistemas Fisiológicos forma parte del plan de estudios de la carrera en Ingeniería Biomédica con la siguiente competencia general del curso: Utiliza las propiedades de los circuitos RLC para describir la dinámica de sistemas fisiológicos, obtener modelos matemáticos y aplicar el control clásico, esto con el objetivo de integrar los principios de la Ingeniería de Control, la Electrónica Analógica y las Ciencias de la Computación con la Anatomía y Fisiología del cuerpo humano para proporcionar descripciones cuantitativas y cualitativas de sistemas fisiológicos complejos con el objetivo de modelizar, analizar, controlar, ilustrar y predecir su dinámica tanto en el corto como en el largo plazo.

## Objetivos

1. Obtener las funciones de transferencia correspondientes a los sistemas cardiovasculares normotenso, hipotenso e hipertenso.
2. Formular el modelo matemático mediante las ecuaciones integro-diferenciales que describen la dinámica del sistema.
3. Analizar la estabilidad de los modelos cardiovasculares en lazo abierto.
4. Calcular el error en estado estacionario de los sistemas estudiados.
5. Simular el comportamiento del modelo cardiovascular en Simulink/Simscape mediante una señal aleatoria uniforme con mínimo de -0.2 V, máximo de 1 V, semilla de 106 y tiempo de muestreo de 0.5 s.
6. Sintonizar las ganancias de controladores PID para reducir el error entre las respuestas de los sistemas hipotenso e hipertenso y la respuesta normotensa de referencia.
7. Analizar y comparar las respuestas en lazo abierto y en lazo cerrado mediante las simulaciones del modelo cardiovascular.
8. Implementar en Python, utilizando Visual Studio Code, las funciones de transferencia y los controladores PID para estudiar la respuesta de los sistemas en lazo abierto y en lazo cerrado.

## Descripción detallada del sistema

En esta práctica se estudia el modelo de Windkessel de cuatro elementos, utilizado para representar características dinámicas del sistema cardiovascular mediante una analogía con circuitos eléctricos. El modelo considera la impedancia característica (Z), la distensibilidad arterial (C), la resistencia vascular periférica (R) y la inertancia arterial (L).

A partir de estos parámetros se obtienen las funciones de transferencia de los sistemas normotenso, hipotenso e hipertenso, lo que permite analizar y comparar sus respuestas dinámicas. También se estudian las ecuaciones que describen el comportamiento del modelo, su estabilidad en lazo abierto y el error en estado estacionario.

Finalmente, se diseñan controladores PID para reducir las diferencias entre las respuestas de los sistemas hipotenso e hipertenso y la respuesta normotensa de referencia. Las simulaciones en MATLAB, Simulink y Python permiten observar el comportamiento de los modelos y evaluar el efecto de la realimentación sobre la respuesta del sistema cardiovascular.

Palabras clave: Sistema cardiovascular; Modelo de Windkessel; Presión arterial; Función de transferencia; Controlador PID.

## Lista de archivos incluidos en el repositorio

1. Cuaderno computacional de MATLAB [.mlx y .pdf].
2. Modelo de Simulink [.slx].
3. Scripts de Python desarrollados en Visual Studio Code [.py].
4. Archivo de datos en Excel usado para Visual Studio Code [.xlsx].
5. Archivo o imagen con los parámetros y las ganancias de los controladores PID.
6. Imágenes y documentos de las simulaciones [.pdf y .png].
7. Análisis matemático: funciones de transferencia de los sistemas normotenso, hipotenso e hipertenso, ecuaciones integro-diferenciales, estabilidad y error en estado estacionario.

## Referencias

[1] P. A. Valle, Syllabus para Modelado de Sistemas Fisiológicos, Tecnológico Nacional de México / Instituto Tecnológico de Tijuana, Tijuana, B.C., México, 2025. Permalink: https://biomath.xyz/course/

[2] M. C. Khoo, Physiological Control Systems: Analysis, Simulation, and Estimation, 2nd ed. Piscataway, New Jersey, USA: IEEE Press, 2018, Section 4, Page 93.

[3] N. S. Nise, Control Systems Engineering, 8th ed. Hoboken, New Jersey, USA: John Wiley & Sons, 2020.

[4] T. Kind, T. J. Faes, J. W. Lankhaar, A. Vonk-Noordegraaf & M. Verhaegen, "Estimation of three-and four-element Windkessel parameters using subspace model identification", IEEE Transactions on Biomedical Engineering, vol. 57, issue 7, pp. 1531-1538, July 2010. https://doi.org/10.1109/TBME.2010.2041351
