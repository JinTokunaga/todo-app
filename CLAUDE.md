# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A simple TODO application built with React + TypeScript and Vite. Features include adding, deleting, toggling completion status, and filtering todos.

## Development Commands

```bash
# Install dependencies
npm install

# Start development server (http://localhost:5173)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linter
npm run lint
```

## Architecture

**Tech Stack:**
- React 18 with TypeScript
- Vite for build tooling
- CSS for styling (no UI library)

**Key Files:**
- `src/App.tsx` - Main component with TODO logic and state management
- `src/App.css` - Application styles
- `src/main.tsx` - Application entry point

**Data Model:**
```typescript
interface Todo {
  id: number        // Timestamp-based unique ID
  text: string      // TODO text
  completed: boolean // Completion status
}
```

**State Management:**
- Uses React hooks (`useState`)
- Three state variables: `todos`, `inputValue`, `filter`
- No external state management library

**Features:**
- Add TODO (Enter key or button click)
- Toggle completion (checkbox or text click)
- Delete TODO
- Filter by All/Active/Completed
- Count display for each filter
