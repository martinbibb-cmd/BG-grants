# BG Grant Finder - Progressive Web App

A mobile-first Progressive Web App (PWA) that helps users quickly determine their eligibility for British Gas support schemes through a simple 7-question questionnaire.

## Features

- **Quick Eligibility Assessment** - 7-question questionnaire takes under 2 minutes to complete
- **Comprehensive Coverage** - Evaluates eligibility for all 6 British Gas support schemes:
  - British Gas Energy Trust (BGET)
  - LEAP Emergency Boiler Replacement
  - LEAP Energy Advice Service
  - Help4Homes
  - ECO4 Scheme
  - Great British Insulation Scheme (GBIS)
- **Smart Eligibility Logic** - Accurately matches user circumstances to scheme requirements
- **Mobile-Optimized Design** - British Gas brand colors and responsive layout
- **Progressive Web App** - Works offline and can be installed to home screen
- **Clear Results** - Shows eligible schemes first with direct application links
- **User-Friendly** - Progress indicator, back/next navigation, and helpful explanations

## Grant Schemes Covered

### 1. British Gas Energy Trust (BGET)
- Grants to clear energy debt (£250-£1,500)
- Requires money advice before applying

### 2. LEAP - Emergency Boiler Replacement
- Free boiler replacement for no-heat emergencies
- For homeowners on benefits with vulnerable household members

### 3. LEAP - Energy Advice Service
- Free energy and money-saving advice
- Available to those on benefits or income under £31,000

### 4. Help4Homes
- Comprehensive energy support
- Includes insulation, solar PV, boilers, and white goods

### 5. ECO4 Scheme
- Home improvement measures including insulation and heat pumps
- For homeowners on benefits with EPC D or lower

### 6. Great British Insulation Scheme (GBIS)
- Single insulation measures
- Based on EPC rating and council tax band

## Technology Stack

- **Pure HTML/CSS/JavaScript** - No frameworks or dependencies required
- **Service Worker** - Enables offline functionality
- **Web Manifest** - Allows installation as PWA
- **Responsive Design** - Mobile-first approach with modern CSS

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A web server (for testing PWA features)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/martinbibb-cmd/BG-grants.git
   cd BG-grants
   ```

2. **Serve the files using a local web server:**

   Using Python 3:
   ```bash
   python -m http.server 8000
   ```

   Using Node.js (with npx):
   ```bash
   npx serve
   ```

   Using PHP:
   ```bash
   php -S localhost:8000
   ```

3. **Open in your browser:**
   ```
   http://localhost:8000
   ```

### PWA Installation

When accessing the app via HTTPS or localhost:
1. Look for the install prompt at the top of the page
2. Click "Install" to add the app to your home screen
3. The app will work offline after installation

**Note:** PWA features (offline mode, install prompt) require HTTPS in production or localhost for testing.

## File Structure

```
BG-grants/
├── index.html          # Main application file
├── manifest.json       # PWA manifest
├── sw.js              # Service worker for offline functionality
├── README.md          # This file
└── (icon files needed):
    ├── icon-192.png   # 192x192px app icon
    └── icon-512.png   # 512x512px app icon
```

## Missing Assets

The app references two icon files that need to be created:
- `icon-192.png` (192x192 pixels)
- `icon-512.png` (512x512 pixels)

These should use British Gas brand colors (primary: #0066CC) and include a recognizable icon or logo.

## Questionnaire Flow

1. **Support Type** - What kind of help the user needs
2. **Home Ownership** - Owner, private tenant, or social tenant
3. **Benefits** - Which means-tested benefits they receive
4. **Household Income** - Annual income amount
5. **Household Composition** - Vulnerable members, children, etc.
6. **Energy Debt** - Current debt amount
7. **Property Info** - EPC rating and council tax band

## Eligibility Logic

The app uses specific criteria for each scheme:

- **BGET:** Debt £250-£1,500 + income/household criteria
- **LEAP Boiler:** Emergency + homeowner + benefits + vulnerable member
- **LEAP Advice:** Benefits OR income < £31,000
- **Help4Homes:** Benefits OR prepayment meter OR high debt ratio
- **ECO4:** Homeowner + benefits + EPC D-G
- **GBIS:** EPC D-G + council tax band A-D/E

## Deployment

### GitHub Pages
1. Enable GitHub Pages in repository settings
2. Select the main branch as source
3. Access via `https://yourusername.github.io/BG-grants/`

### Custom Domain
1. Add a `CNAME` file with your domain name
2. Configure DNS settings with your domain provider
3. Enable HTTPS in GitHub Pages settings

### Other Hosting
Upload all files to any web server that supports HTTPS:
- Netlify
- Vercel
- Firebase Hosting
- AWS S3 + CloudFront

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is provided as-is for British Gas grant eligibility screening purposes.

## Contact

For questions about the grants themselves:
- Email: eco.referrals@britishgas.co.uk
- Visit: https://www.britishgas.co.uk

## Acknowledgments

- Scheme information based on official British Gas support programs
- Built as a user-friendly interface for grant eligibility screening
