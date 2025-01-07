# Project Folder Structure and Collaboration Guide for Habit Tracker App

## Folder Structure

Below is the recommended folder structure for your React + Vite project:

```
habit-tracker/
│
├── public/
│   ├── favicon.ico       # Application favicon
│   └── index.html        # Main HTML file
│
├── src/
│   ├── assets/           # Static assets like images, fonts, and icons
│   │   ├── images/
│   │   └── styles/
│   │       └── global.css # Global styles
│   │
│   ├── components/       # Reusable React components
│   │   ├── HabitCard.jsx  # Component for individual habit cards
│   │   ├── Header.jsx     # Header component
│   │   └── Footer.jsx     # Footer component
│   │
│   ├── features/         # Feature-specific components and logic
│   │   ├── HabitList/     # Habit listing feature
│   │   │   ├── HabitList.jsx
│   │   │   └── HabitList.css
│   │   ├── HabitForm/     # Form to add/edit habits
│   │   │   ├── HabitForm.jsx
│   │   │   └── HabitForm.css
│   │   └── HabitStats/    # Stats and analytics for habits
│   │       ├── HabitStats.jsx
│   │       └── HabitStats.css
│   │
│   ├── contexts/         # React context providers for global state
│   │   └── HabitContext.jsx
│   │
│   ├── hooks/            # Custom React hooks
│   │   └── useHabits.js   # Hook for habit-related logic
│   │
│   ├── pages/            # Page-level components
│   │   ├── Home.jsx       # Home page
│   │   ├── Dashboard.jsx  # User dashboard
│   │   └── About.jsx      # About page
│   │
│   ├── services/         # API calls and utilities
│   │   ├── habitService.js # Functions to interact with backend
│   │   └── authService.js  # Functions to handle authentication
│   │
│   ├── App.jsx           # Root component
│   ├── main.jsx          # Entry point for React
│   └── vite-env.d.ts     # TypeScript environment declarations (if using TS)
│
├── .gitignore            # Git ignore rules
├── package.json          # Project metadata and dependencies
├── README.md             # Project documentation
└── vite.config.js        # Vite configuration file
```

---

## Where to Put Which File

1. **Static Assets**:  
   - Use the `assets/` folder for images, fonts, and global styles.  
   - Example: Place the app logo in `assets/images/` and use it across components.

2. **Reusable Components**:  
   - Create generic UI components (e.g., buttons, cards) in the `components/` directory.  
   - Example: The `HabitCard.jsx` file contains a component to display individual habits.

3. **Feature-specific Code**:  
   - Each feature (e.g., listing habits, analytics) has its own folder under `features/`.
   - Use separate files for JSX and CSS to keep styles modular and scoped.

4. **Global State Management**:  
   - Use `contexts/` to define context providers for global state, such as `HabitContext.jsx`.

5. **Custom Hooks**:  
   - Place reusable custom hooks in `hooks/`, like `useHabits` to encapsulate habit-related logic.

6. **Page-level Components**:  
   - Use `pages/` for components that correspond to routes, such as `Home.jsx` for the landing page.

7. **API Calls and Utilities**:  
   - Write API interactions in `services/`. This ensures separation of concerns.

---

## Collaboration Guidelines

1. **Commit Messages**:  
   - Follow a consistent format:  
     ```
     <type>: <description>
     ```
     - Types: `feat` (feature), `fix` (bug fix), `docs` (documentation), `style` (formatting), `refactor`, `test`, `chore`.
     - Example: `feat: add habit form validation`

2. **Coding Standards**:  
   - Use ESLint and Prettier for code formatting. Add a pre-commit hook to enforce standards.

---
