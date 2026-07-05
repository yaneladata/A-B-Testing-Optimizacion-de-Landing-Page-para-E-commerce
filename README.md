# 🧪 A/B Testing: Optimización de Landing Page para E-commerce

## 📌 Resumen Ejecutivo
Este proyecto analiza un experimento A/B en un e-commerce para comparar dos versiones de una landing page.  
Los resultados muestran que la **Página B** logra una mayor tasa de conversión (+3.38 pp) y un mayor gasto promedio (+$7.66), con un impacto económico estimado de **+$66,000** en ingresos adicionales.  

**Conclusión clave:** Por los resultados obtenidos del análisis realizado, migrar gradualmente a la Página B maximiza la conversión y el ingreso, sin necesidad de segmentar por canal de tráfico ni tipo de usuario.

---

## 📊 Principales Hallazgos
- **Página B** convierte más usuarios y genera mayor gasto promedio.  
- Diferencias estadísticamente significativas (p < 0.05).  
- Canales de tráfico y tipo de usuario no muestran diferencias con valor accionable.  

---

## 💡 Recomendaciones
- Se sugiere implementar la Página B de forma gradual (25% → 100%).  
- Monitorear conversión y gasto semana a semana.  
- Se ssugiere enfocar esfuerzos en optimización de diseño, más que en segmentación por canal o tipo de usuario.  

---

# 🔬 Detalles del Proyecto

## 📌 Objetivo
Evaluar un experimento A/B realizado en la página de inicio de un e-commerce para apoyar una decisión de negocio basada en datos: ¿qué versión de la página (A o B) debería implementarse de forma permanente?

**Preguntas de negocio:**
- ¿Qué página genera mayor conversión y gasto promedio?
- ¿Qué canales de tráfico son más efectivos para generar conversiones?
- ¿Existen diferencias significativas según el tipo de usuario?
- ¿Qué recomendaciones se pueden tomar para optimizar la estrategia de marketing?

## 📂 Conjunto de datos
El archivo contiene información de ~40,000 usuarios expuestos a dos versiones de una landing page durante 28 días (1–28 de enero).

**Columnas:**
- `user_id`: Identificador único del usuario  
- `date`: Fecha de exposición  
- `landing`: Versión de la página (A o B)  
- `region`: Región geográfica  
- `device`: Tipo de dispositivo (Mobile / Desktop)  
- `traffic_source`: Canal de tráfico (Ads, Email, Orgánico, Referencia)  
- `user_type`: Tipo de usuario (Nuevo / Recurrente)  
- `converted`: Conversión (0 = No, 1 = Sí)  
- `spend`: Monto gastado  

El dataset no presenta valores ausentes ni duplicados.

## 🛠️ Herramientas y librerías
- Python (pandas, numpy)  
- `scipy.stats` — pruebas t y chi-cuadrado  
- `statsmodels` — prueba z de proporciones  
- Matplotlib / Seaborn — visualización  

## 🔬 Metodología
1. Carga y validación de datos  
2. Comparación de gasto promedio (A vs. B)  
3. Comparación de tasa de conversión (A vs. B)  
4. Relación entre canal de tráfico y conversión  
5. Relación entre tipo de usuario y conversión  
6. Visualización de resultados  
7. Insight ejecutivo y estimación de impacto económico  

## 📊 Hallazgos principales
**Página A vs. Página B**
| Métrica              | Página A | Página B | Diferencia | Prueba | p-valor    |
|----------------------|----------|----------|------------|--------|------------|
| Tasa de conversión   | 12.57%   | 15.96%   | +3.38 pp   | z-test | 3.76×10⁻²² |
| Gasto promedio       | $61.09   | $68.75   | +$7.66     | t-test | 1.06×10⁻²⁰ |

👉 Ambas diferencias son estadísticamente significativas. La Página B convierte más usuarios y genera mayor gasto promedio.

**Segmentación por canal de tráfico**  
- Email (14.99%) y Ads (14.74%) más altos.  
- Orgánico (13.79%) y Referencia (13.88%) más bajos.  
- Asociación estadísticamente significativa pero de magnitud mínima (p=0.034).  

**Segmentación por tipo de usuario**  
- Nuevos (14.36%) vs. Recurrentes (14.09%).  
- Diferencia mínima (0.27 pp), no significativa (p=0.474).  

## 💡 Recomendaciones de negocio
- Se sugiere migrar gradualmente el tráfico a la Página B.  
- Impacto económico estimado: **+$66,000** en ingresos adicionales.  
- Se sugiere no priorizar canal ni tipo de usuario como criterios de segmentación.  

## ⚠️ Limitaciones
- Período breve (28 días, enero).  
- Posible efecto “novedad” en la Página B.  
- Impacto económico proyectado sin incluir costos de implementación.  

## 🔜 Próximos pasos
- Monitorear conversión y gasto semana a semana tras despliegue.  
- Analizar variables adicionales como región y dispositivo.  

---

## 📂 Estructura del repositorio
- `readme.md`
- `data/` → datasets original.
- `notebooks/` → notebooks de análisis.
- `visualizaciones/` → gráficos generados.
- 
Este proyecto forma parte de mi portfolio de análisis de datos, integrando estadística aplicada y visión de negocio.
