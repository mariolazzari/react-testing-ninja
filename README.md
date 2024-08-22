# React Testing Ninja

## Intro

- *Unit tests* test a piece of code in complete isolation
- *Integration tests* tests interactions between different pieces of code
- *End to end tests* tests end user program flows

## Structure

- *Render* component to test
- *Find* elements to interact with
- *Interacts* with found elements
- *Assert* expected results

```jsx
    import { render, screen, expect } from "@testing-library/react";
    import App from "./App";

    test("Test title", () => {
         render(<App />);
         const link = screen.getByText(/learn/);
         expect(link).toBeInTheDocument();
    });

    // or
    it("Test title", () => {
        render(<App />);
        // ...
    });

```

```sh
pnpm test
```