# Classification Model for Therapeutic Arm Exercises 🦾

![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-success)

Este repositorio contiene el código fuente y la documentación para un modelo de aprendizaje automático diseñado para **clasificar ejercicios terapéuticos de brazo**. El objetivo principal es asistir en procesos de tele-rehabilitación, permitiendo monitorear si el paciente está realizando el movimiento correcto.


---

## 📖 Descripción del Proyecto

La rehabilitación física a menudo requiere la repetición de movimientos específicos. Este proyecto utiliza técnicas de **Visión por Computadora** y **Machine Learning** para identificar y clasificar estos movimientos en tiempo real (o a partir de videos pregrabados).

El sistema es capaz de:
* Detectar puntos clave (keypoints) del cuerpo humano.
* Extraer características biomecánicas del brazo.
* Clasificar el tipo de ejercicio realizado.
* [Opcional: Contar repeticiones o evaluar la calidad del movimiento].

## 🏋️ Ejercicios Soportados

El modelo ha sido entrenado para clasificar las siguientes clases de movimientos:

1. **Flexión de Codo** (Bicep Curl)
2. **Abducción de Hombro** (Levantamiento lateral)
3. **Flexión de Hombro** (Levantamiento frontal)


## 🧠 Arquitectura y Metodología

El flujo de trabajo (pipeline) del proyecto es el siguiente:

1. **Entrada:** Video o stream de webcam.
2. **Pose Estimation:** Uso de [MediaPipe / OpenPose] para extraer las coordenadas (X, Y, Z) de las articulaciones del brazo y hombro.
3. **Preprocesamiento:** Normalización de coordenadas y cálculo de ángulos entre articulaciones.
4. **Clasificación:** Los datos procesados alimentan un modelo [LSTM / Random Forest / SVM ] que predice la etiqueta del ejercicio.

## ⚙️ Instalación

Sigue estos pasos para configurar el entorno de desarrollo:

### Prerrequisitos
* Python 3.8 o superior
* Webcam (para pruebas en tiempo real)

### Pasos
1. Clona el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/arm-exercise-classification.git](https://github.com/tu-usuario/arm-exercise-classification.git)
   cd arm-exercise-classification
