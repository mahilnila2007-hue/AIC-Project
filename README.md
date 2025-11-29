# Enhanced Data Viewer - AIC Project

A modern, feature-rich data visualization and analysis platform with interactive charts, real-time filtering, and advanced analytics capabilities.

![Data Viewer](https://img.shields.io/badge/Version-2.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-success)

## 🚀 Features

### Frontend Features
- **Interactive Dashboard** - Beautiful, responsive UI with modern design
- **Real-time Data Visualization** - Dynamic charts using Chart.js
  - Line charts for trend analysis
  - Pie charts for distribution
  - Bar charts for comparisons
- **Advanced Filtering** - Multi-criteria filtering and search
- **Data Management** - CRUD operations (Create, Read, Update, Delete)
- **Export Functionality** - Export data to JSON format
- **Dark/Light Theme** - Toggle between themes
- **Responsive Design** - Works on desktop, tablet, and mobile
- **Pagination** - Efficient data browsing
- **Sorting** - Sort by any column
- **Statistics Cards** - Real-time statistics display

### Backend Features (Python Flask API)
- **RESTful API** - Complete CRUD operations
- **Statistical Analysis** - Mean, median, standard deviation
- **Trend Analysis** - Time-based trend calculations
- **Category Analysis** - Detailed breakdown by categories
- **Forecasting** - Simple moving average forecasting
- **Advanced Search** - Multi-criteria search functionality
- **Data Export** - CSV and Excel export
- **Health Check** - API monitoring endpoint

## 📋 Prerequisites

### Frontend Only
- Modern web browser (Chrome, Firefox, Edge, Safari)

### Backend (Optional)
- Python 3.8 or higher
- pip (Python package manager)

## 🛠️ Installation

### Quick Start (Frontend Only)

1. Simply open `index.html` in your web browser
2. The application will load with sample data
3. Start exploring!

### Full Installation (with Backend)

1. **Clone or download the project files**

2. **Install Python dependencies:**
```powershell
pip install flask flask-cors pandas numpy openpyxl
```

3. **Start the backend server:**
```powershell
python backend.py
```

4. **Open the frontend:**
   - Open `index.html` in your browser
   - Or use a local server:
```powershell
python -m http.server 8000
```
   Then navigate to `http://localhost:8000`

## 📁 Project Structure

```
PROJECT/
│
├── index.html          # Main HTML file
├── styles.css          # Styling and themes
├── script.js           # Frontend JavaScript logic
├── backend.py          # Python Flask API server
├── requirements.txt    # Python dependencies
└── README.md          # This file
```

## 🎯 Usage Guide

### Loading Data
- Click **"Load Sample Data"** to generate 50 sample records
- Or use the API to load custom data

### Filtering Data
1. Use the **search box** to search across all fields
2. Use **category filter** to filter by category
3. Use **date filter** to filter by time period
4. Click **refresh** to reset all filters

### Managing Records
- **Add Record**: Click the "+ Add Record" button
- **Edit Record**: Click the edit icon on any row
- **Delete Record**: Click the delete icon or select multiple and use "Delete Selected"

### Viewing Analytics
- **Statistics Cards**: View total records, average value, max value, and last update time
- **Trend Chart**: Analyze value trends over time (switch between line, bar, area)
- **Distribution Chart**: See category distribution in pie chart format

### Exporting Data
- Click **"Export"** to download current data as JSON
- Use API endpoints for CSV/Excel export

### Changing Theme
- Click **"Theme"** button to toggle between light and dark modes

## 🔌 API Endpoints

### Data Operations
- `GET /api/data` - Retrieve all records
- `POST /api/data` - Add new record
- `PUT /api/data/<id>` - Update record
- `DELETE /api/data/<id>` - Delete record

### Analytics
- `GET /api/analytics/summary` - Get statistical summary
- `GET /api/analytics/trends` - Get trend analysis
- `GET /api/analytics/category` - Get category analysis
- `POST /api/analytics/forecast` - Generate forecast

### Export
- `GET /api/export/csv` - Export as CSV
- `GET /api/export/excel` - Export as Excel

### Utility
- `POST /api/search` - Advanced search
- `GET /api/health` - Health check

## 🎨 Customization

### Adding Custom Categories
Edit the categories array in `script.js`:
```javascript
const categories = ['sales', 'marketing', 'operations', 'finance', 'your-category'];
```

### Changing Colors
Modify CSS variables in `styles.css`:
```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    /* Add your colors */
}
```

### Adjusting Records Per Page
Change in `script.js`:
```javascript
let recordsPerPage = 10; // Change to your preferred number
```

## 📊 Sample Data Format

```json
{
  "id": 1,
  "category": "sales",
  "value": 5000,
  "date": "2025-11-15",
  "status": "Active"
}
```

## 🔧 Troubleshooting

### Charts not displaying
- Ensure you have internet connection (Chart.js loads from CDN)
- Check browser console for errors

### Backend not connecting
- Verify Python and all dependencies are installed
- Check that port 5000 is not in use
- Ensure Flask is running without errors

### Data not saving
- Frontend-only mode: Data is stored in memory (refreshing page will reset)
- With backend: Data persists in memory until server restart
- For persistent storage, integrate a database

## 🚀 Advanced Features

### Integrating with Database
Replace the `data_storage` list in `backend.py` with database operations:
- SQLite for simple projects
- PostgreSQL/MySQL for production
- MongoDB for NoSQL approach

### Adding Authentication
Implement user authentication using:
- Flask-Login
- JWT tokens
- OAuth2

### Real-time Updates
Add WebSocket support using:
- Flask-SocketIO
- Real-time chart updates
- Live collaboration features

## 📝 Technologies Used

### Frontend
- HTML5
- CSS3 (with CSS Grid and Flexbox)
- JavaScript (ES6+)
- Chart.js 4.4.0
- Font Awesome 6.4.0

### Backend
- Python 3.8+
- Flask
- Pandas
- NumPy
- OpenPyXL

## 🤝 Contributing

Feel free to enhance this project:
1. Add new chart types
2. Implement more analytics features
3. Add data import functionality
4. Improve mobile responsiveness
5. Add more export formats

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

Created for AIC Project - Enhanced Data Viewer
Version 2.0 - November 2025

## 🎓 Learning Resources

- [Chart.js Documentation](https://www.chartjs.org/docs/)
- [Flask Documentation](https://flask.palletsprojects.com/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [MDN Web Docs](https://developer.mozilla.org/)

## 📞 Support

For issues or questions:
1. Check the troubleshooting section
2. Review the code comments
3. Consult the API documentation
4. Test with sample data first

---

**Enjoy your Enhanced Data Viewer! 📊✨**
