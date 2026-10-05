# 📚 Lesson 1.1: The Data Landscape

## Session Overview

| | |
|---|---|
| **Duration** | 3 hours |
| **Format** | Flipped Classroom + Discussion |
| **Tools** | Google Colab (for code demo) |
| **Prerequisite** | Complete the [Pre-Class Reading](./pre-class.md) — The Data Science Hierarchy of Needs |

## Agenda

| Time | Part | Topic |
|------|------|-------|
| 0:00 – 1:00 | Part 1 | The Hierarchy of Insights — Analytics vs. Data Science vs. AI |
| 1:00 – 2:00 | Part 2 | The Data Highway — Pipelines & Data Structures |
| 2:00 – 3:00 | Part 3 | The Conscious Algorithm — Ethics & Bias |

---

## 🏃 Part 1: The Hierarchy of Insights (60 min)

### 🎯 Learning Objective
Explain the difference between Data Analytics, Data Science, and Artificial Intelligence.

### Concept Overview (10 min)

**Analogy:** Imagine a kitchen.
- **Data Analytics** is checking the fridge to see what's left and writing a report on what was eaten (Historical).
- **Data Science** is using that list to predict what ingredients you'll need for next week's dinner (Predictive).
- **AI** is a robot chef that sees the fridge is empty and decides on its own to order groceries — no recipe told it to (Autonomous Decision & Action).

> **Note:** "Automated" isn't the same as "AI." A thermostat or a scheduled script is automated but not AI — it just executes a fixed rule someone wrote. What makes the robot chef AI is that it acts on a *learned or inferred* judgment call, autonomously, without a human approving that specific decision.

### 🛠️ Workshop: "The Company Diagnostic" (40 min)

> **Studying alone?** Work through these questions individually — write your answers down before opening the suggested responses. There are no single right answers; the goal is to practise reasoning through the hierarchy.

**Discussion:**

- "If a CEO says 'I want to build a GPT-4 for my company' but all their data is in paper files, where on the hierarchy are they failing?"
- "If we scanned those papers into PDFs, would that be enough to build an AI tomorrow? Or is there still a 'Cleaning' and 'Analysis' step missing?"

**Activity:**

1. **The Matrix:** Classify each of the following 5 scenarios as Data Analytics, Data Science, or AI — and explain your reasoning:

```
   - A bank system that automatically freezes a card and alerts the customer 
   the instant it detects an unusual transaction, with no analyst reviewing it first
   AI. Does not require an analysts' decision to 
   - A manager building a monthly pivot table of sales figures
   Data Analytics. Pivot table analyses the past
   - A self-driving car that brakes automatically when it detects an obstacle
   AI. Car decides to brake without human intervention
   - A model that predicts which customers are likely to churn next quarter
   Data Science. It is a predictive model, but someone still has to decide what to do with the customers.
   - A dashboard showing last year's revenue broken down by region
   Data Analytics. It is analysing what happened last year
```


<details>
<summary>Answer Key — The Matrix</summary>

| Scenario | Category | Reasoning |
|---|---|---|
| Bank system auto-freezes card on unusual transactions | **AI** | The system doesn't just predict "this looks unusual" — it *acts* on that judgment in real time (freezing the card) with no analyst approving the decision first. Compare this to a system that only flags a transaction for a fraud analyst to review later: that would be Data Science, since a human still decides and acts. The action-without-human-review is what tips this into AI. |
| Manager builds a monthly pivot table | **Data Analytics** | Purely historical and descriptive — it answers "what happened?" using existing data. No prediction, no automation. |
| Self-driving car brakes automatically | **AI** | The car perceives its environment and takes autonomous action with no human in the loop. This is AI at its most literal. |
| Model predicts which customers will churn | **Data Science** | It builds a predictive model from historical patterns to forecast a future outcome. A human still reviews and acts on the results. |
| Dashboard of last year's revenue by region | **Data Analytics** | Historical, descriptive reporting. It visualises what already happened — no model, no prediction. |

**Key distinctions to remember:**
- Analytics = *what happened* (past, human interprets)
- Data Science = *what will happen* (future, model predicts, human decides)
- AI = *do something about it* (autonomous action, no human needed per decision)

</details>

### 💬 Q&A & Reflection (10 min)

- Does AI replace Data Science — or depend on it?

```
AI can replace some parts of data science (e.g. writing code, explaining error statements, developing new models). However, AI was likely developed using predictive models developed by data scientists, and data science as a field is still needed to maintain, support, develop and improve AI models.
```

<details>
<summary>Suggested answer</summary>

AI **depends** on Data Science — it doesn't replace it. You need clean, well-understood data (Data Science work) before you can train a reliable AI model. Think of the hierarchy: Data Science sits below AI in the pyramid. If the data going into an AI model is biased, incomplete, or poorly understood, the AI will amplify those problems. In practice, most AI teams have far more Data Scientists and Data Engineers than they have "AI researchers" — the foundation work is the majority of the effort.

