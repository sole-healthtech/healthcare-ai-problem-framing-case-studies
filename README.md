# Case Studies in Problem Framing for Healthcare AI

## Overview
This repository contains a set of abstracted case studies examining problem framing in healthcare AI. The focus is not on model performance or implementation details, but on whether a problem is appropriate to model in the first place, given clinical workflows, authority boundaries, and potential risk.

These case studies are intended to surface recurring patterns where technically feasible AI systems fail due to misalignment with clinical reality, accountability, or logistics. The goal is to support safer, more effective use of AI as a tool—rather than an autonomous decision-maker—in healthcare settings.

---

## Scope and Intent
These case studies are illustrative rather than exhaustive. They are intentionally abstracted and do not reference specific organizations or products. This is deliberate: the intent is to analyze recurring design and framing patterns, not to critique individual implementations.

---

## Note on Clinical Context
Healthcare AI systems ultimately operate within clinical environments shaped by time pressure, legal accountability, professional judgment, and patient trust. These case studies assume that successful AI tools must fit within existing clinical workflows and respect the realities of bedside decision-making, rather than require clinicians to adapt to the tool.

In practice, misalignment at this level often determines whether a tool is adopted, ignored, or quietly worked around.

---

## Case Study: AI-Enhanced Surgical Navigation in ENT Procedures (Abstracted)

### 1. What was being attempted
An AI-enhanced surgical navigation system was updated to use machine learning to assist ENT surgeons during sinus procedures by identifying anatomical segments and helping guide instrument positioning or path selection in real time.

### 2. Why it seems reasonable at first
Endoscopic sinus procedures occur in high-stakes anatomy with tight margins for error. Navigation assistance can plausibly reduce cognitive load, support precision, and improve consistency—especially under time pressure or variable visualization.

Adding AI is marketed as an upgrade that could improve guidance and safety in complex cases.

### 3. Why the model is unsafe or mis-scoped
In surgery, decision-making authority ultimately rests with the surgeon. Their license, reputation, and legal responsibility are on the line for every intraoperative decision. Introducing AI-based navigation into this context creates a fundamental mismatch between influence and accountability.

If an AI system provides guidance that is incorrect or misleading, responsibility does not transfer to the model or the manufacturer in real time. Accountability defaults to the surgeon as the clinician in charge of the procedure.

Surgeons also develop highly individualized techniques and preferences shaped by experience, anatomical variation, and real-time judgment. A system that implicitly encourages trust in algorithmic guidance risks displacing clinical intuition—especially when marketed as advanced or novel. In such settings, a surgeon may defer to the tool rather than their own assessment, even when uncertainty exists.

The critical framing failure is not whether the model is accurate on average, but whether *any* error rate is acceptable when downstream consequences are irreversible and the burden of liability remains entirely human.

### 4. Worst-case scenario if wrong
A procedure that is otherwise routine results in catastrophic injury—such as vascular damage, stroke, permanent neurologic deficit, or death—due to misplaced reliance on AI-guided navigation.

In these scenarios, responsibility becomes diffuse after the fact, but immediate accountability is clear: the surgeon faces litigation, professional review, and reputational harm. Questions of shared liability between the hospital, device manufacturer, and AI developer may be argued later, but they do not mitigate the real-time risk carried by the clinician at the point of care.

This asymmetry between who influences the decision and who bears the consequences is a central safety concern.

### 5. How this would realistically enter clinical workflow
AI-enhanced navigation systems enter the operating room as embedded, real-time guidance—not optional background information. Surgeons encounter these signals under time pressure, with limited ability to pause, interrogate model behavior, or independently verify outputs.

Unlike documentation or planning tools, intraoperative systems operate within a closed-loop environment where:
- decisions are immediate,
- errors propagate instantly, and
- correction may not be possible once harm occurs.

In high-stakes surgical contexts, the question is not whether the tool can be integrated into workflow, but whether it *should* be. When tolerance for error is near zero, adding another decision influence—especially one that cannot be held accountable—may increase risk rather than reduce it.

### 6. What could have been modeled instead (safer scope)
If AI is used in surgical domains, a safer framing keeps it outside the operative control loop and within clear scope-of-practice boundaries.

Examples include:
- **Pre-operative support**, such as structured chart review assistance that surfaces relevant patient history, imaging, prior complications, or anatomical considerations for the surgeon to review at their discretion.
- **Planning augmentation**, where AI highlights potential anatomical landmarks or variations in advance, without providing real-time directional guidance during surgery.
- **Information organization**, reducing cognitive burden before the procedure rather than influencing instrument placement during it.

The key distinction is that these uses support preparation and situational awareness without competing with intraoperative judgment.

**Closing line:**  
This case illustrates how introducing AI into high-risk clinical environments without aligned authority and liability can undermine, rather than support, safe decision-making.

---

## Case Study: General-Purpose AI Chatbots Used for Health Advice (Abstracted)

### 1. What was being attempted
Large language model–based chatbots, developed as general-purpose conversational systems, are being used by members of the public to interpret medical symptoms and recommend next steps (e.g., self-care, seeing a GP, or seeking emergency care), despite not being licensed medical tools.

### 2. Why it seems reasonable at first
These systems perform well on standardized tests of medical knowledge and generate fluent, confident responses resembling clinical explanations. They are easily accessible, available at all hours, and perceived as a low-barrier alternative to searching the internet or waiting to see a clinician.

