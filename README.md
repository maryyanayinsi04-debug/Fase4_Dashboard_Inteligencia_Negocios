# Mapeo Científico y Análisis de Sentimiento mediante Bibliometría y PLN: Inteligencia Estratégica desde la Literatura Científica en Analítica Educativa

**Dashboard de inteligencia de negocios — Fase 4**
Curso: Métodos Cuantitativos y Cualitativos para los Negocios (107071)
Programa: Maestría en Administración de Organizaciones
Universidad Nacional Abierta y a Distancia (UNAD) — Escuela ECACEN

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maryyanayinsi04-debug/Fase4_Dashboard_Inteligencia_Negocios/blob/main/Fase4_Dashboard_Inteligencia_Negocios.ipynb)

> Actualizar el enlace del badge una vez creado el repositorio, reemplazando `maryyanayinsi04-debug/Fase4_Dashboard_Inteligencia_Negocios` por el usuario y nombre reales en GitHub.

## Integrantes

- Maryya Nayinsi Cossio Porras
- Carlos Augusto Sierra

**Tutora:** Ana González

## 1. Descripción del proyecto

Este repositorio contiene el flujo de trabajo analítico desarrollado para construir un dashboard de inteligencia de negocios que integra análisis bibliométrico y análisis de sentimiento sobre un corpus de 101 artículos científicos (Scopus, 2007–2026) del dominio de **analítica educativa e inteligencia artificial en educación superior**. El proyecto da continuidad al mapeo científico desarrollado en la Fase 3, incorporando en la Fase 4 un componente de modelado predictivo (machine learning), un dashboard dinámico y una interpretación estratégica generada con apoyo de un modelo de lenguaje de gran escala (LLM).

## 2. Problemática de negocio

Las instituciones de educación superior que operan en modalidad virtual y a distancia enfrentan el reto de decidir, con evidencia y no solo con intuición, en qué tecnologías de analítica educativa invertir (sistemas de alerta temprana, modelos predictivos de deserción, herramientas de PLN para retroalimentación) y en qué orden de prioridad implementarlas. La literatura científica crece de forma acelerada y dispersa, lo que dificulta una lectura sistemática por parte de los equipos directivos. Este proyecto convierte un corpus bibliográfico en inteligencia estratégica accionable: identifica líneas de investigación consolidadas frente a líneas emergentes, mide el tono predominante con que la comunidad científica evalúa estas tecnologías, proyecta la tendencia de crecimiento de la producción científica del campo y traduce todo ello en estrategias y KPIs concretos para la toma de decisiones institucionales.

## 3. Objetivos

**Objetivo general:** Construir un dashboard de inteligencia de negocios que integre análisis bibliométrico, análisis de sentimiento y modelado predictivo sobre la literatura científica de analítica educativa e IA en educación superior, para apoyar decisiones estratégicas de adopción tecnológica.

**Objetivos específicos:**
1. Consolidar los insumos bibliométricos y de sentimiento generados en la Fase 3 como base analítica del dashboard.
2. Modelar la tendencia de crecimiento de la producción científica mediante funciones de densidad de probabilidad y un modelo de machine learning, con sus respectivas métricas de desempeño.
3. Diseñar un dashboard dinámico que integre las salidas bibliométricas, de sentimiento y de modelado, junto con una interpretación estratégica generada por un LLM.
4. Formular estrategias de negocio y KPIs derivados de la problemática identificada.

## 4. Estructura del repositorio

```
NOMBRE-REPO/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── data/
│   └── corpus_scopus_101.csv          # Exportación cruda de Scopus (101 registros, 2007–2026)
├── notebooks/
│   └── Fase4_Dashboard_Inteligencia_Negocios.ipynb   # Notebook principal, ejecutable en Colab
├── biblioshiny/
│   ├── red_cocitacion.png             # Exportaciones de Bibliometrix/Biblioshiny
│   └── mapa_tematico.png
├── dashboard/
│   └── reporte_dashboard.pdf          # Gráficas + interpretación LLM en PDF (entregable Paso 8)
└── docs/
    └── informe_fase3.pdf              # Antecedente: informe de mapeo científico (Fase 3)
```

