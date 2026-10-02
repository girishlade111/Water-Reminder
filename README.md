# Water Reminder

A lightweight **water-intake tracker component** built with React, TypeScript, Tailwind CSS, and [shadcn/ui](https://ui.shadcn.com/) primitives. It helps you track daily hydration with a customizable goal, quick-add buttons, a live progress bar, and a daily reset.

> Single-file, framework-agnostic snippet — drop it into any React + Tailwind project and it just works.

---

## Features

- **Daily hydration goal** — defaults to 2000 ml, adjustable up/down in 100 ml steps
- **Quick-add buttons** — log common drink sizes (250 ml, 500 ml, 750 ml, 1000 ml) with one tap
- **Live progress bar** — animated percentage bar showing intake vs. goal
- **Last-drink timestamp** — records when you last logged a drink
- **Daily reset** — one button clears intake back to zero for a new day
- **Responsive layout** — centered card design, mobile-friendly

## Tech Stack

| Layer    | Technology            |
|----------|-----------------------|
| UI       | React + TypeScript    |
| Styling  | Tailwind CSS          |
| Components | shadcn/ui (`Card`, `Button`) |
| Icons    | lucide-react (`Plus`, `Minus`) |

## Quick Start

The tracker lives in the single file **`Water Reminder`** in this repo. To use it:

1. Copy the file into your React project, e.g. `src/components/WaterReminder.tsx`.
2. Make sure your project has the shadcn/ui `Button` and `Card` components installed:

   ```bash
   npx shadcn-ui@latest add button card
   ```

3. Import and render it:

   ```tsx
   import WaterReminder from "./components/WaterReminder";

   export default function App() {
     return <WaterReminder />;
   }
   ```

No build configuration is needed beyond a standard Vite / Next.js React setup, and there are no environment variables or backend services.

## Project Structure

```
Water-Reminder/
├── Water Reminder   # The component (TSX source, extensionless file)
├── LICENSE          # CC0 1.0 Universal
└── README.md
```

## Notes

- The component is fully client-side; intake data lives in React state (no persistence). For persistence across reloads, wire `currentIntake` / `dailyGoal` to `localStorage` or IndexedDB.
- The original description mentioned WorkManager (Android) / BackgroundTasks (iOS) for reminder notifications — push-notification scheduling is not implemented in this snippet and is a possible extension.

## License

CC0 1.0 Universal — use it freely, no attribution required.

---

Built by Girish Lade — [ladestack.in](https://ladestack.in)