### 3. Why the model is unsafe or mis-scoped
Patient self-assessment is inherently unreliable. Individuals may omit diagnoses, downplay symptoms, or lack full understanding of their own medical history and comorbidities. Many patients reasonably rely on clinicians to interpret their health information rather than maintaining clinically precise self-knowledge.

General-purpose AI chatbots rely entirely on user-provided input, without access to longitudinal medical records, problem lists, medication histories, allergies, or prior adverse events. As a result, they cannot detect missing or contraindicating information that would materially alter clinical interpretation.

Even when a chatbot suggests a plausible intervention, it lacks authority to order tests, prescribe medications, or ensure appropriate follow-up. Clinical decision-making is not only about identifying an intervention, but about verifying appropriateness, monitoring response, and adjusting course if the patient deteriorates.

The framing failure lies in treating symptom interpretation as a standalone task, rather than as part of a continuous clinical feedback loop.

### 4. Worst-case scenario if wrong
A patient experiencing a serious or time-sensitive condition receives reassurance or low-urgency advice and delays seeking care. The patient may believe they are improving because they “did something,” even as their condition worsens.

Because AI systems do not hold a clinical license and cannot be held professionally accountable, harm falls entirely on the patient and downstream clinicians. Clinical data—when available at all—represent only a snapshot in time. Without structured follow-up or escalation, deterioration may go unnoticed.

### 5. How this would realistically enter clinical workflow
These systems do not integrate into formal clinical workflows. Instead, they influence patient behavior before clinical contact occurs.

Healthcare workers already manage the consequences of misinformation from online searches. AI-generated health advice risks amplifying this dynamic by presenting information with greater fluency and perceived authority.

Clinicians must then:
- correct misunderstandings,
- re-establish clinical authority, and
- manage delayed or worsened presentations,

often under time pressure.

### 6. What could have been modeled instead (safer scope)
A safer framing avoids symptom triage or action recommendations and instead supports access to appropriate care.

Examples include:
- Reinforcing patient self-awareness without interpretation.
- Helping patients organize questions or concerns for clinical visits.
- Defaulting consistently to professional evaluation when serious harm is plausible.

The shift is from *telling patients what to do* to *supporting timely clinical evaluation without substituting judgment*.

**Closing line:**  
This case illustrates how tools that bypass clinical authority and follow-up can increase risk, even when they appear informative or well-intentioned.

---

## Case Study: EHR-Embedded Sepsis Prediction Model (Abstracted)

### 1. What was being attempted
A machine-learning model was embedded within an electronic health record to identify hospitalized patients at risk of developing sepsis, with the goal of enabling earlier recognition and intervention.

### 2. Why it seems reasonable at first
Sepsis is a leading cause of morbidity and mortality, and earlier recognition is associated with improved outcomes. Hospitals face pressure to identify sepsis sooner, and EHR systems aggregate large volumes of clinical data.

At a surface level, synthesizing these signals into an early warning system appears logical.

### 3. Why the model is unsafe or mis-scoped
Sepsis is an acute, rapidly evolving syndrome. False negatives carry especially high risk, as delayed recognition may result in irreversible harm or death.

Any assessment must be interpreted within full clinical context, including diagnoses, medications, recent changes, and bedside assessment—elements that belong to clinical judgment and cannot be safely abstracted into a standalone prediction.

Predictive alerts also increase alert fatigue. When alerts lack transparency or clear actionability, clinicians may over-rely on or systematically ignore them.

Uncertainty around how subjective complaints are represented, how inconsistently documented symptoms are weighted, and how missing data affects output further undermines trust.

The framing failure lies in treating sepsis as a prediction problem, rather than as a dynamic clinical assessment process requiring continuous interpretation and reassessment.

### 4. Worst-case scenario if wrong
A patient developing sepsis is not flagged, leading to delayed intervention and deterioration. Repeated false alarms desensitize staff, reducing responsiveness overall.

Repeated failures erode clinician trust not only in the tool, but in future AI systems more broadly—an institutional and cultural harm beyond individual patients.

### 5. How this would realistically enter clinical workflow
The model surfaces as alerts during routine work:
- alerts compete with many others,
- outputs lack transparency, and
- the model does not clearly replace an existing task.

This creates additive cognitive burden rather than meaningful support.

### 6. What could have been modeled instead (safer scope)
A safer framing supports trend-based awareness rather than prediction.

Examples include:
- Highlighting trends in vitals or labs over time.
- Surfacing deviations without diagnostic labeling.
- Allowing clinicians to flag patients as “high concern for infection” to support continuity across shifts.

The shift is from *predicting sepsis* to *supporting vigilance, communication, and reassessment*.

**Closing line:**  
This case illustrates how collapsing complex, time-sensitive clinical reasoning into predictive alerts can increase risk when purpose, authority, and workflow are not clearly aligned.

---

## Summary
Effective healthcare AI systems must earn the trust of healthcare workers through clearly defined scope, boundaries, and purpose. AI is a tool to support clinical judgment—not a replacement for it—and it cannot assume clinical authority or accountability.

The most successful applications reduce redundant or unnecessary work and support patient-centered care. Tools that increase workload, obscure responsibility, or conflict with clinical reasoning are likely to be ignored or worked around in practice.

Safe and durable healthcare AI requires an iterative design process with continuous feedback from domain experts who understand clinical workflows, risk, and accountability. Without this translation layer between technical teams and clinical reality, even well-intentioned systems are likely to fail at deployment rather than in development.
