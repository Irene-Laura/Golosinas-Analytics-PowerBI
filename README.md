# 🍭 Business Intelligence: Análisis de Ventas y Rentabilidad

Este proyecto representó el **puntapié inicial** en mi transición hacia el análisis de datos avanzado. Utilicé Power BI para transformar un conjunto de datos transaccionales en una herramienta estratégica de toma de decisiones para una tienda de golosinas.

## 🌟 El Origen del Proyecto
A partir de registros de facturación en Excel, detecté la necesidad de centralizar la información para responder preguntas críticas: ¿Qué productos tienen mayor facturación? ¿Qué vendedores están superando sus metas? ¿Cómo varía el crecimiento mes a mes?

Este análisis fue tan exitoso que posteriormente decidí escalarlo y recrear sus funcionalidades en un entorno de desarrollo con **R Shiny** (también disponible en mi perfil).

## 🛠️ Stack Tecnológico
* **Power Query (M):** Limpieza, normalización y transformación de datos.
* **Modelado:** Creación de un esquema en estrella (*Star Schema*) para conectar ventas, productos, canales y tiempos.
* **DAX:** Implementación de métricas de crecimiento interanual y lógica de detección de nuevos clientes/vendedores.

## 💡 Lógica DAX Destacada
Para este reporte desarrollé medidas que permiten una visión dinámica del negocio:

### 1. Crecimiento Interanual (YoY)
Crecimiento en % = DIVIDE([Crecimiento Absoluto], [Facturación año anterior], 0)

### 2. Segmentación de Nuevos Vendedores
Vendedor Solo Año Actual = IF([Facturación Total] > 0 && [Facturación año anterior] = 0, 1, 0)

### 3. Métricas de Operatividad
Fragmento de código
Promedio por Factura = AVERAGE(H_Base[total])
Canales de Venta = DISTINCTCOUNT(H_Base[canal])

## 📸 Visualización

Aqui se puede ver la interfaz y la estructura del modelo:

Vista del Dashboard
<img width="1424" height="788" alt="captura datos principales" src="https://github.com/user-attachments/assets/6809c76b-1086-4282-979d-46c284b2f333" />
<img width="1422" height="799" alt="captura dashboard dinamico" src="https://github.com/user-attachments/assets/c99ede81-9853-441f-a777-7649349ecdb5" />

Modelado Relacional
<img width="1192" height="789" alt="captura modelo de datos" src="https://github.com/user-attachments/assets/7fd2056b-de65-48d6-a975-0a92df7d8679" />

📂 Datos: Se adjunta el archivo Excel original para transparencia en el proceso de ETL.
