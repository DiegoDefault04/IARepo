# 🤖 Inteligencia Artificial (IA) – Guía Completa

Este repositorio es una **guía introductoria y práctica sobre Inteligencia Artificial (IA)**, enfocada en explicar **qué tipos de modelos existen**, **cómo funcionan**, **cómo se entrenan**, **qué es el fine-tuning**, **qué librerías se usan en Python** y **por qué la GPU es clave en Deep Learning**.

Pensado para estudiantes, desarrolladores y personas que quieren construir bases sólidas en IA.

---

## 🧠 ¿Qué es la Inteligencia Artificial?

La Inteligencia Artificial es una rama de la computación que permite a las máquinas:

- Aprender a partir de datos
- Reconocer patrones
- Tomar decisiones
- Resolver problemas complejos

En lugar de reglas fijas, los modelos **aprenden automáticamente** a partir de ejemplos.

---

## 📚 Tipos de modelos de IA

### 1️⃣ Aprendizaje Supervisado
Aprende con datos etiquetados (entrada + respuesta correcta).

Ejemplos:
- Clasificación de correos
- Diagnóstico médico
- Predicción de precios

Modelos comunes:
- Regresión lineal / logística
- Árboles de decisión
- Random Forest
- Redes neuronales

---

### 2️⃣ Aprendizaje No Supervisado
Trabaja con datos sin etiquetas y busca patrones ocultos.

Ejemplos:
- Segmentación de clientes
- Agrupación de imágenes
- Detección de anomalías

Modelos:
- K-Means
- DBSCAN
- PCA

---

### 3️⃣ Aprendizaje por Refuerzo
Un agente aprende por prueba y error mediante recompensas.

Ejemplos:
- Videojuegos
- Robótica
- Sistemas autónomos

---

### 4️⃣ Deep Learning
Usa redes neuronales profundas para resolver problemas complejos.

Aplicaciones:
- Visión por computadora
- NLP
- Audio

---

## 🧠 ¿Cómo funciona una red neuronal?

Una red neuronal está compuesta por neuronas artificiales organizadas en capas:

Entrada → Capas ocultas → Salida

Cada conexión tiene un peso que indica su importancia.

---

## 🔢 ¿Qué hace una neurona?

1. Recibe entradas
2. Multiplica por pesos
3. Suma los valores
4. Aplica una función de activación
5. Produce una salida

Fórmula:
salida = activación((x · w) + b)

---

## 📌 ¿Qué es una red neuronal?

Una **red neuronal** es una forma en la que una computadora aprende a **tomar decisiones**, inspirada en el cerebro humano.

- Aprende con ejemplos
- Se equivoca
- Corrige
- Mejora con la práctica

📌 *No piensa como un humano, pero aprende ajustando números.*

---

## 🧩 Ejemplo práctico

### ❓ Pregunta que resolverá la red
**¿Debo ponerme chamarra? 🧥**

---

## 🟦 Paso 1: Entradas (lo que la red recibe)

La red recibe información del entorno:

```
🌡️ Temperatura = 10°C
🌬️ Viento = fuerte
🌧️ Lluvia = sí
```

La red solo entiende números:

```
x1 = 10   (temperatura)
x2 = 1    (viento fuerte)
x3 = 1    (lluvia)
```

### Dibujo:
```
[ 10 ]   [ 1 ]   [ 1 ]
  🌡️      🌬️      🌧️
```

---

## ⚖️ Paso 2: Pesos (importancia de cada dato)

La red decide qué tan importante es cada cosa:

```
w1 = 0.6  → temperatura (muy importante)
w2 = 0.3  → viento (importancia media)
w3 = 0.1  → lluvia (poca importancia)
```

### Dibujo:
```
[10] --×0.6-->
[ 1] --×0.3-->
[ 1] --×0.1-->
```

---

## 🧮 Paso 3: Multiplicar y sumar

La neurona hace este cálculo:

```
(10 × 0.6) = 6
(1 × 0.3)  = 0.3
(1 × 0.1)  = 0.1
----------------
Suma = 6.4
```

### Dibujo:
```
   6
 + 0.3
 + 0.1
 ------
   6.4
```

🧠 *"Parece que hace frío"*

---

## ➕ Paso 4: Bias (personalidad de la neurona)

El **bias** ajusta la decisión final.

Ejemplo:
```
bias = -5

6.4 - 5 = 1.4
```

### Dibujo:
```
   6.4
 - 5.0
 ------
   1.4
```

---

## 🚦 Paso 5: Función de activación (decisión final)

Regla simple:

```
Si resultado > 0  → 🧥 Sí chamarra
Si resultado ≤ 0  → ❌ No chamarra
```

Resultado:
```
1.4 > 0 → 🧥 SÍ
```

### Dibujo final:
```
        🟣
     ┌───────────┐
     │ ¿Chamarra?│
     └───────────┘
            ↓
          🧥 SÍ
```

---

## 🧠 Todo el proceso junto

```
[10]   [1]   [1]
 🌡️    🌬️    🌧️
  |     |     |
 ×0.6  ×0.3  ×0.1
  |     |     |
  6   +0.3  +0.1
        ↓
      6.4
        ↓
     bias -5
        ↓
      1.4
        ↓
   FUNCIÓN
        ↓
      🧥 SÍ
```

---

## 🔁 ¿Cómo aprende una red neuronal?

1. Da una respuesta
2. Se compara con la respuesta correcta
3. Calcula el error
4. Ajusta los pesos y el bias
5. Repite miles de veces

📌 *Aprende igual que una persona practicando.*

---

## ⚡ Funciones de activación

- ReLU (la más usada)
- Sigmoid
- Softmax
- Tanh

Permiten aprender relaciones no lineales.

---

## 🔁 ¿Cómo aprende una red?

1. Forward pass
2. Cálculo de pérdida (loss)
3. Backpropagation (ajuste de pesos)

---

## 📆 Epochs

Un epoch es una pasada completa del dataset por el modelo.

Ejemplo:
- Dataset de 1,000 muestras
- 10 epochs = el modelo ve los datos 10 veces

---

## 📦 Batch Size

Cantidad de datos procesados al mismo tiempo.

Ejemplo:
- Dataset: 1,000
- Batch size: 100
- 1 epoch = 10 batches

---

## 🎯 Learning Rate

Controla qué tan rápido aprende el modelo.

Muy alto → inestable  
Muy bajo → lento

---

## 🧪 Overfitting vs Underfitting

Overfitting:
- Memoriza datos
- Falla con datos nuevos

Underfitting:
- No aprende lo suficiente

---

## 🔧 Fine-Tuning

Consiste en ajustar un modelo preentrenado a un problema específico.

Ventajas:
- Menos datos
- Menos tiempo
- Mejores resultados

---

## 🐍 Librerías en Python

Básicas:
pip install numpy pandas matplotlib

Machine Learning:
pip install scikit-learn

Deep Learning:
pip install torch torchvision torchaudio

NLP:
pip install transformers datasets

Visión:
pip install opencv-python pillow

---

## 🚀 ¿Por qué usar GPU?

Las GPUs permiten miles de operaciones en paralelo.

Beneficios:
- Entrenamiento mucho más rápido
- Ideal para Deep Learning
- Uso de CUDA

Ejemplo PyTorch:

device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
model.to(device)

---

## 📦 Flujo típico de IA

1. Recolección de datos
2. Limpieza
3. Entrenamiento
4. Evaluación
5. Fine-tuning
6. Despliegue

---

## 📌 Recomendaciones

- Usa modelos preentrenados
- Entrena en GPU
- Guarda checkpoints
- Usa Docker

---

## 🏁 Conclusión

La IA combina datos, modelos y cómputo.  
Entender conceptos como **epochs**, **batch size** y **fine-tuning** es clave para construir modelos reales.
