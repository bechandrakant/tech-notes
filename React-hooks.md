## React Hooks

**Topics**
- State Management
  - useState
  - useReducer
  - useContext
  - useSyncExternalStore
- Ref Hooks
  - useRef
  - useImperativeHandle
- Effect Hooks
  - useEffect
  - useLayoutEffect
  - useInsertionEffect
- Performance Hooks
  - useMemo
  - useCallback
- Transition Hooks
  - useTransition
  - useDeferredValue
- Random Hooks
  - useId
  - useDebugValue
- React 19 Hooks
  - use
  - useOptimistic
  - useFormState
  - useFormStatus

Here’s a table with all React hooks, their descriptions, and common uses:

| **Hook**              | **Description**                                                                                                                                                          | **Common Uses**                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `useState`            | Declares state variables in functional components.                                                                                                                       | Tracking local component state, such as form inputs, toggles, counters.                                                                                                                                                          |
| `useEffect`           | Performs side effects in function components. Runs after render by default.                                                                                             | Fetching data, updating DOM, setting up timers or subscriptions, and cleaning up when the component unmounts.                                                                                                                    |
| `useContext`          | Accepts a context object and returns the current context value.                                                                                                         | Accessing context values like themes, authentication data, or global state without passing props.                                                                                                                                |
| `useReducer`          | An alternative to `useState` for more complex state logic using reducers.                                                                                               | Managing complex component states, handling complex state transitions, or sharing logic between components.                                                                                                                      |
| `useCallback`         | Returns a memoized version of a callback function that only changes if dependencies change.                                                                             | Optimizing performance by preventing re-creation of functions in components or avoiding unnecessary renders.                                                                                                                     |
| `useMemo`             | Returns a memoized value that only recalculates if dependencies change.                                                                                                 | Optimizing performance by memoizing computed values, such as expensive calculations or derived state.                                                                                                                            |
| `useRef`              | Creates a mutable object that persists between renders, often used to access DOM elements directly.                                                                     | Accessing or manipulating DOM elements, storing previous values, or maintaining state that does not trigger re-renders.                                                                                                         |
| `useLayoutEffect`     | Similar to `useEffect` but runs synchronously after all DOM mutations.                                                                                                  | Making DOM changes or measuring layout dimensions before the browser paints. Useful for animations or layout shifts.                                                                                                             |
| `useImperativeHandle` | Allows customization of the instance value exposed to parent components when using `React.forwardRef`.                                                                  | Providing specific values or methods to parent components that use a ref, enabling more control over child components.                                                                                                           |
| `useDebugValue`       | Customizes the label shown in React DevTools for custom hooks.                                                                                                          | Debugging custom hooks more easily by adding meaningful labels in DevTools.                                                                                                                                                      |
| `useTransition`       | Allows you to mark state updates as non-urgent, enabling transitions.                                                                                                   | Creating smoother UI updates by deferring non-critical state updates, often for complex layouts or animations.                                                                                                                   |
| `useDeferredValue`    | Returns a deferred version of a state value, delaying updates until less urgent work is done.                                                                           | Improving performance in UI-intensive components by deferring non-essential changes until after critical updates are complete.                                                                                                   |
| `useId`               | Generates a unique ID that is consistent across renders.                                                                                                                | Creating unique identifiers for accessibility attributes or when mapping items without needing a manually specified key.                                                                                                         |
| `useSyncExternalStore`| Allows subscribing to external stores and synchronizing with external data sources.                                                                                     | Syncing components with global state management libraries like Redux or Zustand in a way that works with concurrent rendering.                                                                                                   |
| `useInsertionEffect`  | A hook for injecting CSS styles into the DOM before the DOM is painted.                                                                                                 | Useful for library authors or applications where CSS-in-JS is used to ensure styles are applied before content is displayed, minimizing layout shifts.

Here are quick notes for React hooks to help you remember their purpose and use cases:

---

### 1. `useState`
- **Purpose**: Adds state to functional components.
- **Usage**: Declare a state variable and a function to update it.
- **Example**: `const [count, setCount] = useState(0);`
- **Notes**: Re-rendering happens when state changes. Great for local states like form inputs, toggles, or counters.

---

### 2. `useReducer`
- **Purpose**: An alternative to `useState` for complex state logic or state transitions.
- **Usage**: Accepts a reducer function and an initial state, returns state and dispatch function.
- **Example**: `const [state, dispatch] = useReducer(reducer, initialState);`
- **Notes**: Ideal for managing complex local state or state machines.

---

### 3. `useContext`
- **Purpose**: Accesses context values in any component without prop drilling.
- **Usage**: Takes a context object and returns its current value.
- **Example**: `const value = useContext(MyContext);`
- **Notes**: Useful for themes, authentication, and global state.

---

### 4. `useSyncExternalStore`
- **Purpose**: Synchronizes components with external state stores.
- **Usage**: Particularly useful with state management libraries (Redux, Zustand).
- **Example**: `useSyncExternalStore(subscribe, getSnapshot);`
- **Notes**: Ensures compatibility with React’s concurrent rendering.

---


### 5. `useEffect`
- **Purpose**: Handles side effects in function components (e.g., fetching data, subscriptions).
- **Usage**: Accepts a function that runs after render, with an optional dependency array.
- **Example**: `useEffect(() => { /* side effect */ }, [dependencies]);`
- **Notes**: Dependency array controls when it re-runs. Empty array (`[]`) means it runs once on mount.

---

### 6. `useLayoutEffect`
- **Purpose**: Similar to `useEffect` but fires after all DOM changes.
- **Usage**: Used for measuring DOM elements and making layout adjustments.
- **Example**: `useLayoutEffect(() => { /* layout effect */ }, [dependencies]);`
- **Notes**: Runs synchronously after DOM updates, ideal for animations or measurements.

---

### 7. `useInsertionEffect`
- **Purpose**: Injects CSS styles before the browser paints the DOM.
- **Usage**: Helps avoid layout shifts by ensuring styles are applied first.
- **Example**: `useInsertionEffect(() => { /* insert styles */ });`
- **Notes**: Primarily for CSS-in-JS libraries to ensure styles are ready before content appears.

--- 

### 8. `useCallback`
- **Purpose**: Memoizes a function so it’s only recreated if dependencies change.
- **Usage**: Prevents unnecessary re-renders by reusing the same function.
- **Example**: `const memoizedCallback = useCallback(() => { /* callback */ }, [dependencies]);`
- **Notes**: Helpful for passing stable functions to child components.

---

### 9. `useMemo`
- **Purpose**: Memoizes a computed value, recalculating only if dependencies change.
- **Usage**: Optimizes performance for expensive calculations.
- **Example**: `const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);`
- **Notes**: Great for derived state that requires significant computation.

---

### 7. `useRef`
- **Purpose**: Creates a persistent, mutable reference that doesn’t trigger re-renders.
- **Usage**: Useful for accessing or manipulating DOM elements.
- **Example**: `const inputRef = useRef(null);`
- **Notes**: Can store previous values or non-state values without causing re-renders.

---

### 9. `useImperativeHandle`
- **Purpose**: Customizes the ref instance value exposed to parent components.
- **Usage**: Paired with `React.forwardRef` to expose functions or values.
- **Example**: `useImperativeHandle(ref, () => ({ customMethod }));`
- **Notes**: Controls what is exposed to the parent, often for methods in child components.

---

### 10. `useDebugValue`
- **Purpose**: Labels custom hooks for better visibility in React DevTools.
- **Usage**: Displays useful debug information.
- **Example**: `useDebugValue(value);`
- **Notes**: Helps understand custom hooks' internal states while debugging.

---

### 11. `useTransition`
- **Purpose**: Defers non-urgent state updates for smoother UI transitions.
- **Usage**: Marks updates as low-priority, improving performance.
- **Example**: `const [isPending, startTransition] = useTransition();`
- **Notes**: Useful for complex UI updates, like search filtering or animations.

---

### 12. `useDeferredValue`
- **Purpose**: Delays state updates until after critical renders are complete.
- **Usage**: Avoids quick, unnecessary re-renders.
- **Example**: `const deferredValue = useDeferredValue(value);`
- **Notes**: Helps prevent flickering by deferring non-essential state changes.

---

### 13. `useId`
- **Purpose**: Generates a unique, stable ID that is consistent across renders.
- **Usage**: Used for form controls or accessibility attributes.
- **Example**: `const id = useId();`
- **Notes**: Guarantees unique IDs for dynamic elements without hardcoded values.

---

These notes cover the purpose, usage, and best practices for each React hook, which should serve as a handy reference for quick understanding and application.