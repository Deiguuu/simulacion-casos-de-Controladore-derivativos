# ⚡ Laboratorio Interactivo de Sistemas de Control Automático

Repositorio centralizado que recopila simulaciones interactivas basadas en web orientadas a la enseñanza, análisis y diseño de **sistemas de control clásico y moderno** (Control P, PI, PD y PID), con especial énfasis en el **análisis de la acción derivativa ($D$)**, reducción de ruido en sensores y mitigación del *golpe derivativo*.

---

## 🛠️ Proyectos Incluidos

### 1. 🤖 Control PD en Robot Autobalanceado (Péndulo Invertido Móvil)
* **Descripción:** Simulación en tiempo real de la estabilización de un robot autobalanceado de dos ruedas modelado como un péndulo invertido móvil. 
* **Conceptos Clave:** Dinámica de sistemas inestables (\(a > 0\)), ganancia proporcional (\(K_p\)), amortiguamiento giroscópico (\(K_d\)), plano de fase, ubicación de polos en el semiplano derecho e izquierdo ($s$-plane) y filtrado de ruido en sensores.
* **Características:** Interfaz interactiva para alterar parámetros de inestabilidad, aplicar perturbaciones (empujones), añadir carga útil y visualizar diagramas de fase en vivo.

### 2. 🦾 Posicionamiento de Articulación con Servomotor de CD
* **Descripción:** Banco de pruebas virtual para el control de posición angular de un servomotor de corriente directa (modelo DM-J4340-2EC) acoplado a un brazo robótico.
* **Conceptos Clave:** Comparativa directa de control P vs. control PD, cero del controlador derivativo, cuantización de encoders, efectos de saturación en el driver (\(\pm 24\,\text{V}\)) y filtros derivativos con constante de corte ($N$).
* **Características:** Gráficas duales en tiempo real de respuesta temporal de la posición \(\theta(t)\) y de la tensión de control \(u(t)\).

### 3. 🔥 Control PID de Temperatura en Horno Industrial
* **Descripción:** Simulación térmica de procesos de orden superior con gran inercia y retardo de transporte, orientada a la industria de tratamiento térmico de metales.
* **Conceptos Clave:** Sintonización por el método de Ziegler-Nichols, rechazo a perturbaciones de carga (apertura de puertas del horno), índices de desempeño de calidad (\(C_p\), \(C_{pk}\)), eficiencia energética y análisis de fatiga/desgaste en actuadores.
* **Características:** Comparativa directa entre control PI y PID, histogramas de distribución de temperatura y monitorización de tolerancia industrial estricta (\(\pm \text{tol}\)).

---

## 🚀 Tecnologías y Características Técnicas

* **Núcleo de Simulación:** Algoritmos numéricos implementados en **JavaScript nativo** (métodos de Runge-Kutta y aproximación en tiempo discreto de alta frecuencia).
* **Renderizado Gráfico:** HTML5 Canvas optimizado con soporte para temas claros y oscuros automáticos.
* **Representación Matemática:** Ecuaciones renderizadas de forma profesional mediante **MathJax**.
* **Diseño UI/UX:** Estructura modular tipo *bento grid*, diseñada para visualizar simulaciones, ecuaciones, diagramas y controles en una sola pantalla sin necesidad de desplazamiento vertical excesivo.

---

## 📂 Estructura del Repositorio

```text
├── index.html                  # Diseño de controladores derivativos (Robot Autobalanceado)
├── servomotor-control-pd.html  # Posicionamiento de un servomotor de CD
├── horno-industrial-pid.html   # Control de temperatura en un horno industrial
└── README.md                   # Documentación principal del proyecto
