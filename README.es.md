# 🚀 Global Financial Data Platform (GCP)

### De Data Analyst a Data Engineer: Un Ecosistema de Datos de Extremo a Extremo

Este repositorio centraliza una plataforma de datos financiera diseñada para demostrar la convergencia entre el **procesamiento por lotes (Batch)**, el **monitoreo en tiempo real (Streaming)** y la **infraestructura como código (IaC)** en Google Cloud Platform.

---
## 🏗️ Arquitectura del Sistema

La plataforma se divide en dos capas operativas que conviven para ofrecer una visión 360° del mercado:

### 1. Layer de Análisis Histórico (Batch)
**Repositorio:** https://github.com/AFGU94/finance-lakehouse-gcp
* **Objetivo:** Ingesta masiva de datos históricos para análisis de tendencias y entrenamiento de modelos.
* **Stack:** Python (Yahoo Finance API), GCS (Bronze), BigQuery (Silver/Gold).
* **Highlights:** Implementación de particionamiento y clustering en BigQuery para optimización de costos y rendimiento.

### 2. Layer de Monitoreo Proactivo (Real-time)
**Repositorio:** https://github.com/AFGU94/real_time_monitor_streaming
* **Objetivo:** Detección de señales técnicas (RSI, EMA) en intervalos de 15 minutos para alertas inmediatas.
* **Stack:** Docker, Cloud Run Jobs, Firestore (State Management), Discord Webhooks.
* **Highlights:** Uso de Firestore para evitar redundancia de alertas y lógica de "promediado de precio" ante caídas de mercado.

---
## 🛠️ Stack Tecnológico & Cloud-Native

* **Infraestructura:** Terraform (IaC) para un despliegue replicable y seguro.
* **Cómputo:** Cloud Run Jobs (Serverless) para una ejecución eficiente en costos.
* **Base de Datos:** BigQuery (Analítica) y Firestore (NoSQL / Operativa).
* **Seguridad:** Google Secret Manager para gestión de API Keys.
* **DevOps:** Cleanup Policies en Artifact Registry para mantenimiento automático.

---
## 💰 Optimización de Costos (FinOps)

Uno de los pilares de este proyecto fue el diseño bajo el **GCP Always Free Tier**. 
- **BigQuery:** Uso de TTL (Time To Live) y particiones para mantenerse bajo los 10GB gratuitos.
- **Artifact Registry:** Políticas de limpieza automática para mantener una sola imagen activa.
- **Firestore:** TTL de 30 días para documentos de alerta.

---
## 📈 Evolución del Proyecto & Roadmap Profesional

Este ecosistema es el resultado de mi transición estratégica desde el análisis de datos hacia la arquitectura de infraestructura en la nube. Mi enfoque ha evolucionado en tres etapas clave:

1. **Fase Data Analyst (El "Qué"):** Comencé extrayendo valor de los datos financieros mediante análisis exploratorio (EDA) y visualización. Sin embargo, identifiqué que la calidad del análisis dependía totalmente de la robustez de la ingesta.
   
2. **Fase Associate Cloud Engineer (El "Dónde"):** Para construir soluciones profesionales, obtuve la certificación **Google Cloud Associate Cloud Engineer (ACE)**. Esto me permitió diseñar este ecosistema aplicando mejores prácticas de seguridad (IAM), gestión de recursos (Proyectos/Billing) y redes globales de GCP.
   **

3. **Fase Data Engineer (El "Cómo"):** Actualmente, escalo mis soluciones utilizando **Infraestructura como Código (Terraform)**, orquestación serverless y modelos de datos (Star Schema/Lakehouse). Este proyecto demuestra mi capacidad para gestionar el ciclo de vida completo del dato: desde la API hasta el insight, priorizando siempre la eficiencia de costos (FinOps).


**Contacto:**  https://www.linkedin.com/in/andresfelipegutierrezu/| pipegutierrez.u@gmail.com