# Label Run Calculator

A lightweight, single-page web application for calculating label printing production runs from die configuration.

![Label Run Calculator](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-AGPLv3-green)

## Features

- **Die Configuration** — Define across/around count, label size, spacing; C/C and repeat length auto-calculated
- **Roll by Amount** — Split a total label quantity into individual rolls, automatically rounding to die multiples
- **Split Roll** — Calculate copies of die for a continuous run, with optional:
  - **Divider** — Split each lane into N equal sub-rolls
  - **Max per Roll** — Set a fixed label count per roll (last roll gets the remainder)
- **Run in Meters** — Total linear run length displayed in both modes
- **Responsive Design** — Works on desktop and mobile
- **Zero Dependencies** — Pure HTML, CSS, and JavaScript

## Getting Started

### Option 1: Open Directly

Open `src/index.html` in any modern web browser — no build step or server required.

### Option 2: Serve Locally

```bash
# Using Python
python -m http.server 8080 --directory src

# Using Node.js (npx)
npx serve src
```

Then navigate to `http://localhost:8080`.

## Usage

### Die Configuration

| Field       | Description                                    |
|-------------|------------------------------------------------|
| **Across**  | Number of labels across the web (width lanes)  |
| **Around**  | Number of labels per revolution of the die     |
| **Size**    | Label dimension in mm                          |
| **Space**   | Gap between labels in mm                       |
| **C/C**     | Centre-to-centre distance (auto-calculated)    |

### Roll by Amount

Enter the **Total Labels** needed and the desired **Labels per Roll**. The calculator rounds the roll count up to the nearest multiple of the across count and shows:

- Rolls needed vs. actual rolls produced
- Extra rolls
- Revolutions per roll
- Total die copies
- Run length in meters

### Split Roll

Enter the **Total Labels** for a single continuous press run. Optionally:

- Set a **Divider** (e.g. 4) to split each lane into equal sub-rolls
- Set a **Max Labels per Roll** (e.g. 200) for fixed-size rolls with a remainder on the last

## Project Structure

```
LabelCalculate/
├── src/
│   └── index.html      # Complete application (HTML + CSS + JS)
├── README.md
├── LICENSE
└── .gitignore
```

## License

This project is licensed under the GNU Affero General Public License v3.0 — see the [LICENSE](LICENSE) file for details.

## Author

**Roger Jemterud** — [@RzrZrx](https://github.com/RzrZrx)
