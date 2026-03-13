# 🌱 AgroExpert - Aplicación Móvil Inteligente para Identificación y Cuidado de Plantas

![Java](https://img.shields.io/badge/Java-17-orange?style=for-the-badge&logo=java) 
![Android](https://img.shields.io/badge/Android-SDK-3DDC84?style=for-the-badge&logo=android) 
![Firebase](https://img.shields.io/badge/Firebase-Firestore-FFCA28?style=for-the-badge&logo=firebase) 
![API](https://img.shields.io/badge/API-Plant.id-blue?style=for-the-badge) 
![Status](https://img.shields.io/badge/Status-Desarrollo-brightgreen?style=for-the-badge)

> **Proyecto de Desarrollo de Software presentado en SOLACYT - INFO MATRIX IBEROAMÉRICA 2026** ---

## 📑 Tabla de Contenidos

1. [Acerca del Proyecto](#-acerca-del-proyecto)
2. [Características Principales](#-características-principales)
3. [Tecnologías y Herramientas](#️-tecnologías-y-herramientas)
4. [Arquitectura del Sistema](#-arquitectura-del-sistema)
5. [Integración con API Plant.id](#-integración-con-api-plantid)
6. [Resultados e Impacto](#-resultados-e-impacto)
7. [Instalación Local](#-instalación-local)
8. [Redes Sociales](#-redes-sociales)
9. [Autores y Reconocimientos](#-autores)

---

## 📖 Acerca del Proyecto

**AgroExpert** es una aplicación móvil basada en Inteligencia Artificial diseñada para asistir a jardineros aficionados, agricultores urbanos y estudiantes en la identificación precisa de especies vegetales y su mantenimiento.

La falta de conocimientos especializados suele derivar en diagnósticos erróneos, riego incorrecto y, finalmente, la pérdida de las plantas. AgroExpert resuelve esta problemática permitiendo identificar plantas a través de la cámara del dispositivo móvil, ofreciendo además recomendaciones personalizadas, recordatorios y un historial de seguimiento.

---

## ✨ Características Principales

* 📸 **Identificación Inteligente:** Reconocimiento botánico impulsado por IA con un alto grado de confianza.
* 🌿 **Registro y Gestión:** Catálogo personal de plantas con monitoreo de su estado general.
* ⏰ **Recordatorios Automáticos:** Alertas programadas para tareas críticas como el riego y la fertilización.
* 📊 **Historial y Reportes:** Trazabilidad de cada planta registrada a lo largo del tiempo.
* ☁️ **Sincronización en la Nube:** Todos los datos y fotografías se respaldan en tiempo real de forma segura.

---

## 🛠️ Tecnologías y Herramientas

### Lenguajes y Frameworks
* **Java 17** * **Android SDK** (Compatible con Android 8.0+) 
* **Material Design** para la UI/UX 

### Servicios Cloud (Firebase)
* **Firebase Authentication:** Gestión y autenticación de usuarios.
* **Firebase Firestore:** Base de datos NoSQL para información de plantas e historiales.
* **Firebase Storage:** Almacenamiento optimizado de las imágenes capturadas.

### Integraciones y Librerías
* **API Plant.id:** Motor externo de *Machine Learning* para la visión por computadora.
* **Retrofit:** Cliente HTTP seguro.
* **GSON:** Procesamiento de JSON.
* **WorkManager:** Gestión de tareas en segundo plano para notificaciones.

---

## 🏗️ Arquitectura del Sistema

El proyecto sigue un modelo robusto de **Arquitectura de 3 Capas** para asegurar escalabilidad y facilidad de mantenimiento:

1. **Capa de Presentación:** Construida con el SDK de Android y Material Design, facilitando la interacción amigable con el usuario.
2. **Capa de Dominio:** Centraliza la lógica de negocio, el control del algoritmo de identificación y la generación de recomendaciones.
3. **Capa de Datos:** Gestiona toda la interacción remota utilizando el ecosistema de Firebase (Auth, Firestore y Storage).

### 🔄 Flujo de Identificación y Cuidados
Para ofrecer un diagnóstico y tratamiento preciso, la aplicación sigue este ciclo de funcionamiento:
1. **Captura de Imagen:** El usuario toma una fotografía de la planta, hoja o fruto desde la interfaz de la cámara nativa de la app.
2. **Análisis Externo:** La imagen es procesada y enviada de forma segura a la API de **Plant.id**, la cual identifica la taxonomía exacta de la planta.
3. **Generación de Cuidados:** Una vez que la API devuelve la especie identificada, la Capa de Dominio de AgroExpert cruza esta información con nuestra base de datos en Firestore para extraer las recomendaciones de cuidado específicas (frecuencia de riego, necesidades de luz solar, tipo de sustrato y temperatura ideal).
4. **Programación de Alertas:** Con base en estos cuidados, el sistema utiliza `WorkManager` para crear un calendario de tareas locales, enviando notificaciones push al usuario para recordarle cuándo debe regar o fertilizar cada planta en particular.

---

## 🤖 Integración con API Plant.id

El núcleo de reconocimiento visual no se ejecuta localmente en el dispositivo para ahorrar recursos, sino que opera comunicándose de forma fluida con una API especializada bajo el siguiente algoritmo de procesamiento:

1. El usuario captura la imagen a través de la interfaz nativa. 
2. Se realiza una compresión de la imagen y conversión a formato `JPEG`. 
3. Se codifica la imagen a formato `Base64` para facilitar su transmisión. 
4. Envío asíncrono (vía Retrofit) al endpoint de análisis de la **API Plant.id**. 
5. La API procesa la imagen usando sus propias redes neuronales y visión por computadora. 
6. Retorno de un objeto JSON con el nombre de la especie, taxonomía y el porcentaje (%) de probabilidad/confianza. 
7. Despliegue en pantalla de los resultados y opción para guardar la planta en el catálogo del perfil del usuario. 

---

## 📈 Resultados e Impacto

AgroExpert fue sometido a un riguroso protocolo de pruebas experimentales en las que participaron 44 estudiantes de la carrera de Ingeniería en Biotecnología. Se analizaron 30 especies realizando 300 intentos de identificación:

* 🎯 **Aumento de Precisión:** La aplicación alcanzó un **89% de precisión**, comparado con apenas un 54% logrado mediante el método tradicional manual (+35 puntos porcentuales).
* ⚡ **Eficiencia:** El tiempo promedio de respuesta y reconocimiento fue de tan solo **3.5 segundos**.
* 💡 **Aceptación Educativa:** La inmensa mayoría de usuarios indicaron que la app es una herramienta muy útil que favorece activamente su aprendizaje.

---

📱 Redes Sociales
¡Sigue el crecimiento del proyecto y conéctate con la comunidad de tecnología agrícola!

Facebook: @agroexpert

Instagram: @agroexpert

TikTok: @agroexpert

X (Twitter): @agroexpert

👨‍💻 Autores
Giovanni Rojas Damian - Desarrollo e Investigación

Orlando Flores Rodríguez - Desarrollo e Investigación

Asesora: Yesenia Pérez Reyes

Institución: Universidad Politécnica de Puebla

Este proyecto fue registrado bajo el número de ID 37695 para su presentación formal.

## 📥 Descarga
Puedes descargar el APK de la última versión desde aquí:
[👉 Descargar última versión (APK)](https://github.com/orlandu04/AgroExpert/releases/tag/Descarga)

## 🚀 Instalación Local

### Requisitos previos
* Dispositivo móvil o emulador con **Android 8.0** o superior.
* Conexión a Internet.
* Android Studio instalado.

### Clonar el Repositorio e Iniciar

```bash
git clone [https://github.com/orlandu04/AgroExpert.git]


