# SpendWise Dashboard Shell

SpendWise is a responsive personal finance dashboard created with HTML5 and CSS3. It provides a visual overview of income, expenses, savings, spending categories, and recent transactions.

This project is the Week 4 foundation of a larger budget tracker capstone project. It focuses on building a modern dashboard layout using CSS Grid, Flexbox, CSS custom properties, responsive media queries, and card micro-interactions.

## Project Preview

SpendWise includes:

- A sidebar navigation menu.
- A dashboard header.
- Financial overview cards.
- Six spending category cards.
- A recent transactions section.
- Responsive layouts for smaller screens.
- Hover and keyboard focus effects.
- An optional dark theme based on the user's system preference.

## Features

- Available balance summary.
- Total income summary.
- Total expenses summary.
- Savings goal progress.
- Food spending category.
- Transport spending category.
- Rent spending category.
- Entertainment spending category.
- Savings category.
- Utilities category.
- Recent transactions list.
- Responsive dashboard layout.
- Dark theme support.
- Keyboard-accessible card focus states.
- Reduced-motion support for users who prefer less animation.

## Technologies Used

- HTML5
- CSS3
- CSS Grid
- CSS Flexbox
- CSS custom properties
- CSS media queries
- Google Fonts
- Responsive web design

## Project Structure

```text
spendwise-dashboard/
│
├── index.html
├── style.css
└── README.md
```

## Dashboard Sections

### Sidebar

The sidebar contains the SpendWise brand and navigation links for:

- Dashboard
- Transactions
- Budgets
- Reports
- Settings

### Dashboard Header

The header displays:

- The current date.
- A welcome message.
- The user's name.
- A notification button.
- The account type.

### Financial Overview

The overview section contains four summary cards:

- Available balance.
- Total income.
- Total expenses.
- Savings goal progress.

### Spending Categories

The dashboard contains six category cards:

- Food
- Transport
- Rent
- Entertainment
- Savings
- Utilities

Each card includes a category name, amount, percentage, icon, and progress indicator.

### Recent Transactions

The recent transactions section displays sample financial activity, including:

- Grocery shopping.
- Monthly salary.
- Bus fare.

## CSS Grid Usage

CSS Grid is used for the overall dashboard structure:

```css
.dashboard-layout {
    display: grid;
    grid-template-columns: var(--sidebar-width) minmax(0, 1fr);
}
```

CSS Grid is also used for the overview and category cards:

```css
.overview-cards {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
}

.category-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
}
```

Grid is useful for arranging larger page regions and repeated cards in rows and columns. [web:95]

## Flexbox Usage

Flexbox is used to arrange items in one direction, such as rows or columns. [web:99]

Examples from this project include:

```css
.sidebar {
    display: flex;
    flex-direction: column;
}
```

```css
.dashboard-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
```

```css
.overview-card {
    display: flex;
    flex-direction: column;
}
```

Flexbox is used for:

- Sidebar navigation items.
- Header content.
- Profile information.
- Dashboard card content.
- Transaction rows.
- Icons and labels.

## CSS Theme Variables

The color palette is defined using CSS custom properties inside `:root`:

```css
:root {
    --brand-color: #123c69;
    --accent-color: #2a9d8f;
    --surface-color: #ffffff;
    --background-color: #f4f7fb;
    --primary-text: #172b4d;
    --secondary-text: #6b7c93;
}
```

The variables are reused throughout the stylesheet to keep the dashboard colors consistent and easy to update.

## Card Micro-interactions

The overview cards and category cards include hover and keyboard focus effects:

```css
.overview-card:hover,
.overview-card:focus-visible,
.category-card:hover,
.category-card:focus-visible {
    transform: translateY(-4px);
    box-shadow: 0 14px 30px rgba(23, 43, 77, 0.13);
}
```

The cards move slightly upward and receive a stronger shadow when the user hovers over them or focuses on them using the keyboard.

The transition lasts 180 milliseconds, which is below the required 250 milliseconds.

## Responsive Design

The dashboard becomes a single-column layout on smaller screens:

```css
@media (max-width: 767px) {
    .dashboard-layout {
        grid-template-columns: 1fr;
    }
}
```

The responsive design also:

- Stacks the sidebar above the main content.
- Changes the card grids to two columns.
- Changes the cards to one column on very small screens.
- Adjusts spacing and header alignment.
- Makes the dashboard easier to use on mobile devices.

The layout can be tested using the browser's DevTools Device Toolbar. Media queries allow CSS rules to respond to viewport size and device characteristics. [web:97]

## Dark Theme

The dashboard supports a dark theme when the user's device is set to dark mode:

```css
@media (prefers-color-scheme: dark) {
    :root {
        --brand-color: #071d33;
        --background-color: #0b1726;
        --surface-color: #132337;
        --primary-text: #e8f0f7;
        --secondary-text: #9db0c4;
    }
}
```

The dark theme changes the values of the CSS variables while keeping the same HTML and layout structure.

## How to Run the Project

1. Clone or download the repository.
2. Open the project folder.
3. Make sure the following files are present:

```text
index.html
style.css
README.md
```

4. Open `index.html` in a web browser.

You can also open the folder in Visual Studio Code and use the Live Server extension to preview the dashboard.

## How to Test Responsiveness

1. Open the dashboard in a browser.
2. Open Developer Tools.
3. Select the Device Toolbar.
4. Test different screen sizes.
5. Verify that the layout becomes a single column below 768px.
6. Test both desktop and mobile views.

## Accessibility Features

This project includes:

- Semantic HTML sections.
- Accessible navigation labeling.
- Descriptive button labels.
- Keyboard focus states.
- `tabindex="0"` on interactive dashboard cards.
- Reduced-motion support for users who prefer less animation.
- Sufficient spacing between major interface elements.

## Future Improvements

- Add JavaScript functionality.
- Add new transactions dynamically.
- Calculate totals automatically.
- Add edit and delete transaction buttons.
- Store transaction data using local storage.
- Add spending charts.
- Add a working theme toggle.
- Add a functional sidebar navigation.
- Connect the dashboard to a database.
- Add user authentication.

## Author

Created by **Zamzam Ismail Abdi**.

## License

This project was created for educational purposes.