</details>

- How does Netflix use Analytics, Data Science, and AI differently in its product?

```
Netflix uses data analytics to tell users how many hours they have spent watching Netflix, across what shows and genres etc.
Data science is used to forecast / predict what shows users are likely to watch based on their watch history.
AI would be used to push the predicted / forecasted shows to your Netflix feed and to populate the Recommended shows.
```

<details>
<summary>Suggested answer</summary>

- **Analytics:** Netflix tracks which shows have the highest completion rates, which thumbnails get the most clicks, and what time of day users are most active. These are historical reports that guide business decisions.
- **Data Science:** Netflix builds recommendation models that predict which shows a specific user will want to watch next, based on their history and the behaviour of similar users.
- **AI:** Netflix uses AI to automatically select and personalise the thumbnail image shown to each user for the same show — different users see different artwork, chosen autonomously without a human deciding for each case.

</details>

---

## 🏃 Part 2: The Data Highway (60 min)

### 🎯 Learning Objective
Identify the 4 stages of a Data Pipeline and distinguish between Structured, Unstructured, and Semi-Structured data.

### Concept Overview (10 min)

**The Pipeline:** Collection ➔ Cleaning ➔ Analysis ➔ Visualisation

**Data Structure Analogy:**
- **Structured:** Think of an Egg Carton — every slot is identical, fixed-size, and pre-defined. You know exactly where an egg goes and nothing else fits there.
- **Semi-Structured:** Think of a Bento Box — it has compartments, so there's real organisation, but the compartments vary in size and count from box to box, and you can put anything in each one. No two bento boxes are laid out identically — just like two JSON documents can use different keys.
- **Unstructured:** Think of a Grocery Bag — everything's jumbled together with zero compartments. You have to sort it all yourself before you can use anything.

![Structured, Semi-Structured & Unstructured Data Classification](assets/structured_semi_unstructured_data_classification.svg)

A quick heads-up on one term: **JSON**. It's simply a way of writing down data with labels attached, like a sticky note that says `heart rate: 80, time: 12:00`. Computers love it because the labels say what each value means. It's more organised than a paragraph of text, but looser than a spreadsheet — which is why we call it "semi-structured."

### 🛠️ Activity 1: "The Smart Watch Data Pipeline" (20 min)

**Scenario:** You are designing the data flow for a "Sleep Tracker" app.

**Task:** Fill in the blanks below. If studying alone, write your own answers first, then check the sample responses below the table.

| Pipeline Stage | What happens here? (Specific to a Smart Watch) |
|:---|:---|
| **1. Collection** | The smart watch sensor reads user's heart rate, skin temperature, movement every 5 seconds *Example: Heart rate sensor records BPM every 5 seconds...* |
| **2. Cleaning** | The smart watch detects when there is a gap in heart rate data (e.g. more than 5 minutes) and removes it *(What if the user takes the watch off? What if the battery dies mid-night?)* |
| **3. Analysis** | The smart watch combines heart rate variability, skin temperature and movement into a sleep score, e.g. if heart rate, skin temperature and amount of movement are high, low sleep score *(How do we turn raw heartbeats into a "Sleep Score"? What is the math?)* |
| **4. Visualisation** | The smart watch app shows the user their total sleep duration, amount of sleep in each stage (light, REM, deep), and a line graph of how long the user has slept in each stage. *(What does the user actually see on their phone screen?)* |

```
| **1. Collection** | The smart watch sensor reads user's heart rate, skin temperature, movement every 5 seconds |
| **2. Cleaning** | The smart watch detects when there is a gap in heart rate data (e.g. more than 5 minutes) and removes excessively high or low heart rate |
| **3. Analysis** | The smart watch weights heart rate variability, skin temperature and movement, and combines it into a sleep score, e.g. if heart rate, skin temperature and amount of movement are high, low sleep score |
| **4. Visualisation** | The smart watch app shows the user total sleep duration, and amount of sleep in each stage (light, REM, deep) via a line graph|
```

<details>
<summary>Sample answers for Stages 2–4</summary>

| Pipeline Stage | Sample Answer |
|:---|:---|
| **2. Cleaning** | Detect and remove invalid readings: if BPM is 0 for more than 2 minutes, mark those intervals as "watch removed" and exclude them from the sleep score. Also handle sudden spikes (e.g. BPM of 200 mid-sleep) as sensor noise. |
| **3. Analysis** | Calculate average BPM per 30-minute window. Map BPM ranges to sleep stages: 40–55 BPM → Deep Sleep, 56–70 BPM → Light Sleep, 70+ BPM → Awake. A weighted formula then produces the "Sleep Score" (e.g. more Deep Sleep = higher score). |
| **4. Visualisation** | The phone app shows a colour-coded sleep timeline (dark blue = Deep Sleep, light blue = Light Sleep, grey = Awake), a single Sleep Score out of 100, and a summary of total hours slept. |

