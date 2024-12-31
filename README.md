# Sustainability-Simulation-LEED-Project
A simulation project focused on preparing for LEED certification and sustainability benchmarks

# Objective
This project simulates the preparation process for certifying a sustainable facility under the LEED framework. It explores key project deliverables, including stakeholder engagement, implementation timelines, benchmarks, and compliance with Minimum Program Requirements (MPRs) and prerequisites.

# Key Deliverables
Stakeholder Register: Identified stakeholders crucial for LEED certification and their roles/responsibilities.
Timeline (Gantt Chart): A detailed implementation schedule for achieving project milestones.
Benchmarks: Critical success metrics for energy efficiency, water management, and sustainable materials.
Minimum Program Requirements (MPRs): Guidelines for LEED project eligibility.
Prerequisites: Baseline requirements for LEED certification compliance.

# Workbook
The Excel workbook contains:
Stakeholders: Register with roles and responsibilities.
Timeline: Gantt chart of implementation phases.
Benchmarks: Sustainability performance metrics.
MPRs and Prerequisites: Detailed checklists.
You can view/download the workbook in the /workbook folder [LEED Simulation project.xlsx](https://github.com/user-attachments/files/18268714/LEED.Simulation.project.xlsx)

# Python code for Ganttchart
[Gantt Chart code.txt](https://github.com/user-attachments/files/18283114/Gantt.Chart.code.txt)

Re-importing necessary libraries and re-creating the Gantt chart due to session reset
import matplotlib.pyplot as plt
import matplotlib.dates as mdates
from datetime import datetime, timedelta

Define the project phases, tasks, start dates, and durations
tasks = [
    ("Stakeholder Identification & Engagement", "2025-01-01", 14),
    ("Feasibility Study", "2025-01-15", 21),
    ("Sustainability Goal Setting", "2025-02-05", 7),
    ("Architectural Design & Energy Modeling", "2025-02-13", 42),
    ("Selection of Sustainable Materials", "2025-04-01", 21),
    ("Cost-Benefit Analysis of Design Options", "2025-04-22", 14),
    ("Submit Preliminary LEED Application", "2025-05-06", 7),
    ("Contractor Training on Green Practices", "2025-05-14", 14),
    ("Site Preparation", "2025-05-29", 28),
    ("Core Construction", "2025-06-27", 140),
    ("Implementation of Green Systems (HVAC, etc.)", "2025-11-15", 84),
    ("Building Commissioning", "2026-02-03", 21),
    ("LEED, WELL, and Fitwel Final Applications", "2026-02-25", 28),
    ("Certification Audits & Adjustments", "2026-03-25", 56),
    ("Stakeholder Training on Operations", "2026-05-20", 14)
]

Convert task start dates to datetime objects and calculate end dates
tasks_with_dates = [(task, datetime.strptime(start, "%Y-%m-%d"), datetime.strptime(start, "%Y-%m-%d") + timedelta(days=duration)) for task, start, duration in tasks]

Plotting the Gantt chart
fig, ax = plt.subplots(figsize=(12, 8))
for i, (task, start, end) in enumerate(tasks_with_dates):
    ax.barh(i, (end - start).days, left=start, color="skyblue", edgecolor="black")

Formatting the chart
ax.set_yticks(range(len(tasks_with_dates)))
ax.set_yticklabels([task for task, _, _ in tasks_with_dates])
ax.xaxis.set_major_locator(mdates.MonthLocator())
ax.xaxis.set_major_formatter(mdates.DateFormatter("%b %Y"))
ax.set_xlabel("Timeline")
ax.set_title("Gantt Chart: Sustainable Facility Implementation")
plt.xticks(rotation=45)
plt.tight_layout()

Show the chart
plt.show()
<img width="564" alt="image" src="https://github.com/user-attachments/assets/1fa69214-0925-4635-a7eb-daf83d42e635" />

# Why This Project Matters
This project showcases my ability to:

Apply sustainability principles to real-world scenarios.
Work with frameworks like LEED, WELL, and Fitwel.
Manage projects effectively using tools such as Gantt charts and stakeholder analysis.

Portfolio Site
For more details, visit the portfolio site: [Link to Google Portfolio Site] (Coming Soon).


