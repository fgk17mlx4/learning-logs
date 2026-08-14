# React Hooks Notes (2026-08-14)

- `useCallback` vs `useMemo`: useCallback returns memoized function, useMemo returns memoized value.
- Avoid creating new object/array deps in useEffect — use refs or split effects.
- Custom hooks should start with `use` and return a stable API.
- `useReducer` is better than multiple `useState` for related state transitions.
- Remember: `setState` inside effects can cause infinite loops if deps missing.

Next: explore `useDeferredValue` for expensive renders.