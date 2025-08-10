# SIP-SWP-CALCULATOR
# 📊 SIP + SWP Calculator
https://sip-swp-calculator.netlify.app/ Live

A comprehensive financial planning tool that helps you calculate Systematic Investment Plan (SIP) accumulation and Systematic Withdrawal Plan (SWP) sustainability. Perfect for retirement planning, wealth creation, and generating regular income from investments.

## 🎯 What This Calculator Does

### SIP (Systematic Investment Plan) Phase
- **Calculate wealth accumulation** through regular monthly investments
- **Visualize the power of compounding** over long-term periods
- **Track total invested amount vs. returns** generated
- **Plan your wealth creation journey** with different scenarios

### SWP (Systematic Withdrawal Plan) Phase  
- **Determine sustainable withdrawal rates** from your accumulated corpus
- **Analyze multiple corpus scenarios** (₹50L, ₹75L, ₹1Cr, ₹1.25Cr, ₹1.5Cr)
- **Check sustainability** - will your money last throughout the withdrawal period?
- **Calculate annual withdrawal rates** as percentage of corpus

## 🚀 Live Demo
(https://sip-swp-calculator.netlify.app/)

## ✨ Key Features

### 📈 SIP Calculator
- **Monthly Investment Amount**: Set your regular SIP amount (minimum ₹1,000)
- **Investment Duration**: Choose investment period (1-40 years)
- **Expected Returns**: Set annual return rate (1-30%)
- **Real-time Calculations**: Instantly see maturity amount, total invested, and returns

### 📉 SWP Calculator  
- **Monthly Withdrawal**: Set your desired monthly income
- **Withdrawal Period**: Plan for 1-50 years of withdrawals
- **Conservative Returns**: Set expected returns during withdrawal phase
- **Sustainability Analysis**: Check if your corpus will last

### 📊 Advanced Analytics
- **Multiple Scenario Analysis**: Compare different corpus amounts
- **Sustainability Indicators**: Green checkmarks for sustainable plans
- **Annual Withdrawal Rates**: See what percentage you're withdrawing yearly
- **Visual Feedback**: Color-coded results for easy interpretation

## 🛠️ Technology Stack

- **Frontend Framework**: React 18.x with Hooks
- **Styling**: Tailwind CSS for responsive design
- **Icons**: Lucide React for beautiful iconography
- **Calculations**: JavaScript for complex financial computations
- **State Management**: React useState for real-time updates

## 📱 Responsive Design

- ✅ **Desktop**: Full-featured experience with side-by-side layout
- ✅ **Tablet**: Optimized grid layout for medium screens
- ✅ **Mobile**: Single-column responsive design for phones
- ✅ **Accessibility**: Proper contrast and semantic HTML

## 🔧 Installation & Setup

### Method 1: Simple HTML Deployment
```bash
# Clone the repository
git clone https://github.com/your-username/sip-swp-calculator.git
cd sip-swp-calculator

# Open index.html in your browser
open index.html
```

### Method 2: React Development Environment
```bash
# Create new React app
npx create-react-app sip-swp-calculator
cd sip-swp-calculator

# Install dependencies
npm install lucide-react

# Replace src/App.js with the calculator component
# Start development server
npm start
```

### Method 3: Next.js Setup
```bash
# Create Next.js app with Tailwind
npx create-next-app@latest sip-swp-calculator --tailwind --typescript
cd sip-swp-calculator

# Install dependencies
npm install lucide-react

# Add component and run
npm run dev
```

## 🚀 Deployment Options

### GitHub Pages (Free)
1. Push your code to GitHub repository
2. Go to Settings → Pages
3. Select "Deploy from a branch" → main → / (root)
4. Your site will be live at `https://username.github.io/repo-name`

### Netlify (Recommended)
1. Build your project: `npm run build`
2. Drag and drop `build` folder to [netlify.com](https://netlify.com)
3. Or connect GitHub repo for automatic deployments

### Vercel (Easy)
1. Push to GitHub
2. Import repository at [vercel.com](https://vercel.com)
3. Automatic deployment with every push

## 📊 How the Calculations Work

### SIP Formula
```javascript
// Monthly SIP calculation
const monthlyRate = annualRate / 100 / 12;
const months = years * 12;
const maturityAmount = monthlyAmount * 
    (((1 + monthlyRate) ** months - 1) / monthlyRate) * 
    (1 + monthlyRate);
```

### SWP Simulation
```javascript
// Month-by-month simulation
for (let month = 1; month <= totalMonths; month++) {
    balance = balance * (1 + monthlyRate) - withdrawalAmount;
    if (balance <= 0) break;
}
```

## 🎯 Use Cases

### 👨‍💼 Retirement Planning
- Calculate how much to invest monthly for retirement
- Determine sustainable withdrawal rate in retirement
- Plan for 20-30 years of post-retirement income

### 💰 Wealth Creation
- Set wealth targets (₹1 crore, ₹2 crore, etc.)
- Calculate required monthly SIP amounts
- Track progress with different return scenarios

### 📈 Financial Independence
- Calculate corpus needed for financial freedom
- Determine safe withdrawal rates (typically 4-8%)
- Plan transition from accumulation to withdrawal phase

### 🏠 Goal-Based Planning
- Children's education funding
- Wedding expense planning
- Emergency fund creation

## 💡 Financial Insights Built-In

### SIP Phase Benefits
- **Rupee Cost Averaging**: Reduces impact of market volatility
- **Power of Compounding**: Money grows exponentially over time
- **Disciplined Investing**: Regular investments build wealth systematically
- **Tax Benefits**: ELSS investments offer tax deductions

### SWP Phase Benefits
- **Regular Income**: Monthly cash flow while investments continue growing
- **Tax Efficiency**: Only capital gains taxed, not entire withdrawal
- **Flexibility**: Can adjust withdrawal amounts as needed
- **Inflation Protection**: Remaining corpus continues to grow

### Recommended Withdrawal Rates
- **Conservative**: 6-7% annually (sustainable for 25+ years)
- **Moderate**: 8-9% annually (good for 20-25 years)
- **Aggressive**: 10%+ annually (higher risk of corpus depletion)

## 🎨 Customization Options

### Color Themes
```css
/* Change primary colors in Tailwind classes */
.sip-section { @apply bg-green-50 text-green-800; }
.swp-section { @apply bg-orange-50 text-orange-800; }
.results-section { @apply bg-blue-50 text-blue-800; }
```

### Input Ranges
```javascript
// Modify input constraints
const sipAmountRange = { min: 1000, max: 500000, step: 1000 };
const tenureRange = { min: 1, max: 50 };
const returnRange = { min: 1, max: 30, step: 0.5 };
```

### Currency Formats
```javascript
// Indian Rupee formatting
const formatINR = (amount) => 
    new Intl.NumberFormat('en-IN', {
        style: 'currency',
        currency: 'INR',
        maximumFractionDigits: 0
    }).format(amount);
```

## 📈 Advanced Features

### Scenario Analysis
The calculator automatically tests 5 different corpus amounts:
- ₹50 Lakhs
- ₹75 Lakhs  
- ₹1 Crore
- ₹1.25 Crore
- ₹1.5 Crore

### Sustainability Indicators
- ✅ **Green Checkmark**: Corpus lasts entire withdrawal period
- ⚠️ **Red Warning**: Corpus gets depleted before end period

### Annual Withdrawal Rate Display
Shows what percentage of corpus you're withdrawing annually:
- **Safe Zone**: Under 8% annually
- **Caution Zone**: 8-12% annually  
- **Risk Zone**: Above 12% annually

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Bug Reports
1. Check existing issues first
2. Create detailed bug report with steps to reproduce
3. Include browser/device information

### Feature Requests
1. Describe the feature and its benefits
2. Provide mockups or examples if possible
3. Explain use cases

### Code Contributions
1. Fork the repository
2. Create feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open Pull Request

### Development Guidelines
```bash
# Code style
- Use meaningful variable names
- Add comments for complex calculations
- Follow React best practices
- Ensure mobile responsiveness

# Testing
- Test all input ranges
- Verify calculations manually
- Check responsive design
- Test browser compatibility
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 SIP + SWP Calculator

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

## 🙏 Acknowledgments

- **Financial Formulas**: Based on standard SIP/SWP mathematical models
- **UI Design**: Inspired by modern fintech applications
- **Icons**: Beautiful icons from [Lucide](https://lucide.dev)
- **Styling**: Powered by [Tailwind CSS](https://tailwindcss.com)

- 📊 Interactive charts and graphs
- 💾 Save/load calculation scenarios
- 📱 Progressive Web App (PWA) support
- 🌙 Dark mode theme
- 📈 Historical return data integration

---

**⭐ If this calculator helped you plan your financial future, please give it a star!**

**🔗 Share it with others who might benefit from better financial planning!**
