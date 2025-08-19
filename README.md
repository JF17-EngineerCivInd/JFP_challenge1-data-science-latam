# Alura Store LATAM — Informe de Análisis

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JF17-EngineerCivInd/JFP_challenge1-data-science-latam/blob/main/AluraStoreLatam.ipynb?authuser=3#scrollTo=GQPGHbrGPse3)

**Autor:** Jimmy Nicolás Flores Pinto  
**Objetivo:** Identificar la **tienda menos eficiente** para recomendar su venta, utilizando facturación, unidades vendidas, calificación promedio y costo de envío.

---

## 1) Propósito
Unificar y analizar los datos de **4 tiendas** de *Alura Store* para compararlas de forma justa y decidir **qué tienda conviene vender**, con argumentos basados en datos.

---

## 2) Metodología (resumen)
- **Unificación** de los 4 CSV en un único `DataFrame`, con etiqueta `Tienda`.
- **Limpieza ligera**: normalización de tipos (fechas/números) y nombres de columnas.
- **KPIs por tienda**:
  - **Facturación** (suma de `Precio`)
  - **Unidades vendidas** (conteo de `Producto`)
  - **Calificación promedio** (promedio de `Calificación`)
  - **Costo de envío promedio** (promedio de `Costo de envío`)
- **Score compuesto (Min–Max, ponderado)**  
  Facturación **40%**, Calificación **30%**, Unidades **20%**, Envío **10%** (menor costo → mejor).
- **Visualizaciones interactivas** con Plotly (y apoyo de Matplotlib).

---

## 3) Resultados (highlights)
- **Tienda recomendada para vender:** **Tienda 4**  
  Presenta el **menor desempeño compuesto** por combinación de **menor facturación** y **menor volumen**; la calificación es similar al resto (~4.0) y su ventaja en costo de envío **no** compensa el bajo rendimiento.
- **Mejor desempeño general:** **Tienda 2** (destaca en facturación y unidades).
- **Ventas por categoría:** Muebles y Electrónicos dominan en todas las tiendas.
- **Top 5 por tienda:** el *mix* de productos líderes es diferente por tienda → sugiere acciones de surtido y reposición específicas.

> **Conclusión:** vender **Tienda 4** y optimizar categorías, costos de envío y experiencia del cliente en las tiendas restantes.

---

## 4) Visualizaciones incluidas
- **Facturación por tienda** (barras; escala en MM COP).
- **Ventas por categoría**:
  - Línea comparativa (4 tiendas en un gráfico).
  - Pasteles 2×2 (una rosca por tienda).
- **Calificación promedio por tienda** (línea con marcadores).
- **Top 5 productos más vendidos** (4 paneles, uno por tienda).
- **Costo de envío promedio** (dispersión).

> Todas las gráficas son **interactivas**: leyendas clicables y *tooltips* con detalle.

---

## 5) Estructura del proyecto
.
├── base-de-datos-challenge1-latam/ # CSV de las 4 tiendas (del repositorio base)
├── AluraStoreLatam.ipynb # Notebook con el análisis
└── README.md # Este archivo


---

## 6) Cómo abrir el notebook
- **En Colab (recomendado):**  
  https://colab.research.google.com/github/JF17-EngineerCivInd/JFP_challenge1-data-science-latam/blob/main/AluraStoreLatam.ipynb?authuser=3#scrollTo=GQPGHbrGPse3
- **En GitHub:**  
  https://github.com/JF17-EngineerCivInd/JFP_challenge1-data-science-latam/blob/main/AluraStoreLatam.ipynb

> Si Colab muestra “Guardar en GitHub para conservar los cambios”, utiliza ese botón para *commitear* tus ediciones al repo.

---

## 7) Requisitos (ejecución local opcional)
```bash
pip install pandas plotly matplotlib
Python 3.10+ recomendado.

## 8) Licencia

Uso educativo para el challenge de Alura LATAM.

## 9) Referencias

Guía Alura: Cómo escribir un README increíble en tu GitHub
https://www.aluracursos.com/blog/como-escribir-un-readme-increible-en-tu-github
