# 🧠 KNN desde cero y comparación con KStar (Weka)

Implementación del algoritmo **k-Nearest Neighbors (KNN)** completamente **desde cero en Python**, aplicada al conjunto de datos clásico **Wine**.  
El proyecto incluye la evaluación del modelo mediante **validación cruzada (5-fold)** y **Leave-One-Out (LOOCV)**, además de la comparación con el clasificador **KNN de scikit-learn** y el algoritmo **KStar** de **Weka**.
---

## ⚙️ Características principales

- Implementación manual del algoritmo **KNN**, sin uso de librerías de machine learning.  
- Métricas de distancia disponibles:
  - Euclidiana  
  - Manhattan  
  - Coseno  
- Selección del parámetro óptimo \( k \) mediante **validación cruzada 5-fold**.  
- Evaluación de desempeño mediante:
  - Accuracy  
  - Matriz de confusión  
  - Validación **LOOCV (Leave-One-Out)**  
- Comparación con:
  - `KNeighborsClassifier` de **scikit-learn**  
  - **KStar** (métrica basada en entropía) de **Weka**

---

## 📊 Resultados principales

| Distancia  | k óptimo | Accuracy (CV) | Accuracy (LOOCV) | Accuracy sklearn (CV) |
|-------------|-----------|----------------|-------------------|------------------------|
| Euclidiana  | 15 | 0.9776 | 0.9775 | 0.9775 |
| Manhattan   | 17 | 0.9778 | 0.9775 | 0.9719 |
| Coseno      | 3  | 0.9722 | 0.9663 | 0.9551 |

**KStar (Weka, B=20):** Accuracy = **73.0 %**

---

## 🚀 Ejecución

Para ejecutar el modelo, abre el notebook:
```bash
Script_KNN_MargotPaco.ipynb
```

### 🔹 Opción 1 — Desde Jupyter Notebook o JupyterLab
1. Abre tu entorno Jupyter (`jupyter notebook` o `jupyter lab` en la terminal).  
2. Navega hasta el archivo `Script_KNN_MargotPaco.ipynb`.  
3. Ejecuta las celdas en orden (menú **Kernel → Restart & Run All**).

### 🔹 Opción 2 — Desde VS Code o Google Colab
- En **VS Code**, instala la extensión *Jupyter* y abre el `.ipynb` directamente.  
- En **Google Colab**, sube el notebook y ejecuta las celdas online (solo necesitas `numpy` y `pandas`).

### 🔧 Parámetros configurables
Dentro del notebook puedes modificar los valores de **k** y **distancia**:
```python
k = 15
dist_name = "euclidean"  # opciones: "manhattan", "cosine"
```

---

## 🧾 Informe

El proyecto incluye un informe académico en formato PDF con los resultados, análisis y comparaciones:
📄 `Informe_KNN_MargotPaco.pdf`

---

## 🧩 Conclusiones

- La implementación manual del algoritmo KNN reproduce correctamente los resultados del modelo de **scikit-learn**, validando su funcionamiento.  
- Las métricas **Euclidiana** y **Manhattan** ofrecen el mejor rendimiento (≈97.7 % de exactitud).  
- La distancia **del Coseno** presenta una ligera disminución en precisión debido a su dependencia angular.  
- El clasificador **KStar** de **Weka**, basado en entropía, obtiene un rendimiento menor (≈73 %) al aplicarse sobre un conjunto puramente numérico y bien separado como *Wine*.

---

## 🧪 Requisitos

- Python ≥ 3.8  
- NumPy ≥ 1.24  
- Pandas (solo para manejo de datos CSV)  
- Weka (para la comparación con KStar)
---

## 👩‍💻 Autora

**Margot P.C.**  
📘 [Repositorio en GitHub](https://github.com/MargotPC/KNN-from-Scratch-wine-)
