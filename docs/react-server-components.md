# React Server Components Notes

- Server Components run only on the server, reducing client JS bundle size.
- They can directly access databases/APIs without exposing secrets.
- Client Components are marked with `"use client"` directive.
- Can mix both: pass Server Components as children to Client Components.
- Key tradeoff: no hooks/state in Server Components — lift state to client boundaries.

## Quick Example
```jsx
// ServerComponent.js (default)
export default function ServerComponent() {
  const data = await fetchData(); // runs on server
  return <ClientComponent>{data}</ClientComponent>;
}
```

Remember: streaming and Suspense pair well with RSC for progressive rendering.