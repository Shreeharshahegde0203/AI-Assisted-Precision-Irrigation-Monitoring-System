
# AI-Assisted Precision Irrigation Monitoring System 🌱💧

## 📌 Overview

This project implements an **AI-Assisted Precision Irrigation Monitoring System** using a **multi-agent architecture** built with **LangFlow** and the **IBM Granite model**.
The system analyzes soil and weather conditions to identify irrigation stress patterns and provides **assistive, non-automated irrigation insights** to promote water-efficient and sustainable farming practices.

The system is **advisory only** and does **not** automate irrigation, prescribe water quantities, or provide chemical, fertilizer, pest, or disease recommendations.

---

## 🎯 Problem Statement

Inefficient irrigation practices often lead to water wastage, crop stress, and reduced agricultural productivity. Farmers lack continuous insights into soil moisture dynamics and crop water requirements, making it difficult to adapt irrigation decisions to changing weather and soil conditions.

This project addresses the need for an **intelligent assistive system** that:

* Analyzes irrigation-related data
* Detects under- and over-irrigation risks
* Provides water-efficiency and scheduling awareness
* Supports sustainable irrigation practices

---

## 🧠 System Architecture

The system follows a **three-agent pipeline**, where each agent has a clearly defined role.

```
User Input (Soil & Weather Data)
        ↓
Soil & Weather Data Analysis Agent
        ↓
Water Stress Detection Agent
        ↓
Irrigation Advisory Assistant (RAG-based)
        ↓
Assistive Irrigation Insights
```

---

## 🤖 Agents Description

### 1️⃣ Soil & Weather Data Analysis Agent

**Purpose:**

* Analyzes soil moisture, rainfall, temperature, evapotranspiration, crop type, growth stage, and season.
* Converts raw environmental data into irrigation-relevant summaries.

**Key Constraints:**

* No recommendations or actions
* No pests, diseases, fertilizers, or chemicals

---

### 2️⃣ Water Stress Detection Agent

**Purpose:**

* Identifies irrigation stress patterns.
* Classifies stress as **Low, Medium, or High**.
* Detects under-irrigation or over-irrigation risks using seasonal and crop-stage baselines.

**Key Constraints:**

* No irrigation commands or quantities
* No automation or chemical guidance

---

### 3️⃣ Irrigation Advisory Assistant (RAG-based)

**Purpose:**

* Provides **high-level irrigation awareness and water-efficiency insights**.
* Uses **Retrieval-Augmented Generation (RAG)** with sustainable irrigation guidelines.

**Key Constraints:**

* Assistive only
* Non-automated
* No prescriptions, chemicals, fertilizers, pests, or diseases

---

## 📚 Retrieval-Augmented Generation (RAG)

The advisory agent uses **external irrigation and sustainable water-management knowledge** through a Mock Data source in LangFlow.

RAG ensures:

* Grounded and reliable responses
* Reduced hallucinations
* Alignment with sustainability principles

---

## 🛠️ Technology Stack

* **LangFlow** – Visual AI workflow and agent orchestration
* **IBM Granite Model (watsonx.ai)** – Large Language Model
* **RAG (Retrieval-Augmented Generation)** – Knowledge-grounded advisory system
* **JSON Flow Export** – Project configuration and reproducibility

---

## 🧪 Sample Input

```
Soil Moisture: Low (18%)
Rainfall: None in last 7 days
Temperature: High (32°C)
Evapotranspiration: High
Crop: Maize
Growth Stage: Flowering
Season: Summer
```

---

## 📤 Sample Output

```
Soil & Weather Summary:
Low soil moisture combined with high temperature and evapotranspiration
indicates increased moisture loss.

Water Stress Assessment:
Stress Level: High
Reason: Insufficient soil moisture during a critical growth stage.

Irrigation Advisory:
Monitoring soil moisture trends can support timely irrigation planning.
High evaporative demand suggests increased attention to water-use efficiency.
Sustainable irrigation practices help reduce water stress.
```

---

## 🚦 System Constraints & Safety

* ❌ No automated irrigation control
* ❌ No exact water quantity prescriptions
* ❌ No fertilizer, pesticide, or chemical recommendations
* ❌ No pest or disease diagnosis
* ✅ Assistive, explainable, and sustainability-focused

---

## 📁 Repository Contents

```
├── langflow_project.json   # Exported LangFlow flow configuration
├── README.md               # Project documentation
```

---

## ▶️ How to Use

1. Import the `langflow_project.json` file into LangFlow.
2. Ensure IBM watsonx (Granite model) credentials are configured.
3. Connect the language model to all three agents.
4. Provide soil and weather inputs via the chat interface.
5. Observe irrigation analysis, stress detection, and advisory outputs.

---

## 🌍 Outcome & Impact

* Promotes efficient water use
* Reduces irrigation-related resource wastage
* Supports sustainable and climate-resilient farming
* Improves irrigation awareness without automation risk





