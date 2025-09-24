# 📈 IDX Stock Analysis & Investment Dashboard

**Comprehensive Indonesian Stock Exchange (IDX) analysis toolkit featuring advanced technical indicators, risk-return optimization, and executive-level investment recommendations with automated dashboard generation.**

![Executive Dashboard](images/IDX_Executive_Dashboard_Example.png)

## 🎯 Project Overview

Professional-grade stock analysis system that provides institutional-quality investment insights for Indonesian equities. This project combines quantitative analysis, technical indicators, and portfolio optimization to deliver actionable investment recommendations.

### Key Features
- **Multi-Stock Comparative Analysis** - Side-by-side performance evaluation
- **Technical Indicators** - RSI, Moving Averages, Trend Analysis
- **Risk-Return Optimization** - Sharpe ratio calculations and portfolio allocation
- **Executive Dashboard** - Automated generation of presentation-ready visualizations
- **Investment Scoring System** - Quantitative recommendation engine
- **Real-time Market Data Integration** - Dynamic data processing pipeline

## 📊 Analysis Components

### 1. Performance Analytics
- **Price Movement Analysis** - Period returns and volatility metrics
- **Relative Performance** - Normalized price comparisons
- **Risk-Adjusted Returns** - Sharpe ratio calculations
- **Volatility Regime Classification** - Market condition assessment

### 2. Technical Analysis
- **Moving Averages** - 20-day and 50-day trend indicators
- **RSI (Relative Strength Index)** - Momentum oscillator with overbought/oversold signals
- **Trend Classification** - Multi-level trend strength assessment
- **Support/Resistance Levels** - Key price level identification

### 3. Investment Scoring
- **Quantitative Scoring Model** - 5-point investment attractiveness scale
- **Multi-Factor Analysis** - Trend, momentum, risk, and return integration
- **Automated Recommendations** - Data-driven buy/hold/sell signals
- **Portfolio Allocation** - Score-weighted position sizing

### 4. Executive Dashboard
- **8-Panel Visualization Suite** - Comprehensive analytical overview
- **Performance Matrix** - Risk vs return scatter plot analysis
- **Recommendation Table** - Executive summary with actionable insights
- **Portfolio Allocation Chart** - Optimized investment distribution

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
Jupyter Notebook/Lab
Financial data source (Yahoo Finance, Bloomberg, etc.)
```

### Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn yfinance
```

### Installation
```bash
git clone https://github.com/yourusername/idx-stock-analysis.git
cd idx-stock-analysis
pip install -r requirements.txt
jupyter notebook
```

## 📁 Project Structure

```
idx-stock-analysis/
├── notebooks/
│   ├── data_collection.ipynb           # Market data acquisition
│   ├── technical_analysis.ipynb        # Technical indicators calculation
│   ├── portfolio_optimization.ipynb    # Risk-return analysis
│   └── executive_dashboard.ipynb       # Dashboard generation
├── data/
│   ├── raw/                           # Original market data
│   ├── processed/                     # Clean, processed datasets
│   └── external/                      # External market data
├── images/
│   ├── IDX_Executive_Dashboard_*.png  # Generated dashboards
│   ├── performance_analysis.png       # Individual analysis charts
│   └── technical_indicators.png       # Technical analysis visualizations
├── src/
│   ├── data_processor.py              # Data cleaning utilities
│   ├── technical_indicators.py        # Technical analysis functions
│   ├── portfolio_optimizer.py         # Portfolio optimization algorithms
│   └── dashboard_generator.py         # Automated dashboard creation
├── config/
│   └── analysis_config.yaml          # Analysis parameters
├── README.md
├── requirements.txt
└── .gitignore
```

## 📊 Sample Analysis Results

### Executive Dashboard Components

#### 1. Performance Overview
![Performance Chart](images/performance_overview.png)
- Period returns across all analyzed stocks
- Comparative performance ranking
- Risk-adjusted return metrics

#### 2. Risk-Return Matrix
![Risk Return Matrix](images/risk_return_matrix.png)
- Annual return vs volatility positioning
- Efficient frontier identification
- Stock positioning analysis

#### 3. Technical Indicators Dashboard
![Technical Analysis](images/technical_indicators.png)
- RSI levels with overbought/oversold zones
- Moving average trend analysis
- Momentum indicator signals

#### 4. Investment Recommendations
![Investment Table](images/investment_recommendations.png)
- Quantitative scoring results
- Buy/Hold/Sell recommendations
- Portfolio allocation suggestions

## 🔧 Technical Implementation

### Data Processing Pipeline
```python
# Market data collection and preprocessing
stock_data = fetch_market_data(symbols=['BBCA', 'BMRI', 'TLKM'])
cleaned_data = preprocess_stock_data(stock_data)
```

### Technical Indicator Calculations
```python
# RSI calculation
def calculate_rsi(prices, period=14):
    delta = prices.diff()
    gain = delta.where(delta > 0, 0).rolling(window=period).mean()
    loss = (-delta.where(delta < 0, 0)).rolling(window=period).mean()
    rs = gain / loss
    rsi = 100 - (100 / (1 + rs))
    return rsi
```

### Investment Scoring Algorithm
```python
# Multi-factor scoring system
def calculate_investment_score(stock_data):
    score = 0
    if trend_strength > threshold: score += 2
    if rsi_level < 70: score += 1  # Not overbought
    if sharpe_ratio > 0.5: score += 1
    if annual_return > benchmark: score += 1
    return min(score, 5)  # Cap at 5
```

## 📈 Analysis Methodology

### 1. Data Collection
- **Market Data Sources** - Multiple data provider integration
- **Data Quality Checks** - Missing value handling and outlier detection
- **Frequency Management** - Daily, weekly, monthly analysis options

