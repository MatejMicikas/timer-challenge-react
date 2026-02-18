# Timer Challenge - React App

A small React project focused on **refs management**, **imperative
component control**, and **accurate state-driven UI updates**.

The repository serves as a **portfolio project** demonstrating
intermediate React concepts such as `useRef`, `forwardRef`,
`useImperativeHandle`, portals, and precise timer handling with
`setInterval`.

---

## Live Preview

https://timer-challenge-react.vercel.app/

---

## Features

-   Multiple difficulty levels (1s, 5s, 10s, 15s challenges)
-   Player name input using `useRef`
-   High-precision countdown timer (10ms interval updates)
-   Score calculation based on timing accuracy
-   Modal dialog rendered via **React Portal**
-   Imperative control of child component (`forwardRef` +
    `useImperativeHandle`)
-   Dynamic UI state (active timer, win/loss state)

---

## Tech Stack

-   **React** (functional components, hooks)
-   **Vite**
-   **JavaScript (ES6+)**
-   **CSS**
-   Native HTML `<dialog>` element

---

## Project Structure

``` text
src/
├── components/
│   ├── Player.jsx
│   ├── TimerChallenge.jsx
│   └── ResultModal.jsx
├── assets/
│   └── react.svg
├── App.jsx
├── main.jsx
└── index.css
```

**Highlights:**

-   `useRef` for DOM access and timer storage
-   `forwardRef` + `useImperativeHandle` for exposing imperative methods
-   `createPortal` for rendering modal outside main DOM hierarchy
-   Derived state (`score`, formatted time, active state)
-   Interval management and cleanup logic

---

## Key Concepts Demonstrated

-   Imperative vs declarative React patterns
-   Managing side effects with timers
-   Preventing stale state updates (functional state updates)
-   Component communication via refs
-   Portals for UI layering
-   Conditional rendering
-   Encapsulation of UI logic into reusable components

---

## How It Works

The player attempts to stop the timer as close as possible to the target
time.

Score is calculated as:

    score = (1 - remainingTime / targetTime) * 100

The closer the stop is to zero remaining time (without exceeding), the
higher the score.

If the timer reaches zero before stopping, the player loses.

---

## Getting Started

### 1. Clone the repository

``` bash
git clone https://github.com/MatejMicikas/timer-challenge-react
cd timer-challenge-react
```

### 2. Install dependencies

``` bash
npm install
```

### 3. Run the development server

``` bash
npm run dev
```

The app will be available at:

    http://localhost:5173

---

## Possible Improvements

-   Add persistent high scores (localStorage)
-   Add sound effects
-   Add animations for better UX
-   Improve mobile responsiveness
-   Add unit tests for timer logic
-   Convert to TypeScript

---

## 👤 Author

Matej Micikáš\
Front-end / JavaScript developer\
Interested in clean React architecture and maintainable code

---

## License

This project is open source and available under the [MIT](LICENSE)
License.
