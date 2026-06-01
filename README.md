# 🎵 Spotify Popularity Predictor

Proyecto Integrador — Desarrollo de Proyectos de Sistemas de Información  
**Universidad Internacional del Ecuador (UIDE) · Sexto Semestre · 2026**

> Predicción de popularidad de canciones en Spotify mediante técnicas de Machine Learning, aplicando la metodología CRISP-DM en un entorno cloud-first colaborativo.

---

## 👥 Equipo

| Nombre | Rama de desarrollo |
|---|---|
| Bryan Montaguano | `dev/bryan` |
| Sebastián Aucapiña | `dev/auca` |
| Testing | `test` |

---

## 📂 Dataset

**Spotify Tracks Dataset** — por [maharshipandya](https://www.kaggle.com/maharshipandya) en Kaggle

| Atributo | Detalle |
|---|---|
| 🔗 Fuente | [kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset) |
| 📊 Registros | ~114,000 canciones |
| 🎯 Variable objetivo | `popularity` (0–100) |
| 📥 Acceso | API de Kaggle (token configurado como secreto en el repositorio) |

### Características principales del dataset

| Feature | Descripción |
|---|---|
| `track_name` | Nombre de la canción |
| `artists` | Artista(s) |
| `album_name` | Nombre del álbum |
| `track_genre` | Género musical |
| `popularity` | Puntuación de popularidad (0–100) — **variable objetivo** |
| `duration_ms` | Duración en milisegundos |
| `danceability` | Qué tan bailable es la canción (0.0–1.0) |
| `energy` | Intensidad y actividad percibida (0.0–1.0) |
| `loudness` | Volumen promedio en dB |
| `speechiness` | Presencia de palabras habladas (0.0–1.0) |
| `acousticness` | Confianza de que la pista es acústica (0.0–1.0) |
| `instrumentalness` | Probabilidad de que no tenga vocales (0.0–1.0) |
| `liveness` | Presencia de audiencia en la grabación (0.0–1.0) |
| `valence` | Positividad musical de la pista (0.0–1.0) |
| `tempo` | Tempo estimado en BPM |
| `time_signature` | Compás estimado de la pista |

---

## 🏗️ Arquitectura del Proyecto

El proyecto opera sobre una arquitectura **cloud-first** organizada en tres capas:

```
┌─────────────────────────────────────────────────────────────┐
│  CAPA DE DATOS                                              │
│  Kaggle API → dataset (114k registros)                      │
│  GitHub → almacenamiento persistente del notebook           │
├─────────────────────────────────────────────────────────────┤
│  CAPA DE PROCESAMIENTO                                       │
│  GitHub Codespaces + devcontainer                           │
│  Python · Pandas · NumPy · Scikit-learn                     │
│  Matplotlib · Seaborn                                       │
├─────────────────────────────────────────────────────────────┤
│  CAPA DE COLABORACIÓN Y CONTROL                             │
│  GitHub (control de versiones)                              │
│  GitHub Projects (gestión ágil · Scrum + CRISP-DM)         │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔁 Metodología

El proyecto combina el marco ágil **Scrum** con la metodología **CRISP-DM**:

| Fase CRISP-DM | Sprint | Estado |
|---|---|---|
| Entendimiento del negocio + datos | Sprint 1 | ✅ En curso |
| Preparación de datos + transformación | Sprint 2 | 🔲 Pendiente |
| Modelado + evaluación + visualización | Sprint 3 | 🔲 Pendiente |

---

## 🗂️ Estructura del Repositorio

```
spotify-uide/
├── .devcontainer/
│   └── devcontainer.json       # Entorno reproducible
├── notebooks/
│   └── spotify_analysis.ipynb  # Notebook principal (Google Colab / Codespaces)
└── README.md
```

---

## ⚙️ Configuración del Entorno

### Requisitos previos

- Cuenta de GitHub con acceso al repositorio
- Credenciales de Kaggle (token API)


---

## 📋 Product Backlog (resumen por sprint)

| Sprint | Periodo | Historias | Objetivo |
|---|---|---|---|
| **Sprint 1** | 20 may – 02 jun 2026 | HU-01 a HU-08 | Entorno + entregables + EDA inicial |
| **Sprint 2** | 03 jun – 16 jun 2026 | HU-09 a HU-12 | Transformación + entrenamiento de modelos |
| **Sprint 3** | 17 jun – 26 jun 2026 | HU-13 a HU-15 | Visualización + documentación + entrega final |

🔗 **Tablero GitHub Projects:** [github.com/users/CtrlAltBryan/projects/1](https://github.com/users/CtrlAltBryan/projects/1)

---

## 🔒 Políticas de Gestión

- Cada integrante trabaja en su rama (`dev/bryan` · `dev/auca`) y hace PR a `main` al cerrar una HU
- Formato de commits: `[HU-XX] Descripción breve`
- No se almacenan credenciales ni datos sensibles en el repositorio
- Semilla fija en todos los experimentos de ML para garantizar reproducibilidad
- El docente tiene acceso de **solo lectura** al repositorio y al tablero

---

## 📚 Referencias

- IBM SPSS Modeler. *CRISP-DM Help Overview*. https://www.ibm.com/docs/es/spss-modeler/saas?topic=dm-crisp-help-overview
- Winks, E. (2024). *Cloud First vs Cloud Native: Key Differences for 2025*. Atlan. https://atlan.com/cloud-first-vs-cloud-native/
- Pandya, M. (2022). *Spotify Tracks Dataset*. Kaggle. https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset
