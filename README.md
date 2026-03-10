# EXTRAS**COL** — Calculadora de Horas Extras 🇨🇴

> Herramienta web personal para liquidar horas extras y recargos laborales bajo la legislación colombiana vigente (Código Sustantivo del Trabajo).

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Sin dependencias](https://img.shields.io/badge/dependencias-ninguna-brightgreen?style=flat-square)
![Uso personal](https://img.shields.io/badge/uso-personal-gold?style=flat-square)
![Colombia 2025](https://img.shields.io/badge/Colombia-SMMLV%202025-yellow?style=flat-square)

---

## 📋 Tabla de contenido

- [¿Qué es?](#-qué-es)
- [Características](#-características)
- [Tipos de hora soportados](#-tipos-de-hora-soportados)
- [Marco legal](#-marco-legal)
- [Cómo usar](#-cómo-usar)
- [Fórmula de cálculo](#-fórmula-de-cálculo)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Stack tecnológico](#-stack-tecnológico)
- [Cómo ejecutar](#-cómo-ejecutar)
- [Constantes legales 2025](#-constantes-legales-2025)
- [Advertencias y límites legales](#-advertencias-y-límites-legales)
- [Consideraciones importantes](#-consideraciones-importantes)
- [Autor](#-autor)

---

## ¿Qué es?

**EXTRASCOL** es una calculadora web de uso personal, sin servidor ni base de datos, que permite liquidar de forma rápida y precisa el valor de horas extras y recargos laborales en Colombia, siguiendo las tarifas del **Código Sustantivo del Trabajo (CST)** y la normativa vigente para el año 2025.

Fue diseñada con un enfoque minimalista y funcional para uso cotidiano: solo hay que abrir el archivo `index.html` en cualquier navegador moderno.

---

## ✨ Características

| Funcionalidad | Descripción |
|---|---|
| 💰 **Salario base configurable** | Ingresa cualquier salario en COP; muestra automáticamente el equivalente en SMMLV y el valor de la hora ordinaria |
| 📅 **Período de liquidación** | Mensual (240 h), quincenal (120 h) o semanal (48 h) |
| ➕ **Filas dinámicas** | Agrega o elimina tantos tipos de hora como necesites en una misma liquidación |
| 🧮 **Cálculo automático** | Valor exacto por tipo de hora, con recargo aplicado y subtotal por fila |
| ⚠️ **Validación de límites legales** | Alerta si las horas extras superan el máximo legal (12 h/semana — Art. 165 CST) |
| 📊 **Panel de resultados detallado** | Desglose por cada tipo de hora + total a pagar en una sola vista |
| 🚌 **Subsidio de transporte** | Informa automáticamente si el trabajador tiene derecho al auxilio de transporte (≤ 2 SMMLV) |
| 🔴 **Alerta salario mínimo** | Avisa si el salario ingresado es inferior al SMMLV 2025 (ilegal según Art. 145 CST) |
| 📜 **Tabla de recargos** | Referencia rápida de todos los porcentajes legales vigentes |
| ⚖️ **Marco legal integrado** | Sección con los artículos del CST aplicables al cálculo |
| 🎨 **Diseño dark premium** | Interfaz oscura con tipografía monospace, sin distracciones |
| 📱 **Responsive** | Funciona en escritorio y dispositivos móviles |

---

## 📊 Tipos de hora soportados

| Código | Tipo | Horario | Recargo |
|--------|------|---------|---------|
| `ed` | Extra diurna | Lunes–Sábado · 06:00–21:00 | **+25%** |
| `en` | Extra nocturna | Lunes–Sábado · 21:00–06:00 | **+75%** |
| `edf` | Extra Dom/Fest. diurna | Domingos y festivos · 06:00–21:00 | **+100%** |
| `enf` | Extra Dom/Fest. nocturna | Domingos y festivos · 21:00–06:00 | **+150%** |
| `rn` | Recargo nocturno | Hora ordinaria nocturna (no es extra) | **+35%** |
| `rdf` | Recargo dominical/festivo | Trabajo ordinario en domingo o festivo | **+75%** |

> **Nota:** Los tipos `rn` y `rdf` son **recargos sobre hora ordinaria**, no horas extras propiamente dichas. No cuentan para el límite semanal de 12 horas extras.

---

## ⚖️ Marco legal

La calculadora implementa las siguientes normas laborales colombianas:

| Norma | Contenido aplicado |
|-------|--------------------|
| **Art. 145 CST** | Salario mínimo legal vigente — ningún salario puede ser inferior |
| **Art. 159 CST** | Definición de trabajo suplementario o de horas extras |
| **Art. 161 CST** | Jornada máxima: 8 h/día · 46 h/semana desde 2026 (proceso gradual, Ley 2101/2021) |
| **Art. 165 CST** | Límite de horas extras: máx. **2 h/día** y **12 h/semana** |
| **Art. 168 CST** | Tasas y fórmula de liquidación de recargos (base: salario ordinario) |
| **Art. 179 CST** | Trabajo dominical y festivo obligatorio genera recargo del 75% adicional |
| **Decreto 1174/2020** | SMMLV 2025: $1.423.500 COP · Auxilio de transporte: $200.000 COP |

---

## 🚀 Cómo usar

1. **Abre** el archivo `index.html` directamente en tu navegador (no requiere servidor).
2. **Ingresa el salario mensual** en pesos colombianos (COP).  
   - Verás en tiempo real cuántos SMMLV representa y el valor de la hora ordinaria.
3. **Selecciona el período** de liquidación: mensual, quincenal o semanal.
4. **Agrega las horas** haciendo clic en **"+ Agregar tipo de hora"**:
   - Escribe la cantidad de horas en el campo numérico.
   - Selecciona el tipo correspondiente en el desplegable.
   - Repite para cada tipo de hora diferente que debas liquidar.
5. Haz clic en **"Calcular liquidación"**.
6. El panel derecho mostrará:
   - Valor hora ordinaria
   - Subtotal por cada tipo de hora con el recargo aplicado
   - **Total a pagar** en COP
   - Alertas de subsidio de transporte o salario mínimo si aplican

---

## 🧮 Fórmula de cálculo

```
Valor hora ordinaria = Salario / Horas del período

Valor hora tipo X    = Valor hora ordinaria × (1 + % recargo)

Subtotal tipo X      = Valor hora tipo X × Cantidad de horas

Total a pagar        = Σ Subtotales de todos los tipos
```

**Ejemplo:** Salario $2.000.000, período mensual (240 h), 4 horas extra diurnas:

```
Valor hora ordinaria = 2.000.000 / 240 = $8.333,33
Valor hora extra diurna = 8.333,33 × 1,25 = $10.416,67
Subtotal = 10.416,67 × 4 = $41.666,67
```

---

## 📁 Estructura del proyecto

```
CalculadoraHorasExtras/
│
├── index.html      ← Aplicación completa (HTML + lógica JS embebida)
├── styles.css      ← Estilos visuales (tema dark, layout responsive)
└── README.md       ← Este archivo
```

> La aplicación es intencionalmente un **single-file app**: toda la lógica de negocio vive en `index.html` junto al marcado, lo que la hace portátil y fácil de compartir o respaldar.

---

## 🛠 Stack tecnológico

| Tecnología | Uso |
|---|---|
| **HTML5** | Estructura y marcado semántico |
| **CSS3** (custom properties, grid, flexbox) | Layout responsive y tema visual |
| **JavaScript ES6** (vanilla, sin frameworks) | Lógica de cálculo, DOM dinámico y validaciones |
| **Google Fonts** · Syne + DM Mono | Tipografía del interfaz |

No requiere `npm`, `node_modules`, bundlers ni ninguna dependencia externa más allá de una conexión a Google Fonts para las tipografías (o funcionará con la fuente de sistema como fallback sin conexión).

---

## ▶️ Cómo ejecutar

### Opción 1 — Abrir directo (más fácil)

Haz doble clic sobre `index.html` o ábrelo desde el explorador de archivos.

### Opción 2 — Servidor local con VS Code

Con la extensión **Live Server** instalada:

```
Clic derecho sobre index.html → "Open with Live Server"
```

### Opción 3 — Servidor local con Python

```bash
# Python 3
python -m http.server 8080

# Luego abre: http://localhost:8080
```

### Opción 4 — Servidor local con Node.js

```bash
npx serve .
```

---

## 📌 Constantes legales 2025

Estas constantes están definidas en el script de `index.html` y son las que rigen los cálculos:

```javascript
const SMMLV             = 1_423_500;   // Salario Mínimo Mensual Legal Vigente
const AUX_TRANSPORTE    = 200_000;     // Auxilio de transporte mensual
const HORAS_MES         = 240;         // Horas laborales en un mes (periodo mensual)
const HORAS_SEMANA      = 48;          // Jornada semanal 2025 (transición Ley 2101/2021)
const MAX_EXTRAS_SEMANA = 12;          // Máximo de horas extras por semana (Art. 165 CST)
const MAX_EXTRAS_DIA    = 2;           // Máximo de horas extras por día (Art. 165 CST)
```

> Para actualizar los valores al inicio de un nuevo año laboral, modifica únicamente estas constantes en el bloque `<script>` de `index.html`.

---

## 🔔 Advertencias y límites legales

La calculadora muestra las siguientes alertas automáticas:

| Situación | Mensaje | Color |
|-----------|---------|-------|
| Horas extras > 12 h/semana | "Las horas ingresadas superan el límite legal semanal..." | 🟡 Amarillo |
| Salario < SMMLV | "El salario ingresado es inferior al SMMLV 2025..." | 🔴 Rojo |
| Salario ≤ 2 × SMMLV | "Si el salario es ≤ 2 SMMLV, tiene derecho al auxilio de transporte..." | 🟢 Verde |

---

## ⚠️ Consideraciones importantes

- **Esta herramienta es de uso personal e informativo.** Los resultados son orientativos y no reemplazan la asesoría de un contador o abogado laboralista.
- El cálculo se realiza sobre el **salario ordinario**, sin incluir el auxilio de transporte como base de liquidación (conforme al CST).
- La jornada semanal máxima está en transición gradual: 48 h (2023–2025) → 47 h (2026) → 46 h (2027) → 44 h (2028 en adelante), según la **Ley 2101 de 2021**.
- Los festivos en Colombia son los establecidos por la **Ley 51 de 1983** y sus modificaciones.
- Para superar el límite legal de horas extras (12 h/semana), el empleador debe obtener autorización previa del **Ministerio del Trabajo**.

---

## 👤 Autor

**Andrés Galvis**  
Desarrollo personal · Colombia · 2025  

---

*Desarrollado con HTML, CSS y JavaScript puro — sin frameworks, sin complicaciones.*