## 5. Entornos de trabajo

| Entorno | Herramienta | Uso |
|---|---|---|
| 1 | R / RStudio — Bibliometrix / Biblioshiny | Análisis bibliométrico, redes de co-citación, mapas temáticos |
| 2 | Google Colab (Python) | Carga de datos, NLP/BERT, modelado ML/PDF estadístico, dashboard, LLM |
| 3 | GitHub | Control de versiones y entrega final del repositorio |

Este notebook (`notebooks/Fase4_Dashboard_Inteligencia_Negocios.ipynb`) está diseñado para ejecutarse directamente en **Google Colab**.

## 6. Datos

- **Fuente:** Scopus.
- **Ecuación de búsqueda:** `TITLE-ABS-KEY ("learning analytics" OR "educational data mining" OR "student dropout prediction" OR "academic performance prediction") AND ("machine learning" OR "artificial intelligence" OR "deep learning") AND ("higher education" OR "university" OR "online learning")`.
- **Corpus:** 101 documentos, período 2007–2026.
- **Formato de entrega:** archivo `.csv` ubicado en `data/corpus_scopus_101.csv`.

## 7. Cómo ejecutar el proyecto

1. Abrir el notebook en Google Colab usando el badge de la parte superior de este README.
2. Montar Google Drive o subir manualmente `data/corpus_scopus_101.csv` cuando el notebook lo solicite.
3. Ejecutar las celdas en orden; cada paso de la guía de actividades corresponde a una sección del notebook.
4. El dashboard final (gráficas + interpretación LLM) se exporta automáticamente como PDF en `dashboard/reporte_dashboard.pdf`.

## 8. Lista de chequeo de la entrega (Fase 4)

- [ ] Datos: archivo `.csv` descargado de Scopus.
- [ ] NLP: el código genera una calificación de sentimiento.
- [ ] ML: modelo predictivo con métricas de desempeño.
- [ ] Dashboard: gráficas exportadas en PDF.
- [ ] LLM: cuadro de texto en el dashboard con interpretación estratégica.
- [ ] GitHub: repositorio público, código visible, README actualizado.

## 9. Referencias (APA 7.ª edición)

Aria, M., & Cuccurullo, C. (2017). bibliometrix: An R-tool for comprehensive science mapping analysis. *Journal of Informetrics, 11*(4), 959–975. https://doi.org/10.1016/j.joi.2017.08.007

Aria, M., & Cuccurullo, C. (2022, 25 de marzo). *A brief introduction to bibliometrix* [Viñeta del paquete]. Bibliometrix. https://www.bibliometrix.org/vignettes/Introduction_to_bibliometrix.html

Devlin, J., & Chang, M. (2019). BERT: Pre-training of deep bidirectional transformers for language understanding. En *Proceedings of NAACL-HLT 2019* (pp. 4171–4186). Association for Computational Linguistics. https://doi.org/10.18653/v1/N19-1423

Naveed, H., Khan, A. U., Qiu, S., Saqib, M., Anwar, S., Usman, M., Akhtar, N., Barnes, N., & Mian, A. (2023). *A comprehensive overview of large language models* (arXiv preimpresión n.º 2307.06435). arXiv. https://arxiv.org/pdf/2307.06435

Raschka, S., Liu, Y., & Mirjalili, V. (2023). *Machine learning con PyTorch y Scikit-Learn* (1.ª ed.). Marcombo. https://elibro-net.bibliotecavirtual.unad.edu.co/es/lc/unad/titulos/281644

Siemens, G., & Baker, R. S. (2012). Learning analytics and educational data mining: Towards communication and collaboration. En *Proceedings of the 2nd International Conference on Learning Analytics and Knowledge* (pp. 252–254). ACM. https://doi.org/10.1145/2330601.2330661

Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, L., & Polosukhin, I. (2017). *Attention is all you need* (arXiv preimpresión n.º 1706.03762). arXiv. https://doi.org/10.48550/arXiv.1706.03762

## 10. Licencia

Este proyecto se entrega con fines exclusivamente académicos, en el marco del curso Métodos Cuantitativos y Cualitativos para los Negocios (UNAD).