### 2. Technical Analysis
- **Trend Analysis** - Multi-timeframe trend identification
- **Momentum Indicators** - RSI, MACD, Stochastic calculations
- **Volume Analysis** - Trading volume pattern recognition
- **Price Patterns** - Support/resistance level identification

### 3. Risk Management
- **Volatility Metrics** - Historical and implied volatility analysis
- **Value at Risk (VaR)** - Portfolio risk quantification
- **Correlation Analysis** - Inter-stock relationship assessment
- **Regime Detection** - Market condition classification

### 4. Portfolio Optimization
- **Mean Reversion Strategy** - Statistical arbitrage opportunities
- **Momentum Strategy** - Trend-following position sizing
- **Risk Parity** - Volatility-weighted allocation
- **Black-Litterman Model** - Bayesian portfolio construction

## 📊 Key Performance Indicators

### Risk Metrics
- **Annual Volatility** - Standard deviation of returns
- **Maximum Drawdown** - Peak-to-trough decline analysis
- **Sharpe Ratio** - Risk-adjusted return measurement
- **Beta Coefficient** - Market sensitivity analysis

### Return Metrics
- **Total Return** - Price appreciation + dividends
- **Annual Return** - Annualized performance calculation
- **Alpha Generation** - Excess return vs benchmark
- **Information Ratio** - Active return per unit of active risk

### Technical Metrics
- **RSI Levels** - Current momentum status
- **Moving Average Position** - Trend confirmation signals
- **Volume Indicators** - Accumulation/distribution patterns
- **Volatility Regime** - Current market condition classification

## 🎯 Investment Framework

### Scoring Methodology
```
Score Components (Max 5 points):
├── Trend Analysis (0-2 points)
│   ├── Strong Uptrend: 2 points
│   ├── Uptrend: 1 point
│   └── Sideways/Down: 0 points
├── Technical Indicators (0-1 point)
│   └── RSI < 70 (not overbought): 1 point
├── Risk-Adjusted Return (0-1 point)
│   └── Sharpe Ratio > 0.5: 1 point
└── Absolute Performance (0-1 point)
    └── Annual Return > 5%: 1 point
```

### Recommendation Framework
- **Score 4-5**: Strong Buy - High conviction positions
- **Score 3**: Buy - Attractive investment opportunity  
- **Score 2**: Hold - Neutral position, monitor closely
- **Score 0-1**: Cautious - High risk, careful evaluation needed

## 🚀 Advanced Features

### Automated Dashboard Generation
- **Scheduled Updates** - Daily/weekly dashboard refresh
- **Custom Branding** - Corporate presentation templates
- **Multi-Format Export** - PNG, PDF, HTML outputs
- **Email Integration** - Automated report distribution

### Backtesting Engine
- **Historical Performance** - Strategy validation across time periods
- **Walk-Forward Analysis** - Out-of-sample testing methodology
- **Monte Carlo Simulation** - Scenario analysis and stress testing
- **Performance Attribution** - Factor-based return decomposition

### API Integration
- **Real-Time Data** - Live market data feeds
- **News Sentiment** - Natural language processing integration
- **Economic Indicators** - Macro factor incorporation
- **Alternative Data** - Social media, satellite, web scraping

## 📋 Usage Examples

### Basic Analysis
```python
# Load and analyze stock data
from src.stock_analyzer import StockAnalyzer

analyzer = StockAnalyzer(['BBCA', 'BMRI', 'TLKM'])
analyzer.load_data(start_date='2023-01-01')
analyzer.calculate_indicators()
analyzer.generate_dashboard()
```

### Custom Portfolio Analysis
```python
# Custom portfolio with weights
portfolio = {
    'BBCA': 0.4,  # 40% allocation
    'BMRI': 0.35, # 35% allocation  
    'TLKM': 0.25  # 25% allocation
}

analyzer.analyze_portfolio(portfolio)
analyzer.optimize_allocation()
```

### Advanced Technical Analysis
```python
# Multi-timeframe analysis
analyzer.calculate_indicators(periods=[14, 30, 50])
analyzer.identify_patterns()
analyzer.generate_signals()
```

## ⚠️ Important Disclaimers

### Investment Risk Warning
- **Past Performance**: Historical results do not guarantee future returns
- **Market Risk**: All investments carry risk of principal loss
- **Model Limitations**: Quantitative models have inherent limitations
- **Professional Advice**: Consult licensed financial advisors

### Technical Limitations
- **Data Accuracy**: Results depend on data quality and availability
- **Model Assumptions**: Statistical models make simplifying assumptions
- **Market Conditions**: Analysis may not account for extraordinary events
- **Execution Risk**: Theoretical returns may differ from actual trading results

## 🤝 Contributing

### Development Guidelines
1. **Code Standards** - Follow PEP 8 style guidelines
2. **Testing** - Include unit tests for all new functions
3. **Documentation** - Update README for new features
4. **Performance** - Optimize for large dataset processing

### Contribution Process
```bash
git checkout -b feature/new-indicator
# Make your changes
git commit -m "Add new technical indicator"
git push origin feature/new-indicator
# Open Pull Request
```

## 📜 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## 📞 Support & Contact

- **Technical Issues**: Create GitHub Issue
- **Feature Requests**: Use GitHub Discussions
- **Collaboration**: Email for partnership inquiries

---

**⚠️ INVESTMENT DISCLAIMER**: This tool is for educational and research purposes only. It does not constitute investment advice, recommendation, or solicitation. Trading stocks involves substantial risk and may result in loss of capital. Always conduct your own research and consult with qualified financial professionals before making investment decisions.

**Built for Indonesian Capital Markets Analysis** 🇮🇩📊