</details>

**Discussion Question:**

If the "Cleaning" stage fails (e.g., we count the time the watch was on the nightstand as "Deep Sleep"), how does that ruin the "Visualisation"?

The app would show the entire night as being in deep sleep, when this is not factually true.

<details>
<summary>Suggested answer</summary>

The app would show a falsely high Sleep Score and report more "Deep Sleep" than the user actually had. The visualisation looks clean and professional, but it's built on corrupted data. The user might think their sleep is fine when it isn't — or they might lose trust in the app entirely if they notice the numbers are wrong. This is the "Garbage In, Garbage Out" principle in action: no amount of good analysis or beautiful charts can compensate for bad data in Stage 2.

</details>

### 🛠️ Activity 2: "Data Binning" (20 min)

**Task 1:** Categorise each of the following hospital data items as Structured, Unstructured, or Semi-Structured:

```
1. Patient Name ("John Doe") - structured
2. X-Ray Image (chest_scan_001.jpg) - unstructured
3. Doctor's handwritten notes on a clipboard - unstructured
4. Patient Age (34) - structured
5. Blood Type (O+) - structured
6. Audio recording of a patient consultation - unstructured
7. JSON log from a heart monitor `{"bpm": 80, "time": "12:00"}` *(Tricky!)* - semi-structured
```

<details>
<summary>Answer Key — Data Binning</summary>

| Item | Category | Reasoning |
|---|---|---|
| Patient Name ("John Doe") | **Structured** | A defined text field in a table row — consistent format, queryable. |
| X-Ray Image (chest_scan_001.jpg) | **Unstructured** | A binary image file. There's no inherent schema — a database can store the filename, but the pixels themselves carry no structured meaning without analysis. |
| Doctor's handwritten notes | **Unstructured** | Free-form text with no consistent format, field names, or schema. Each doctor writes differently. |
| Patient Age (34) | **Structured** | A numeric value in a defined column — highly structured. |
| Blood Type (O+) | **Structured** | A categorical value from a fixed set (A, B, O, AB × +/−). Structured and easily queried. |
| Audio recording of a consultation | **Unstructured** | Raw audio has no schema. Like an image, you need additional processing (e.g. speech-to-text) to extract meaning. |
| JSON heart monitor log `{"bpm": 80, "time": "12:00"}` | **Semi-Structured** | This is the tricky one. JSON has keys and values (some organisation), but no rigid schema — different monitors might use different key names, nest data differently, or include optional fields. It's more structured than audio but less rigid than a database table. |

**The conversion question:** You can convert unstructured doctor's notes into structured data by extracting specific fields using NLP (Natural Language Processing). For example: scanning notes for medication names → populate a `medication` column; detecting phrases like "patient reports pain in..." → populate a `symptom` column. This is called **information extraction**.

</details>

