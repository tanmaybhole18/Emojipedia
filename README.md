# Emojipedia

This is a simple **React** project that displays a list of emojis along with their meanings. The project was created using **CodeSandbox**.

## Features
- Displays a list of emojis with their names and meanings.
- Uses the `map` function to dynamically generate emoji components.
- Built with **React** to efficiently render UI components.

## Technologies Used
- React.js
- JavaScript (ES6+)
- JSX
- CSS

## How `map` is Used
In this project, the `map` function is used to iterate over an array of emoji objects (`emojipedia`) and render a component for each item dynamically.

Example of using `map`:

```jsx
import React from "react";
import Entry from "./Entry";
import emojipedia from "../emojipedia";

function createEntry(emojiTerm) {
  return (
    <Entry
      key={emojiTerm.id}
      emoji={emojiTerm.emoji}
      name={emojiTerm.name}
      description={emojiTerm.meaning}
    />
  );
}

function App() {
  return (
    <div>
      <h1>
        <span>emojipedia</span>
      </h1>
      <dl className="dictionary">{emojipedia.map(createEntry)}</dl>
    </div>
  );
}

export default App;
```

### Explanation
- The `map` function loops through each emoji object in `emojipedia`.
- For each object, it creates an `Entry` component and passes its properties (`emoji`, `name`, `description`) as props.
- This dynamically generates all the emoji entries without manually writing each one.

## Getting Started
1. Clone the repository or open it iCn **CodeSandbox**.
2. Run the React app to see the Emojipedia displayed.
3. Modify `emojipedia.js` to add more emojis if needed.

## Conclusion
This project demonstrates the power of React and the `map` function to dynamically generate UI components from an array of data, making the code reusable and maintainable.

