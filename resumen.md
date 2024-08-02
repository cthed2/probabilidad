# Probabilidad: La Ciencia de la Incertidumbre y los Datos
por Fabián Kozyinski

---

## Probabilidad

### Modelos y axiomas de probabilidad

**Definición (Espacio muestral):**  
Un espacio muestral \(\Omega\) es el conjunto de todos los resultados posibles. Los elementos del conjunto deben ser mutuamente excluyentes, colectivamente exhaustivos y del nivel de granularidad correcto.

**Definición (Evento):**  
Un evento es un subconjunto del espacio muestral. Se asigna probabilidad a los eventos.

**Definición (Axiomas de probabilidad):**  
Una ley de probabilidad \(P\) asigna probabilidades a eventos y satisface los siguientes axiomas:

- **No negatividad:** \(P(A) \geq 0\) para todos los eventos \(A\).
- **Normalización:** \(P(\Omega) = 1\).
- **Aditividad (contable):** Para cualquier secuencia de eventos \(A_1, A_2, \ldots\) tales que \(A_i \cap A_j = \emptyset\) para \(i \neq j\):

  \[
  P\left(\bigcup_i A_i\right) = \sum_i P(A_i)
  \]

**Corolarios (Consecuencias de los axiomas):**

- \(P(\emptyset) = 0\).
- Para cualquier colección finita de eventos disjuntos \(A_1, \ldots, A_n\):

  \[
  P\left(\bigcup_{i=1}^n A_i\right) = \sum_{i=1}^n P(A_i)
  \]

- \(P(A) + P(A^c) = 1\).
- \(P(A) \leq 1\).
- Si \(A \subseteq B\), entonces \(P(A) \leq P(B)\).
- \(P(A \cup B) = P(A) + P(B) - P(A \cap B)\).
- \(P(A \cup B) \leq P(A) + P(B)\).

**Ejemplo (Ley uniforme discreta):**  
Supongamos que \(\Omega\) es finito y consiste en \(n\) elementos igualmente probables. Además, supongamos que \(A \subseteq \Omega\) con \(k\) elementos. Entonces \(P(A) = \frac{k}{n}\).

---

### Condicionalidad y Regla de Bayes

**Definición (Probabilidad condicional):**  
Dado que el evento \(B\) ha ocurrido y que \(P(B) > 0\), la probabilidad de que ocurra \(A\) es:

\[
P(A|B) \triangleq \frac{P(A \cap B)}{P(B)}
\]

**Observación (Propiedades de las probabilidades condicionales):**  
Son las mismas que las probabilidades ordinarias. Asumiendo \(P(B) > 0\):

- \(P(A|B) \geq 0\).
- \(P(B|B) = 1\).
- \(P(\Omega|B) = 1\).
- Si \(A \cap C = \emptyset\), \(P((A \cup C)|B) = P(A|B) + P(C|B)\).

**Proposición (Regla de multiplicación):**

\[
P(A_1 \cap A_2 \cap \cdots \cap A_n) = P(A_1) \cdot P(A_2|A_1) \cdot \ldots \cdot P(A_n|A_1 \cap \cdots \cap A_{n-1})
\]

**Teorema (Teorema de la probabilidad total):**  
Dada una partición \(\{A_1, A_2, \ldots\}\) del espacio muestral, significando que \(\bigcup_i A_i = \Omega\) y que los eventos son disjuntos, y para cualquier evento \(B\), tenemos:

\[
P(B) = \sum_i P(A_i) P(B|A_i)
\]

