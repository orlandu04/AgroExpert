# 🌱 AgroExpert - Aplicación Móvil Inteligente para Identificación y Cuidado de Plantas

[cite_start]![Java](https://img.shields.io/badge/Java-17-orange?style=for-the-badge&logo=java) [cite: 341]
[cite_start]![Android](https://img.shields.io/badge/Android-SDK-3DDC84?style=for-the-badge&logo=android) [cite: 341]
[cite_start]![Firebase](https://img.shields.io/badge/Firebase-Firestore-FFCA28?style=for-the-badge&logo=firebase) [cite: 341]
[cite_start]![API](https://img.shields.io/badge/API-Plant.id-blue?style=for-the-badge) [cite: 342]
![Status](https://img.shields.io/badge/Status-Completado-brightgreen?style=for-the-badge)

> [cite_start]**Proyecto de Desarrollo de Software presentado en SOLACYT - INFO MATRIX IBEROAMÉRICA 2026** [cite: 1, 101, 112]

---

## 📑 Tabla de Contenidos

1. [Acerca del Proyecto](#-acerca-del-proyecto)
2. [Características Principales](#-características-principales)
3. [Tecnologías y Herramientas](#️-tecnologías-y-herramientas)
4. [Arquitectura del Sistema](#-arquitectura-del-sistema)
5. [Motor de Inteligencia Artificial](#-motor-de-inteligencia-artificial)
6. [Resultados e Impacto](#-resultados-e-impacto)
7. [Instalación Local](#-instalación-local)
8. [Generación de Reportes (LaTeX)](#-generación-de-reportes-latex)
9. [Redes Sociales](#-redes-sociales)
10. [Autores y Reconocimientos](#-autores)

---

## 📖 Acerca del Proyecto

[cite_start]**AgroExpert** es una aplicación móvil basada en Inteligencia Artificial diseñada para asistir a jardineros aficionados, agricultores urbanos y estudiantes en la identificación precisa de especies vegetales y su mantenimiento[cite: 122, 123].

[cite_start]La falta de conocimientos especializados suele derivar en diagnósticos erróneos, riego incorrecto y, finalmente, la pérdida de las plantas[cite: 162, 163, 164]. [cite_start]AgroExpert resuelve esta problemática permitiendo identificar plantas a través de la cámara del dispositivo móvil, ofreciendo además recomendaciones personalizadas, recordatorios y un historial de seguimiento[cite: 123, 124].

---

## ✨ Características Principales

* [cite_start]📸 **Identificación Inteligente:** Reconocimiento botánico impulsado por IA con un alto grado de confianza[cite: 82, 84].
* [cite_start]🌿 **Registro y Gestión:** Catálogo personal de plantas con monitoreo de su estado general[cite: 84].
* [cite_start]⏰ **Recordatorios Automáticos:** Alertas programadas para tareas críticas como el riego y la fertilización[cite: 84].
* [cite_start]📊 **Historial y Reportes:** Trazabilidad de cada planta registrada a lo largo del tiempo[cite: 84].
* [cite_start]☁️ **Sincronización en la Nube:** Todos los datos y fotografías se respaldan en tiempo real de forma segura[cite: 340].

---

## 🛠️ Tecnologías y Herramientas

### Lenguajes y Frameworks
* [cite_start]**Java 17** [cite: 341]
* [cite_start]**Android SDK** (Compatible con Android 8.0+) [cite: 341, 85]
* [cite_start]**Material Design** para la UI/UX [cite: 341]

### Servicios Cloud (Firebase)
* [cite_start]**Firebase Authentication:** Gestión y autenticación de usuarios[cite: 341].
* [cite_start]**Firebase Firestore:** Base de datos NoSQL para información de plantas e historiales[cite: 341].
* [cite_start]**Firebase Storage:** Almacenamiento optimizado de las imágenes capturadas[cite: 341].

### Integraciones y Librerías
* [cite_start]**API Plant.id:** Motor externo de *Machine Learning* para la visión por computadora[cite: 342].
* [cite_start]**Retrofit:** Cliente HTTP seguro[cite: 342].
* [cite_start]**GSON:** Procesamiento de JSON[cite: 342].
* [cite_start]**WorkManager:** Gestión de tareas en segundo plano para notificaciones[cite: 342].

---

## 🏗️ Arquitectura del Sistema

[cite_start]El proyecto sigue un modelo robusto de **Arquitectura de 3 Capas** para asegurar escalabilidad y facilidad de mantenimiento[cite: 338]:

1. [cite_start]**Capa de Presentación:** Construida con el SDK de Android y Material Design, facilitando la interacción amigable con el usuario[cite: 339].
2. [cite_start]**Capa de Dominio:** Centraliza la lógica de negocio, el control del algoritmo de identificación y la generación de recomendaciones[cite: 339].
3. [cite_start]**Capa de Datos:** Gestiona toda la interacción remota utilizando el ecosistema de Firebase (Auth, Firestore y Storage)[cite: 340].

---

## 🤖 Motor de Inteligencia Artificial

[cite_start]El proceso de reconocimiento visual opera de forma fluida bajo el siguiente algoritmo de procesamiento[cite: 342, 343, 344, 345, 346]:

1. [cite_start]El usuario captura la imagen a través de la interfaz nativa. [cite: 342]
2. [cite_start]Se realiza compresión y conversión a formato `JPEG`. [cite: 343]
3. [cite_start]Codificación de la imagen a `Base64`. [cite: 343]
4. [cite_start]Envío asíncrono (vía Retrofit) al endpoint de la **API Plant.id**. [cite: 344]
5. [cite_start]Análisis de patrones morfológicos por redes neuronales. [cite: 344]
6. [cite_start]Retorno de JSON con nombre de especie, taxonomía y el % de confianza. [cite: 345]
7. [cite_start]Despliegue en pantalla y opción para guardar en el perfil del usuario. [cite: 346]

---

## 📈 Resultados e Impacto

[cite_start]AgroExpert fue sometido a un riguroso protocolo de pruebas experimentales en las que participaron 44 estudiantes de la carrera de Ingeniería en Biotecnología[cite: 278]. [cite_start]Se analizaron 30 especies realizando 300 intentos de identificación[cite: 279]:

* [cite_start]🎯 **Aumento de Precisión:** La aplicación alcanzó un **89% de precisión**, comparado con apenas un 54% logrado mediante el método tradicional manual (+35 puntos porcentuales)[cite: 281, 282, 283].
* [cite_start]⚡ **Eficiencia:** El tiempo promedio de respuesta y reconocimiento fue de tan solo **3.5 segundos**[cite: 284].
* [cite_start]💡 **Aceptación Educativa:** La inmensa mayoría de usuarios indicaron que la app es una herramienta muy útil que favorece activamente su aprendizaje[cite: 96].

---

## 🚀 Instalación Local

### Requisitos previos
* [cite_start]Dispositivo móvil o emulador con **Android 8.0** o superior[cite: 85].
* [cite_start]Conexión a Internet[cite: 85].
* Android Studio instalado.

### Clonar el Repositorio

```bash
git clone [https://github.com/orlandu04/AgroExpert.git](https://github.com/orlandu04/AgroExpert.git)  [cite: 85]

Abre el proyecto en Android Studio.

Conecta tu proyecto a Firebase insertando tu archivo google-services.json en la carpeta app/.

Compila el proyecto (Build > Rebuild Project).

Ejecútalo en tu dispositivo físico o emulador.

📄 Generación de Reportes (LaTeX)
Para la generación de reportes avanzados y documentos formales del sistema (como los requeridos en eventos científicos), recomendamos utilizar el siguiente bloque LaTeX en el pie de página para referenciar las tecnologías y la comunidad. Requiere el paquete \usepackage{fontawesome5}.

Fragmento de código
\vspace{1cm}
\begin{center}
    \color{verdeMedio}\Large
    \faLeaf \quad \faMicrochip \quad \faUsers
\end{center}

\vspace{0.5cm}
\begin{center}
    \color{verdeMedio}\normalsize
    \begin{tabular}{rl} 
        \faFacebook & @agroexpert \\
        \faInstagram & @agroexpert \\
        \faTiktok & @agroexpert \\
        \faXTwitter & @agroexpert 
    \end{tabular}
\end{center}
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
