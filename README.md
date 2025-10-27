# 🌿 Grow2IoT: Sistema de Monitorización y Control de Invernaderos por IoT

Este proyecto ofrece una solución completa de automatización para invernaderos. Utiliza una robusta **arquitectura Maestro-Esclavo (PC/Java ↔ Arduino)** para la adquisición de datos, la lógica de control avanzada y la persistencia remota de datos en una base de datos MySQL.

**El objetivo es transformar un Arduino en una estación de control de campo (Capa Hardware) y centralizar la lógica compleja, la gestión de datos y el análisis en una aplicación Java (Capa Lógica).**

### ⚖️ Licencia y Filosofía

Este proyecto está liberado bajo la **Licencia Pública General de GNU, Versión 3 (GPLv3)**.

**Filosofía:** El uso de GPLv3 asegura que **el código fuente y todas sus modificaciones permanezcan libres y accesibles para toda la comunidad.** Buscamos fomentar un ecosistema de *software* libre donde nadie pueda tomar este trabajo, mejorarlo y distribuirlo como un producto de código cerrado o propietario.

---

## 🗺️ Arquitectura del Sistema

El sistema Grow2IoT se basa en cuatro capas interconectadas, garantizando modularidad y escalabilidad.

| Capa | Dispositivo / Plataforma | Función Principal | Comunicación Clave |
| :--- | :--- | :--- | :--- |
| **1. Hardware** | Arduino Mega | Adquisición de datos (sensores) y Actuación (ventiladores, válvulas). | Serial/USB |
| **2. Lógica** | PC con **Java** | Aplica decisiones complejas y gestiona la comunicación DB. | Serial & JDBC |
| **3. Almacenamiento** | Servidor Remoto (**MySQL**) | Persistencia de registros históricos (**datalogging 24/7**). | JDBC |
| **4. Visualización** | App Móvil / Web | Interfaz de usuario, gráficos de métricas y control remoto. | API (HTTP/S) |

Nota: El proyecto está en construcción, la idea de implementar IA esta a punto de encajar. Gracias al aprendizaje continuo podremos obtener mejoras en el cuidado de nuestros cultivos. Cabe también la posibilidad de que con cámaras podamos detectar plagas y otras sintomatologías que puedan aparecer y actuar a tiempo con alertas. Este Readme solo es el principio.

---

## 🛠️ Requisitos del Sistema

### Hardware (Capa 1)

* **Microcontrolador:** Arduino Mega (o compatible).
* **Sensores Mínimos:** Sensor de temperatura y humedad tipo HT11 o similar.
* **Actuadores:** Módulos de relé para sistemas de riego y ventilación.
* **Conexión:** PC con puerto USB.

### Software (Capas 2, 3 y 4)

| Componente | Uso Principal | Ubicación del Código |
| :--- | :--- | :--- |
| **Arduino IDE** | Carga del *Sketch* (`.ino`). | `./arduino_sketch` |
| **Java Development Kit (JDK)** | Ejecución de la lógica central (requiere librerías JDBC y Serial). | `./java_logic` |
| **MySQL Server** | Base de datos de registros históricos. | Servidor Remoto |
| **Servidor Web (Apache)** | Alojamiento de la API para la visualización móvil. | `./api_web` |

---

## 🚀 Guía de Instalación Rápida

### 1. Configuración de la Base de Datos (MySQL)

### 2. Carga del Sketch de Arduino

### 3. Ejecución de la Lógica Java

## 🤝 Contribuciones y Contacto

¡Grow2IoT es un proyecto **Open Source** y valoramos tus contribuciones!

* **Reportar Errores:** Por favor, usa la sección **Issues** de este repositorio.
* **Contribuir Código:** Revisa el archivo `CONTRIBUTING.md` para las directrices. **Recuerda:** Todas las contribuciones deben adherirse a los términos de la Licencia GPLv3.

Para consultas directas, puedes contactarme en: ....
