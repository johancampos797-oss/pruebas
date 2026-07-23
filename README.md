# Sales Control Dashboard

A modern, responsive sales control dashboard built with React and Recharts.

## Features

- **Dashboard Overview**: Key metrics and KPIs at a glance
  - Total Sales
  - Orders Count
  - Revenue
  - Customers

- **Interactive Charts**:
  - Sales vs Target line chart
  - Revenue by Product bar chart
  - Responsive and mobile-friendly

- **Recent Activity**: Track recent sales and refunds

- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile

- **Modern UI**: Built with Tailwind CSS for a clean, professional look

## Tech Stack

- **React 18**: Frontend framework
- **Recharts**: Chart library for data visualization
- **Tailwind CSS**: Utility-first CSS framework
- **React Icons**: Icon library
- **Date-fns**: Date utility library
- **Axios**: HTTP client (ready for API integration)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/johancampos797-oss/pruebas.git
cd pruebas
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm start
```

The dashboard will open in your browser at `http://localhost:3000`

## Project Structure

```
src/
├── components/
│   ├── Header.js          # Top navigation bar
│   ├── Sidebar.js         # Left sidebar navigation
│   ├── MetricCard.js      # KPI metric card component
│   ├── SalesChart.js      # Chart visualization component
│   └── RecentActivity.js  # Recent activity list
├── pages/
│   └── DashboardHome.js   # Main dashboard page
├── App.js                 # Root component
├── index.js               # React entry point
└── index.css              # Global styles
```

## Features Breakdown

### Header Component
- Navigation toggle for mobile
- Notification bell with badge
- User profile menu

### Sidebar Component
- Navigation menu with icons
- Responsive toggle (hidden on mobile, visible on desktop)
- Menu items: Dashboard, Analytics, Sales, Settings

### Metric Cards
- Four color themes (blue, green, purple, orange)
- Trending indicators (up/down)
- Percentage change from previous month
- Icon support

### Sales Charts
- Line chart: Track sales performance vs targets
- Bar chart: Revenue breakdown by product
- Interactive tooltips
- Responsive sizing

### Recent Activity
- Transaction list with timestamps
- Color-coded transaction types (sales/refunds)
- Amount display
- Clean, scrollable layout

## Customization

### Update Sales Data
Edit the `salesData` array in `src/pages/DashboardHome.js` to reflect your actual sales data.

### Add API Integration
Update components to fetch data from your backend:

```javascript
import axios from 'axios';

useEffect(() => {
  axios.get('/api/sales').then(response => {
    setSalesData(response.data);
  });
}, []);
```

### Modify Colors
Update the color theme in `tailwind.config.js` or modify individual component styles.

## Available Scripts

- `npm start`: Run development server
- `npm build`: Create production build
- `npm test`: Run tests
- `npm eject`: Eject from Create React App (irreversible)

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - Feel free to use this dashboard in your projects!

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues and questions, please create an issue in the repository.
