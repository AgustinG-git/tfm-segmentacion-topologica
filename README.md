# Métodos topológicos en segmentación de imágenes

Repositorio con el código y los experimentos del Trabajo de Fin de Máster (TFM) del Máster en Lógica, Computación e Inteligencia Artificial.

**Autor:** [Tu Nombre/Usuario]  
**Tutor:** Manuel Soriano Trigueros  
**Fecha prevista de finalización:** Noviembre 2026  

---

## 📌 Descripción del Proyecto

Este repositorio explora y evalúa enfoques basados en grafos y topología para la segmentación de imágenes. El objetivo es analizar cómo la integración de restricciones topológicas (garantizando métricas como conectividad, homología y equivalencia homotópica) afecta al rendimiento y la eficiencia computacional respecto a las funciones de pérdida estándar a nivel de píxel.

## 📂 Estructura del Repositorio

Para evitar conflictos de dependencias y separar claramente el estado del arte de las contribuciones propias, el repositorio sigue una arquitectura modular aislada:

*   **/baselines/**: Implementaciones de referencia oficiales (estado del arte). El código aquí se mantiene lo más fiel posible a las fuentes originales.
    *   `topograph_oficial/`: Código oficial del paper *Topograph* (ICLR 2025).
    *   `cldice/`: Implementación de referencia para segmentación de estructuras tubulares.
*   **/propuestas/**: Contribuciones originales, adaptaciones y variaciones algorítmicas desarrolladas durante este TFM.
    *   `topograph_adaptado/`: Modificaciones sobre la pérdida de *Topograph*.
    *   `[otros_experimentos]/`: Nuevas arquitecturas o funciones de pérdida.
*   **/notebooks/**: Entornos interactivos sincronizados desde Kaggle Notebooks.
    *   `exploracion/`: Análisis exploratorio de los datasets.
    *   `resultados/`: Generación de métricas, gráficas comparativas (DIU, Betti Matching) y tablas para la memoria.
*   **/data/**: Scripts automatizados para la descarga y preprocesamiento de datos (las imágenes no se suben al repositorio).
*   **/docs/**: Documentación adicional, diagramas metodológicos y esquemas exportados para Overleaf.

## ⚙️ Entornos y Ejecución

Dado que cada enfoque en `baselines/` y `propuestas/` puede requerir versiones distintas de librerías (ej. distintas versiones de PyTorch o dependencias topológicas específicas), **cada subdirectorio contiene su propio archivo `requirements.txt`**.

Para ejecutar un modelo específico, navega a su directorio e instala sus dependencias locales:

```bash
cd baselines/topograph_oficial
pip install -r requirements.txt
python train.py
