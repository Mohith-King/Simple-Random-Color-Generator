# Random Background Generator

A lightweight vanilla JavaScript project that generates a new random background color every time you click a button. It also updates the text color so the interface stays visually dynamic and feels alive with each interaction.

## Overview

This project is a simple example of how HTML, CSS, and JavaScript can work together to create an interactive UI without any framework, build step, or external dependency.

The page contains:

- A full-screen content container
- A short text paragraph
- A `Change Background` button

When the button is clicked:

- The container receives a new random background color
- The paragraph text receives a different random color
- The change happens instantly with a smooth transition

## Features

- Fully responsive full-screen layout
- Random hex color generation using JavaScript
- Smooth color transition for a better user experience
- Clean, minimal structure with no dependencies
- Easy to understand and modify

## How It Works

The core logic lives directly inside `index.html`.

### Random Color Generator

The app uses `Math.random()` to generate a number between `0` and `0xffffff`, converts it to a hexadecimal string, and pads it to ensure it always has six digits.

Conceptually, it works like this:

```js
"#" + Math.floor(Math.random() * 0xffffff).toString(16).padStart(6, "0");
```

That produces valid CSS hex colors such as:

- `#7f3caa`
- `#12f09e`
- `#ffcc00`

### Button Interaction

An event listener is attached to the button. On each click, it:

1. Generates one random color for the container background
2. Generates another random color for the paragraph text
3. Applies both colors immediately using inline styles

## Project Structure

```text
.
|-- index.html
|-- style.css
`-- README.md
```

### `index.html`

Contains the page markup and the JavaScript logic that powers the color-changing behavior.

### `style.css`

Handles the layout, spacing, alignment, and transition effects.

## How To Run

This project does not require installation.

1. Open `index.html` in your browser.
2. Click **Change Background**.
3. Watch the background and text colors update instantly.

If you prefer, you can also open the folder in VS Code and use Live Server for a smoother local preview workflow.

## Why This Project Is Useful

Even though the app is small, it demonstrates a few important front-end fundamentals:

- DOM selection
- Event handling
- Inline style updates
- Randomized value generation
- Basic responsive layout with flexbox

It is a strong beginner project because it shows how a few lines of JavaScript can create a visible, interactive effect.

## Possible Improvements

If you want to extend the project, a few nice upgrades would be:

- Show the current hex code on screen
- Add a copy-to-clipboard button
- Generate gradients instead of a single color
- Keep the text color automatically readable against the background
- Add a history of previous colors

## Browser Support

This project uses standard browser features and should work in all modern browsers.

## License

No license has been specified yet. You can add one if you plan to share or publish the project.
