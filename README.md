# 🛡️ LiverGuard

## Clinical Drug Safety Assessment for Hepatic Patients

LiverGuard is an AI-powered clinical decision support system that helps assess medication safety for patients with hepatic impairment.

The system analyzes a drug, identifies its active ingredient, retrieves medical evidence from trusted sources, evaluates the risk, and provides a simple clinical summary.

> **Important:** LiverGuard is a clinical decision support tool and is not a replacement for professional medical advice.

---

## 🎯 Project Goal

The main goal of LiverGuard is to make drug safety assessment easier for patients with liver problems by bringing important drug information together in one system.

Instead of checking multiple sources manually, the system collects the relevant information and presents it in a clear way.

---

## 🔄 How It Works

The system follows these main steps:

**1. Enter Drug Name**
The user enters a drug name or active ingredient.

**2. Identify Active Ingredient**
The system identifies the active ingredient using local drug mapping or RxNav.

**3. Retrieve Medical Evidence**
The system collects information from:

* FDA / openFDA
* LiverTox

**4. Risk Assessment**
Clinical guardrails evaluate the drug and classify the risk as:

* Safe
* Caution
* Contraindicated

**5. AI Clinical Summary**
The AI summarizes the retrieved information using only the available evidence.

**6. Evidence Panel**
The system displays the decision, warnings, risk level, and supporting evidence.

---

## 🧠 AI Safety

LiverGuard does not allow the AI to freely generate medical information.

The AI receives the evidence collected by the system and uses it to generate the clinical summary.

If information is missing, the system does not guess.

### Key Principle

> **The AI explains the evidence. It does not invent the evidence.**

---

## 🛡️ Safety Features

LiverGuard includes several safety mechanisms:

* Evidence-based responses
* Clinical risk classification
* FDA and LiverTox evidence
* Safe refusal when reliable information is unavailable
* Dose adjustment warnings when applicable
* Physician approval warnings
* Fallback response if the AI service fails
* Clinical disclaimer

---

## 🏗️ System Components

The project is organized into several main components:

* `app.py` → Streamlit user interface
* `retriever.py` → Retrieves and combines drug information
* `rxnav_api.py` → Resolves drug names to active ingredients
* `fda_api.py` → Retrieves FDA drug information
* `guardrails.py` → Handles safety rules and risk assessment
* `llm_generator.py` → Generates the evidence-grounded clinical summary
* `main.py` → Runs the complete LiverGuard pipeline

---

## 🛠️ Technologies Used

* Python
* Streamlit
* OpenAI API
* FDA openFDA
* RxNav API
* LiverTox
* JSON
* Clinical Guardrails
* Evidence-Grounded LLM

---

## 📊 Output

The system provides:

* Drug Name
* Active Ingredient
* Risk Level
* Safety Verdict
* Clinical Decision
* Required Action
* Confidence Level
* FDA Warnings
* Hepatic Guidance
* LiverTox Information
* Supporting Evidence

---

## ⚕️ Disclaimer

LiverGuard is designed as a clinical decision support tool.

It does not replace a qualified healthcare professional.

All clinical decisions should be verified by a healthcare professional before use.

---

## 👥 Project

**LiverGuard Team**

AI-powered Clinical Drug Safety Assessment System
