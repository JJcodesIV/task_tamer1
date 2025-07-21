# TaskTamer

**TaskTamer** is an adaptive, ADHD-friendly to-do list web application. It helps users manage and prioritize their daily tasks based on changing priorities and personal energy levels, offering dynamic scheduling, visual cues, and a unified view of tasks and calendar events.

---

## Features

- **Adaptive Prioritization:**  
  Tasks are automatically reordered based on importance, deadlines, and your selected energy level.
- **Flexible Scheduling:**  
  Easily reschedule or snooze tasks as your day progresses.
- **Visual Indicators:**  
  Color bars and category icons signify urgency and type for quick recognition.
- **Energy-based Sorting:**  
  Choose your current energy, and tasks requiring less energy move higher.
- **Calendar Preview:**  
  See today’s (mocked) calendar events alongside your tasks.
- **Drag-and-Drop Ordering:**  
  Manually reorder tasks for extra flexibility.
- **Mobile Friendly:**  
  Fully responsive design for phones and tablets.

---

## Getting Started

### 1. Installation

Just download or copy the `index.html` file (the full prototype code above).  
No installation or dependencies required—everything runs locally in your browser.

### 2. Usage

1. **Open** the `index.html` file in any browser.
2. **Add tasks** using the form at the top. Set category, importance, deadline, and energy requirement.
3. **Set your current energy** using the selector at the top-right (“High”, “Medium”, “Low”).
4. **Review your prioritized task list**. Adjust order manually via drag-and-drop if desired.
5. **Edit, snooze, or delete tasks** using the icons on each card.
6. **Check today’s calendar events** in the “Calendar” section (events are currently mocked).

---

## Screenshots

> *(Add screenshots here once available)*

---

## How Task Prioritization Works

The app calculates a priority score for each task:

- **Importance:** User rates each task (Low/Medium/High).
- **Urgency:** Tasks with closer deadlines are boosted (Urgent/Soon/Later).
- **Energy:** If a task requires more energy than you currently have, it is deprioritized.
- **Manual Order:** You can always override with drag-and-drop.

---

## Customization & Integration

- **Real Calendar Integration:**  
  To sync with Google Calendar or Outlook, extend the JS to use their public APIs and replace the mock calendar events.
- **Persistent Storage:**  
  For saving tasks between sessions, add `localStorage` or integrate with a backend.
- **Categories:**  
  Add more icons or labels by tweaking the `categoryIcons` object in the JS.

---

## Accessibility & ADHD-Friendly Design Choices

- Large, touch-friendly controls
- Color and icon cues for fast scanning
- Flexible, non-punitive snooze/reschedule options
- No registration or distraction-laden onboarding

---

## Development Notes

- **Tech Stack:** Pure HTML, CSS, JavaScript (no frameworks)
- **File:** All logic is contained in a single `index.html` file for easy prototyping.
- **Responsiveness:** Layout adapts to mobile screens.

---

## Contributing

1. Fork the repo or copy the code.
2. Make your changes.
3. Suggest improvements via pull request or by contacting the author.

---

## License

MIT License (Feel free to use, modify, and share.)

---

# Documentation Kit

## File Structure

```
/
└── index.html         # Main (and only) application file
```

---

## Core JS Functions

- **renderTasks()**: Prioritizes and renders the task list, applies visual indicators.
- **calcPriority(task)**: Calculates priority based on importance, urgency, and energy.
- **editTask(idx)**: Loads task data into the form for editing.
- **snoozeTask(idx)**: Moves the task’s deadline to tomorrow.
- **deleteTask(idx)**: Removes a task from the list.
- **enableDragAndDrop()**: Enables drag-and-drop reordering.
- **renderCalendar()**: Shows today's (mock) calendar events.

---

## Extending the App

### Add Task Persistence

Add the following to save and load tasks:

```js
// At the end of renderTasks():
localStorage.setItem('tasks', JSON.stringify(tasks));

// On init():
const saved = localStorage.getItem('tasks');
if (saved) tasks = JSON.parse(saved);
```

### Integrate with Real Calendar

- Use [Google Calendar API](https://developers.google.com/calendar/api/quickstart/js) or [Outlook Calendar API](https://docs.microsoft.com/en-us/graph/api/resources/calendar?view=graph-rest-1.0).
- Replace `calendarEvents` with fetched events.

---

## Accessibility Tips

- Ensure color contrast meets [WCAG guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/).
- Add ARIA labels to interactive elements if expanding app.
- Support keyboard navigation for drag-and-drop (consider a library if needed).

---

## Contact

For questions or feedback, open an issue or email [jjivwr@gmail.com].

---

*Happy taming your tasks!*
