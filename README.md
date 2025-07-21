TaskTamer
TaskTamer is an adaptive, ADHD-friendly to-do list web application. It helps users manage and prioritize their daily tasks based on changing priorities and personal energy levels, offering dynamic scheduling, visual cues, and a unified view of tasks and calendar events.

Features
Adaptive Prioritization:
Tasks are automatically reordered based on importance, deadlines, and your selected energy level.
Flexible Scheduling:
Easily reschedule or snooze tasks as your day progresses.
Visual Indicators:
Color bars and category icons signify urgency and type for quick recognition.
Energy-based Sorting:
Choose your current energy, and tasks requiring less energy move higher.
Calendar Preview:
See today’s (mocked) calendar events alongside your tasks.
Drag-and-Drop Ordering:
Manually reorder tasks for extra flexibility.
Mobile Friendly:
Fully responsive design for phones and tablets.
Getting Started
1. Installation
Just download or copy the index.html file (the full prototype code above).
No installation or dependencies required—everything runs locally in your browser.

2. Usage
Open the index.html file in any browser.
Add tasks using the form at the top. Set category, importance, deadline, and energy requirement.
Set your current energy using the selector at the top-right (“High”, “Medium”, “Low”).
Review your prioritized task list. Adjust order manually via drag-and-drop if desired.
Edit, snooze, or delete tasks using the icons on each card.
Check today’s calendar events in the “Calendar” section (events are currently mocked).
Screenshots
(Add screenshots here once available)

How Task Prioritization Works
The app calculates a priority score for each task:

Importance: User rates each task (Low/Medium/High).
Urgency: Tasks with closer deadlines are boosted (Urgent/Soon/Later).
Energy: If a task requires more energy than you currently have, it is deprioritized.
Manual Order: You can always override with drag-and-drop.
Customization & Integration
Real Calendar Integration:
To sync with Google Calendar or Outlook, extend the JS to use their public APIs and replace the mock calendar events.
Persistent Storage:
For saving tasks between sessions, add localStorage or integrate with a backend.
Categories:
Add more icons or labels by tweaking the categoryIcons object in the JS.
Accessibility & ADHD-Friendly Design Choices
Large, touch-friendly controls
Color and icon cues for fast scanning
Flexible, non-punitive snooze/reschedule options
No registration or distraction-laden onboarding
Development Notes
Tech Stack: Pure HTML, CSS, JavaScript (no frameworks)
File: All logic is contained in a single index.html file for easy prototyping.
Responsiveness: Layout adapts to mobile screens.
Contributing
Fork the repo or copy the code.
Make your changes.
Suggest improvements via pull request or by contacting the author.
License
MIT License (Feel free to use, modify, and share.)# task_tamer1