**Question:** How can you convert Unstructured text (like a doctor's note) into Structured data? Give an example.
Using a template / table e.g. patient name, patient age, blood type, illness, diagnosis, medicine. Each field / column should be as structured as possible, e.g. converting diagnoses into categories.

### 💬 Q&A & Reflection (10 min)

- Is JSON structured or unstructured? Where does it sit on the spectrum?

JSON is semi-structured. It is structured because it has labels, but unstructured because each of the labels can point to different values/

<details>
<summary>Suggested answer</summary>

JSON is **semi-structured**. It has named keys and a predictable format within a single document, which gives it more organisation than raw text or audio. But unlike a database table, there's no enforced schema — two JSON files from different sources can use different key names, different nesting depths, or include entirely different fields. You can't simply import JSON into a spreadsheet the way you can a CSV. The machine can partially understand its structure, but humans still need to interpret and map the fields before it becomes truly structured.

</details>

- Why do Data Scientists reportedly spend ~80% of their time in the Cleaning stage?
Because in reality, a lot of data we receive is from non-data scientists, and it comes as unstructured data, or messy / unclean data.

<details>
<summary>Suggested answer</summary>

Real-world data is messy by default — it arrives from multiple systems with different formats, contains missing values, duplicates, typos, and outliers, and often wasn't collected with analysis in mind. Before any model or chart can be trusted, every one of these issues must be found and resolved. The 80% figure reflects how much hidden complexity exists in making data *usable*, compared to the relatively small amount of time spent running models or building visualisations once the data is clean.

</details>

---

## 🏃 Part 3: The Conscious Algorithm (60 min)

### 🎯 Learning Objective
Recognise potential sources of ethical bias in data collection and understand how "Clean Data" can still be "Biased Data".

### Concept Overview (10 min)

**Key Bias Types:**
- **Selection Bias:** The data you collected doesn't represent the whole world.
- **Historical Bias:** The data reflects past prejudices (e.g., hiring data from the 1970s).
- **Garbage In, Garbage Out:** Perfect code cannot fix broken data.

### 🛠️ Workshop: "The Hiring Bot Post-Mortem" (40 min)

**Scenario:**

You build an AI to screen resumes for a tech company. You train it on the company's "Top Performer" data from the last 10 years.

- **The Data:** 10 years of resumes from employees promoted to Manager.
- **The Result:** The AI starts rejecting all candidates from a nursing background and downgrades resumes containing the word "Women's College".

**Discussion:** *(If studying alone, write your answers before opening the suggested responses below.)*

```
1. Why did the AI do this? Was the AI sexist, or was the *data* sexist?
Because likely the employees promoted to managerial roles were mostly men, if we assume the company follows traditional patriarchal structure. It is selection and historical bias. AI was not sexist, it was the data.

2. Was this a "Data Collection" error or an "Analysis" error?
Data Collection error. This is an example of Garbage In Garbage Out

3. How would you fix this? *(Hint: Can you simply "delete" the gender column? Why might that not be enough?)*
You would need to calibrate the AI to screen for different positions, e.g. entry-level, senior-level, management-level, and feed it resumes from existing employees at each tier. You would also need to define what good and bad resumes are. For hiring for entry-level positions, give it resumes of employees who were brought in as entry-level staff and were promoted at least once as examples of "successful" resumes / candidates, and employees who joined and left soon after (e.g. within 1 year) as examples of "bad" resumes / candidates to look out for. Same for hiring for senior / managerial roles. 

**Output:** Write a one-sentence "Warning Label" that should be placed on this dataset before any Data Scientist uses it.
Warning: this dataset represents anonmymised resumes of employees, with successful resumes based on managers' hiring decisions, which often contain subjective elements beyond resume qualifications. Please validate findings of AI with actual scrutiny / analysis of applicants' resumes before hiring.
```

<details>
<summary>Sample Warning Label</summary>

*"⚠️ This dataset reflects promotion decisions made between 2005–2015 at a male-dominated tech company; it contains strong gender and educational-background bias and must not be used to train hiring or promotion models without demographic auditing and rebalancing."*

A good warning label names: (1) the time period, (2) the source context, (3) the specific bias risk, and (4) what must be done before use. It's a form of **data documentation** — increasingly required by regulation (e.g. EU AI Act) and considered professional best practice.

</details>

### 💬 Q&A & Reflection (10 min)

- Can we ever have 100% unbiased data? If not, what can we do?

```
No, because each person has their own lived experiences, subjectivities and biases. We can try to reduce bias by incorporating some random sampling.
```

<details>
<summary>Suggested answer</summary>

No — all data is collected by humans or human-built systems, and all collection involves choices: what to measure, who to include, which time period to cover. Those choices embed assumptions and blind spots. What we *can* do is be deliberate: document who collected the data and how, actively check for underrepresented groups, test models for differential performance across demographics, and build review processes that catch bias before deployment. The goal isn't zero bias (unachievable) — it's *known and managed* bias.

</details>

- What is the cost — financial and reputational — when an AI system fails in a public-facing application?
```
Financial cost - if AI is used to make financial decisions alone, e.g. buy or sell order on stocks and it fails, it would result in financial losses. Not to mention the existing cost of the AI license / subscription. Reputational loss would be to the company, which will be seen as more disingenuous and relying on AI rather than human judgement. People would trust the company less.
```

<details>
<summary>Suggested answer</summary>

Amazon's internal AI hiring tool (the real-world basis of the Hiring Bot scenario) was scrapped after engineers discovered it was systematically downgrading women's CVs. The reputational cost was significant — the story became a widely-cited cautionary tale in AI ethics. Financially, the costs include: the engineering time spent building and then retiring the system, potential legal liability (discriminatory hiring is illegal in most jurisdictions), and the cost of replacing the tool. In regulated industries like banking or healthcare, biased AI can trigger fines and regulatory scrutiny on top of these costs. A single high-profile failure can also erode public trust in an entire company's AI capabilities for years.

</details>

---

## 🎯 Wrap-Up

**Key Takeaways:**
1. Analytics, Data Science, and AI are a hierarchy — most companies are still working on getting their data clean.
2. ~80% of data work is Collection and Cleaning. The analysis is the remaining 20%.
3. Clean data ≠ Unbiased data. Historical and selection biases are encoded in data that looks perfectly formatted.

**Next Steps:**
- Complete the [Assignment](./assignment.md) — group discussion questions about the data lifecycle.
- Next lesson: Lesson 1.2 covers database design — how data is structurally organised before it can be queried.
