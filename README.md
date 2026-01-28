# La Calka Expense Report System

Professional expense tracking and cost analysis application for restaurant management.

## ✨ Features

### Core Functionality
- 📊 **Cost Analysis** - Real-time expense tracking and variance calculation
- 💰 **Inventory Management** - Track initial, purchases, final values with automatic usage calculation
- 📄 **Invoice Tracking** - Manage supplier invoices and purchases
- 📦 **Weekly Orders** - Plan and track weekly supply orders
- 🍺 **Bar Inventory** - Specialized tracking for bar, glassware, and dishes
- 🌍 **Bilingual** - Full Spanish and English language support

### New Features (2026 Update)
- ✅ **Fixed Calculation Bug** - Corrected negative number handling in totals
- 📅 **2026 Calendar Support** - Full support for 2026 dates with validation
- ↺ **Reset Button** - Clear all week data with confirmation dialog
- 🔍 **Date Navigation** - Jump to specific dates (e.g., January 15, 2026)
- ⬇ **Data Export** - Download backup as JSON file
- 🛡️ **Delete Confirmations** - Prevent accidental data loss
- 💾 **Auto-save** - Data persists in browser localStorage

## 🚀 Quick Start

### Option 1: Open Directly
1. Open `lacalka.html` in your web browser
2. Start entering expense data
3. Click "Guardar" (Save) to save your work

### Option 2: Deploy to Netlify (Recommended for Production)

#### Method A: Drag & Drop (Fastest)
1. Visit https://app.netlify.com/drop
2. Drag and drop `lacalka.html` file
3. Get instant public URL
4. Share the URL with your team

#### Method B: Netlify CLI
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy
cd "/Users/luis_ticas/Documents/expense reports"
netlify deploy --prod
```

#### Method C: Git Integration (Best for Updates)
1. Create GitHub repository
2. Push files to GitHub:
   ```bash
   git init
   git add lacalka.html README.md
   git commit -m "Initial commit: La Calka Expense Reports"
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
3. Connect repository to Netlify
4. Auto-deploy on every commit

### Alternative Deployment Options

#### Vercel
```bash
npm install -g vercel
vercel login
vercel deploy
```

#### Firebase Hosting
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

## 📖 User Guide

### Creating a New Week
1. Click **"+ Nueva Semana"** (New Week)
2. Enter week number (e.g., 3)
3. Enter start date (e.g., LUNES 20 ENERO 2026)
4. Date will be validated automatically
5. All fields cleared for new week entry

### Navigating to Specific Date
1. Click **📅 "Ir a Fecha"** (Go to Date)
2. Enter date to search (e.g., LUNES 15 ENERO 2026)
3. If week exists, it will be loaded automatically

### Resetting Current Week
1. Click **↺ "Restablecer"** (Reset)
2. Confirm the action
3. All fields will be cleared to $0.00
4. Totals automatically recalculated

### Exporting Data
1. Click **⬇ "Exportar"** (Export)
2. JSON backup file downloads automatically
3. Filename includes date: `lacalka-backup-2026-01-20.json`
4. Store backup files for data recovery

### Deleting Entries
1. Click ✕ delete button on any row
2. Confirmation dialog appears
3. Confirm or cancel deletion
4. Totals automatically recalculated

## 🔧 Technical Details

### Data Storage
- **Location**: Browser localStorage
- **Capacity**: 5-10MB (sufficient for 1000+ weeks)
- **Persistence**: Data survives browser restarts
- **Sync**: Single device only (no cloud sync)
- **Backup**: Manual export to JSON files

### Calculation Formula
The expense tracking uses this formula for inventory variance:
```
Usage/Variance = Initial + Purchases - Final
```

**Example:**
- Initial inventory: $6,184.24
- Purchases: $4,929.31
- Final inventory: $3,083.76
- **Usage: $8,029.79** (amount consumed/used)

Negative values (shown in red) indicate inventory shrinkage or accounting discrepancies.

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

### File Structure
```
lacalka.html (566.7KB → 3,809 lines)
├── HTML Structure
├── Embedded CSS Styles
├── JavaScript Logic
│   ├── Calculation functions
│   ├── Data storage (localStorage)
│   ├── Language support (ES/EN)
│   ├── Date validation
│   └── Export/import handlers
└── Translations (Spanish/English)
```

## 🎯 Usage Tips

### Best Practices
1. **Save frequently** - Click "Guardar" after major changes
2. **Export weekly** - Backup data every week
3. **Use date validation** - Follow format: DAY DATE MONTH YEAR
4. **Check calculations** - Verify totals after bulk entry
5. **Name weeks clearly** - Use consistent date format

### Common Issues

#### Data not saving?
- Check browser localStorage is enabled
- Clear browser cache if full
- Try different browser
- Export data before troubleshooting

#### Calculations incorrect?
- Verify all number inputs are valid
- Check for negative values (shown in red)
- Formula: Initial + Purchases - Final = Usage
- Click reset and re-enter if needed

#### Can't find a week?
- Use "📅 Ir a Fecha" button to search
- Check week dropdown for all saved weeks
- Verify date format matches saved format
- Export data to review all weeks in JSON

#### Delete by accident?
- No undo functionality (by design)
- Restore from exported JSON backup
- Use confirmation dialogs carefully
- Consider exporting before bulk deletions

## 🔐 Security & Privacy

- ✅ **No server** - All data stored locally in browser
- ✅ **No tracking** - No analytics or user tracking
- ✅ **No login required** - No authentication needed
- ✅ **Offline-first** - Works without internet connection
- ✅ **Private** - Data never leaves your device
- ⚠️ **Backup responsibility** - Export data regularly

## 📝 Changelog

### Version 2.0 (January 2026)
- ✅ Fixed regex parsing bug for negative numbers
- ✅ Added 2026 calendar support with validation
- ✅ Added reset button with confirmation
- ✅ Added date navigation feature
- ✅ Added data export functionality
- ✅ Added delete confirmations
- ✅ Improved translation system for custom buttons
- ✅ Updated default week to January 2026
- ✅ Added comprehensive date validation (2025-2030)

### Version 1.0 (September 2025)
- Initial release with core features

## 🚨 Important Notes

### Data Persistence
- Data stored in **browser localStorage** only
- Clearing browser data = **permanent data loss**
- **Export backups regularly** to prevent data loss
- No automatic cloud backup or sync

### Year Support
- **Supported years**: 2025-2030
- Date validation enforces year range
- Update validation function for years beyond 2030

### Production Deployment
- **No database required** - localStorage sufficient
- **Free hosting** - Netlify, Vercel, GitHub Pages
- **No server costs** - Static HTML file
- **Instant deployment** - Drag and drop ready

## 🤝 Support

For issues or questions:
1. Check this README for common issues
2. Verify browser compatibility
3. Try exporting and inspecting JSON data
4. Test in different browser
5. Check browser console for errors

## 📄 License

This is a custom business application for La Calka restaurant.

---

**Last Updated**: January 27, 2026
**Version**: 2.0
**File Size**: 566.7KB
**Lines of Code**: 3,809
