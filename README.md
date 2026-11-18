<a id="top"></a>

<div align="center">

# **Event Analytics Dashboard**

<b><ins>Interactive Looker Studio dashboards that turn 25,000+ participant records from 70+ university events into insights on demographics, engagement, future event planning, and exit-ticket feedback.</ins></b>

<br>

![Status](https://img.shields.io/badge/status-COMPLETED-orange?style=for-the-badge)
![Looker Studio](https://img.shields.io/badge/Looker_Studio-4285F4?style=for-the-badge&logo=looker&logoColor=white)

</div>

<br>

<details open>
<summary><b>Table of Contents</b></summary>

1. [Project Overview](#project-overview)
2. [Tech Stack](#tech-stack)
3. [How It Works](#how-it-works)
4. [Skills Learned](#skills-learned)
5. [Challenges and Solutions](#challenges-and-solutions)
6. [Project Structure](#project-structure)
7. [Getting Started](#getting-started)
8. [Extra Things](#extra-things)
9. [Credits and Contact](#credits-and-contact)

</details>

---

## <ins>Project Overview</ins>

> **TL;DR:** A three-page **Looker Studio** dashboard that analyzes **25,000+ participant records** from **70+ university international events** and exit-ticket feedback to show who attends, how they hear about events, and which topics to plan next.

### ▸ Problem
Data on international events was collected through **Microsoft Forms** and kept in one large workbook: a list of programs, every participant per event, the exit-ticket feedback form, and a list of unique participants. With dozens of columns and thousands of rows per sheet, there was no quick way to see who was attending, which events and topics drew the most people, or how participants found out about the events. That made it hard to evaluate past events and plan new ones for the future.

### ▸ Objectives
- *Give a clear overview of participant demographics*: class standing, faculty, major and campus.
- *Show which events, topics, types and countries drew the most participants*, and how participation changed by month.
- *Support planning of future events* with suggested topics and communication channel analysis.
- *Make every page explorable* with dynamic filters that apply across the whole dashboard.

### ▸ Context
This project ran for about 4 months with about biweekly progress tracking. The data was provided to me by a member in charge of international events at my university (my supervisor), and I was trusted to cleanly maintain the form, track participant activity, and use the data to provide decisions or recommendations for the next batch of International events.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>Tech Stack</ins>

> The tools I **used** and what I used them **for**.

| Category | Tool | What I Used It For |
|:---|:---|:---|
| **Data / Storage** | Microsoft Forms, Microsoft Excel | Collecting exit-ticket responses and storing the four-sheet event workbook |
| **Data Processing** | Microsoft Excel | Cleaning the sheets, standardizing event, faculty, and campus values, and building the unique participant list |
| **Visualization** | Looker Studio | The three dashboard pages, calculated fields, and the filters shared across pages |
| **Tools** | Google Gemini | Look up Excel formulas and learn how to utilize Looker Studio's range of dynamic graphs |

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>How It Works</ins>

> Event registration data is cleaned into one dataset, connected to Looker Studio, and explored through three linked dashboard pages.

```
Event Data (70+ events) → Cleaning and Combining → Data Source → Looker Studio (3 pages + shared filters)
```

1. **Collect.** Participant records from the events.
2. **Clean and combine.** Records from every event are merged into one table with consistent values for faculty, major, campus, event topic, type and country. Apart from that, I delete the duplicate records and records that aren't enrolled in my university.
3. **Connect.** The dataset is connected to Looker Studio as the data source.
4. **Visualize.** Three pages answer three questions:
   - **Event IE Dashboard:** *Who attends?* Total participants, plus breakdowns by class standing, faculty, major and campus.
   - **Event Engagement Dashboard:** *What should we plan next?* Suggested future topics, communication channels, and monthly participants with a cumulative trend line.
   - **Event Profile Dashboard (Event Details):** *Which events performed best?* Ranked tables of event titles, topics and countries, plus charts by topic, type and month.
5. **Filter.** Dynamic filters on every page let users narrow the whole dashboard to a specific segment.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>Skills Learned</ins>

> What this project taught me, technically and beyond.

- **Dashboard design:** Planning a multi-page dashboard where each page answers one question, with a consistent layout, color theme and chart style. See `Looker_Studio_Project.pdf`.
- **Data cleaning and preparation:** Working with a four-sheet workbook from Microsoft Forms: picking the columns that matter out of 50+, keeping event names consistent across sheets, and separating participant records from unique students by student ID.
- **Interactive filtering:** Building dynamic filters that work across every page, so one dashboard serves many different questions. See `Looker_Studio_Project.pdf`.
- **Calculated metrics:** Separating unique participants from total records, and adding a cumulative participant trend next to the monthly counts. See `Looker_Studio_Project.pdf`, pages 1–3.
- **Data storytelling:** Turning raw counts into insights that support decisions, such as which topics, countries, and channels to focus on for the next events.
- **Communicating with supervisor:** Presenting and getting continuous feedback from my supervisor (faculty member) biweekly while keeping the dashboard up to date with the goal at hand.

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>Challenges and Solutions</ins>

> What went wrong, how I fixed it, and what I took away from the project.

**Combining data from 70+ different events.** Each event's participant data could use different column names and spellings for the same faculty, major, campus or country, which would split one category into several in the charts. I overcame this challenge by doing standard preprocessing procedures and merging similar columns.

**Turning open-ended answers into usable topics.** Participants wrote their topic suggestions in free text, so the same idea showed up in many different wordings. At first, Microsoft Forms has a summary feature that shows the keywords, but after trying TF-IDF keyword extraction, the results are similar to those in Microsoft Forms. 

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>Project Structure</ins>

```
Event-Analytics-Dashboard-with-Looker-Studio/
├── images/                     # dashboard pages used in this README
├── Looker_Studio_Project.pdf   # PDF export of the three dashboard pages
└── README.md
```

<p align="right">(<a href="#top">back to top</a>)</p>

---

## <ins>Credits and Contact</ins>

**Acknowledgements:** My supervisor for providing the data and entrusting me with the preprocessing and summarization of the feedback forms.

**Author:** **Hansel Sebastian**, *Data Science Student @ Bina Nusantara University*

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/hanhansel)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/hansel-sebastian-5a19b8245)

<p align="right">(<a href="#top">back to top</a>)</p>
