# Site institucional Adriana Magalhães

Esse projeto, foi desenvolvido com o objetivo de apresentar o

## Repository Structure

```
.
├── public/
│   ├── css/
│   ├── fonts/
│   ├── js/
│   ├── index.html
│   └── robots.txt
├── src/
│   ├── components/
│   ├── data/
│   ├── App.jsx
│   ├── App.css
│   ├── index.js
│   └── serviceWorker.js
├── package.json
├── README.md
└── _config.yml
```

### Key Files:
- `src/App.jsx`: Main application component
- `src/components/`: React components for each section
- `src/data/data.json`: Content configuration file
- `public/index.html`: HTML entry point
- `package.json`: Project dependencies and scripts

## Usage Instructions

### Installation

1. Ensure you have Node.js (v12 or later) and npm installed.
2. Clone the repository:
   ```
   git clone <repository-url>
   cd landingpage-react-template
   ```
3. Install dependencies:
   ```
   npm install
   ```

### Getting Started

1. Start the development server:
   ```
   npm start
   ```
2. Open `http://localhost:3000` in your browser.

### Configuration

Edit `src/data/data.json` to customize the content for each section of the landing page.

### Customization

1. Modify components in `src/components/` to change section layouts.
2. Update styles in `src/App.css` or individual component CSS files.
3. Replace images in `public/img/` with your own assets.

### Building for Production

To create a production build:

```
npm run build
```

This will generate optimized files in the `build/` directory.

### Testing

Run the test suite:

```
npm test
```

### Troubleshooting

#### Issue: Components not updating after data changes
- Ensure you've saved all modified files
- Restart the development server: `npm start`

#### Issue: Styles not applying correctly
- Check for CSS syntax errors in your stylesheets
- Verify that the correct CSS classes are being used in components

#### Debugging
- Use React Developer Tools browser extension for component inspection
- Check the browser console for any error messages or warnings

## Data Flow

The application follows a top-down data flow pattern:

1. `App.jsx` loads data from `data.json` using React's `useState` and `useEffect` hooks.
2. The data is then passed down to child components as props.
3. Each component renders its section using the received data.
4. User interactions (e.g., form submissions) are handled within individual components.

```
App (data loaded)
│
├─► Navigation
├─► Header
├─► Features
├─► About
├─► Services
├─► Gallery
├─► Testimonials
├─► Team
└─► Contact
```

This unidirectional data flow ensures that the UI remains consistent with the application state and simplifies debugging and maintenance.