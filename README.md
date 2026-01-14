
# 🎯 M4DI~UciH4 Auction Profile Indicator

<div align="center">

![Version](https://img.shields.io/badge/version-4.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-MetaTrader%205-orange.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

**Professional Auction Market Theory & Volume Profile System for MT5**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Screenshots](#-screenshots) • [Configuration](#%EF%B8%8F-configuration) • [Contributing](#-contributing)

</div>

---

## 📖 Overview

**M4DI~UciH4 Auction Profile** is a comprehensive technical indicator for MetaTrader 5 that implements advanced **Auction Market Theory (AMT)** and **Volume Profile Analysis**. This professional-grade tool helps traders identify key market structures, value areas, and high-probability trading opportunities based on institutional auction dynamics.

### 🎓 What is Auction Market Theory?

Auction Market Theory is a framework that views markets as continuous two-way auctions where price discovery occurs through the interaction of buyers and sellers. The indicator analyzes:

- **Value Area (VA)**: Price range where 70% of trading activity occurred
- **Point of Control (POC)**: Price level with highest trading volume
- **Initial Balance (IB)**: First hour's trading range
- **Market Profile**: Visual representation of price-time-volume relationship

---

## ✨ Features

### 📊 Core Components

#### 1. **Volume Profile Analysis**
- ✅ Real-time volume distribution across price levels
- ✅ High Volume Nodes (HVN) identification
- ✅ Low Volume Nodes (LVN) detection
- ✅ Composite profile tracking with decay factor
- ✅ Customizable price level resolution (up to 500 levels)

#### 2. **Value Area Calculation**
- ✅ Dynamic 70% value area computation
- ✅ Value Area High (VAH) and Low (VAL) levels
- ✅ Developing value area visualization
- ✅ Value area width analysis

#### 3. **Initial Balance (IB)**
- ✅ First 60-minute range tracking
- ✅ IB extension monitoring
- ✅ Wide/Narrow IB classification
- ✅ IB breakout detection with direction

#### 4. **VWAP Analysis**
- ✅ Volume-Weighted Average Price calculation
- ✅ Standard deviation bands (±1σ, ±2σ)
- ✅ Price deviation from VWAP
- ✅ Fair value acceptance/rejection signals

#### 5. **Auction Phase Detection**
- 🔵 **Balance**: Price rotating within value area
- 🟠 **Imbalance**: Directional movement developing
- 🟢 **Breakaway**: Strong momentum beyond value
- 🔴 **Test & Reject**: Failed auction attempt
- 🟢 **Test & Accept**: Successful value extension

#### 6. **Day Type Classification**
- 📅 **Normal Day**: Standard value area development
- 📅 **Neutral Day**: Tight range, no IB break
- 📅 **Trend Day**: Early IB break with continuation
- 📅 **Double Distribution**: Two distinct value areas
- 📅 **Closing Auction**: Late-day value shift

#### 7. **Profile Shape Recognition**
- 📐 **Normal Distribution**: Balanced bell curve
- 📐 **Trending Flat**: Directional with edge POC
- 📐 **Double Distribution**: Two peaks (bi-modal)
- 📐 **Neutral Inside**: Ranging consolidation

#### 8. **Market Participation Analysis**
- 💪 **Initiative**: Aggressive directional buyers/sellers
- 🛡️ **Responsive**: Counter-trend faders
- ⚖️ **Mixed**: Balanced participation

### 🎯 Trading Strategy System

#### Strategy 1: VA Fade
- **Logic**: Fade price extremes back to value area
- **Entry**: Price outside VAH/VAL
- **Exit**: POC target
- **Best For**: Range-bound markets, normal distributions

#### Strategy 2: POC Attraction
- **Logic**: Price gravitates toward point of control
- **Entry**: Significant distance from POC
- **Exit**: POC level
- **Best For**: Balanced auction phases

#### Strategy 3: VA Breakout
- **Logic**: Momentum continuation beyond value
- **Entry**: Breaking VAH/VAL with volume
- **Exit**: Previous VA width extension
- **Best For**: Trend days, breakaway auctions

### 📈 Visual Components

- **Volume Profile Histogram**: Horizontal volume bars with gradient coloring
- **Value Area Box**: 70% volume range highlight
- **POC Line**: Thick white line at volume peak
- **VAH/VAL Lines**: Blue dashed value boundaries
- **VWAP**: Gold line with deviation bands
- **Initial Balance**: Magenta range box
- **HVN Markers**: Green arrows at high volume nodes
- **LVN Markers**: Red arrows at low volume nodes
- **Strategy Signals**: Entry/SL/TP level markers

### 🖥️ Professional Dashboard

Real-time monitoring panel displaying:
- Day structure and type classification
- Initial balance status and range
- Volume profile metrics (POC, VA, height)
- Auction phase and direction
- VWAP deviation analysis
- Strategy matrix with confidence levels
- Overall market status

---

## 🚀 Installation

### Method 1: Direct Installation

1. **Download** the `M4DI_UciH4_Auction_Profile.mq5` file
2. **Copy** to your MetaTrader 5 directory:
   ```
   C:\Users\[YourName]\AppData\Roaming\MetaQuotes\Terminal\[TerminalID]\MQL5\Indicators\
   ```
3. **Restart** MetaTrader 5
4. **Compile** the indicator (F7 in MetaEditor) or use pre-compiled version
5. **Attach** to chart from Navigator → Indicators → Custom

### Method 2: Via MetaEditor

1. Open **MetaEditor** (F4 in MT5)
2. File → New → Indicator
3. Paste the source code
4. Click **Compile** (F7)
5. Indicator appears in Navigator

---

## 📚 Usage

### Basic Setup

1. **Attach to Chart**: Drag indicator to desired chart
2. **Select Timeframe**: Works on all timeframes (H1-H4 recommended)
3. **Configure Settings**: Adjust parameters via indicator settings
4. **Wait for Development**: Profile develops over 24+ bars

### Recommended Settings by Instrument

#### Forex Pairs (EUR/USD, GBP/USD, etc.)
```
Profile Bars: 100
Price Levels: 200
VA Percentage: 70%
IB Minutes: 60
```

#### Stock Indices (S&P500, NASDAQ)
```
Profile Bars: 150
Price Levels: 250
VA Percentage: 70%
IB Minutes: 60
```

#### Commodities (Gold, Oil)
```
Profile Bars: 80
Price Levels: 150
VA Percentage: 68%
IB Minutes: 60
```

### Trading Workflow

#### 1. **Morning Analysis** (Market Open)
   - Identify yesterday's POC and value area
   - Note overnight price action relative to value
   - Wait for Initial Balance to form (first 60 min)

#### 2. **IB Formation** (First Hour)
   - Monitor IB high/low development
   - Classify as Wide/Narrow relative to ATR
   - Prepare for potential IB breakout

#### 3. **Midday Trading** (2-6 hours post-open)
   - Watch for IB breaks (trend day potential)
   - Trade VA fades in balanced markets
   - Use POC as magnet for mean reversion

#### 4. **Afternoon Session** (Last 3 hours)
   - Monitor value area acceptance/rejection
   - Look for closing auction patterns
   - Set alerts at key profile levels

---

## ⚙️ Configuration

### Auction Profile Settings

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| `InpProfileBars` | 100 | 20-500 | Lookback period for profile calculation |
| `InpPriceLevels` | 200 | 50-500 | Price level resolution (higher = more detail) |
| `InpVAPercent` | 70.0 | 60-80 | Value area percentage (70% standard) |
| `InpShowComposite` | true | bool | Display composite profile across sessions |
| `InpShowDeveloping` | true | bool | Show developing value area in real-time |

### Initial Balance Settings

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| `InpIBMinutes` | 60 | 30-120 | IB period in minutes (60 = first hour) |
| `InpIBWideMultiplier` | 1.5 | 1.0-3.0 | ATR multiple for "wide IB" classification |
| `InpIBNarrowMultiplier` | 0.7 | 0.3-1.0 | ATR multiple for "narrow IB" classification |
| `InpShowIB` | true | bool | Display IB levels on chart |

### VWAP Settings

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| `InpShowVWAP` | true | bool | Display VWAP line |
| `InpShowVWAPBands` | true | bool | Show standard deviation bands |
| `InpVWAPBandMult` | 2 | 1-3 | Std dev multiplier (1=68%, 2=95%, 3=99.7%) |

### Strategy Settings

| Parameter | Default | Range | Description |
|-----------|---------|-------|-------------|
| `InpEnableVAFade` | true | bool | Enable VA fade strategy signals |
| `InpEnablePOCAttract` | true | bool | Enable POC attraction signals |
| `InpEnableVABreakout` | true | bool | Enable VA breakout signals |
| `InpMinConfidence` | 60.0 | 0-100 | Minimum confidence % for signal display |

### Visual Settings

| Parameter | Default | Description |
|-----------|---------|-------------|
| `InpShowDashboard` | true | Display information dashboard |
| `InpShowProfile` | true | Show volume profile histogram |
| `InpShowHeatmap` | true | Volume heatmap coloring |
| `InpPOCColor` | White | Point of Control color |
| `InpVAHColor` | DodgerBlue | Value Area High color |
| `InpVALColor` | DodgerBlue | Value Area Low color |
| `InpVWAPColor` | Gold | VWAP line color |
| `InpBullColor` | Lime | Bullish signal color |
| `InpBearColor` | Red | Bearish signal color |
| `InpDashboardX` | 20 | Dashboard X position (pixels) |
| `InpDashboardY` | 50 | Dashboard Y position (pixels) |

### Session Times (GMT)

| Session | Start (Default) | End (Default) |
|---------|----------------|---------------|
| Asian | 0 | 8 |
| London | 8 | 16 |
| New York | 13 | 21 |

**Note**: Adjust session times based on your broker's timezone and DST settings.

---

## 📊 Understanding the Dashboard

### Dashboard Layout

```
═══ M4DI~UciH4 AUCTION PROFILE ═══
github.com/RizkyEvory

▬▬▬ DAY STRUCTURE ▬▬▬
◎ Day Type: TREND
◎ Initial Balance: 1.0850 - 1.0890
◎ IB Status: BROKEN UP

▬▬▬ VOLUME PROFILE ▬▬▬
◎ POC: 1.0870 | Vol: 15.2K
◎ VA Range: 1.0860 - 1.0895
◎ VA Height: 35.0 pips
◎ Profile Shape: TRENDING

▬▬▬ AUCTION PHASE ▬▬▬
◎ Current: BREAKAWAY
◎ Direction: UP ▲
◎ Participation: INITIATIVE

▬▬▬ VWAP ANALYSIS ▬▬▬
◎ Price vs VWAP: +0.45%
◎ VWAP SD: ±1: 1.0875
◎ Fair Value: REJECTED

▬▬▬ STRATEGY MATRIX ▬▬▬
◎ VA Fade: INACTIVE Conf: 35%
◎ POC Attraction: INACTIVE Conf: 42%
◎ VA Breakout: ACTIVE Conf: 78%

═══ STATUS: BREAKING ═══
```

### Status Indicators

| Status | Color | Meaning |
|--------|-------|---------|
| BALANCED | Yellow | Price rotating in value |
| IMBALANCED | Orange | Directional bias forming |
| BREAKING | Lime | Strong momentum phase |

---

## 🎨 Color Coding

### Volume Profile Histogram

| Color | Volume Level | Significance |
|-------|-------------|--------------|
| White | 80-100% | Maximum volume (POC area) |
| Dodger Blue | 60-80% | High volume |
| Royal Blue | 40-60% | Above average |
| Medium Blue | 20-40% | Below average |
| Dark Blue | 0-20% | Low volume (potential LVN) |

### Auction Phase Colors

| Phase | Color | Trading Implication |
|-------|-------|---------------------|
| Balance | Yellow | Range-bound, fade extremes |
| Imbalance | Orange | Directional bias developing |
| Breakaway | Lime | Trend continuation likely |
| Test & Reject | Red | Failed breakout, reversal |
| Test & Accept | Green | New value area forming |

---

## 📖 Trading Examples

### Example 1: VA Fade Trade

**Setup**:
- Day Type: Normal
- Profile Shape: Normal Distribution
- Auction Phase: Balance
- Price: Above VAH

**Signal**:
```
◎ VA Fade: ACTIVE Conf: 82%
Entry: 1.0920 (current price above VAH 1.0895)
Stop Loss: 1.0935 (above resistance)
Take Profit: 1.0870 (POC)
Risk/Reward: 1:3.3
```

**Trade Management**:
1. Enter short at 1.0920
2. Initial stop at 1.0935 (15 pips)
3. Target POC at 1.0870 (50 pips)
4. Move stop to breakeven at +20 pips
5. Take 50% profit at VAL, let rest run to POC

---

### Example 2: POC Attraction Trade

**Setup**:
- Price: Below value area
- Distance to POC: 45 pips (significant)
- Auction Phase: Imbalance
- Participation: Mixed

**Signal**:
```
◎ POC Attraction: ACTIVE Conf: 71%
Entry: 1.0825 (below VAL)
Stop Loss: 1.0800 (recent swing low)
Take Profit: 1.0870 (POC magnet)
Risk/Reward: 1:1.8
```

**Trade Management**:
1. Enter long at 1.0825
2. Stop below structure at 1.0800 (25 pips)
3. First target: VAL at 1.0860 (35 pips)
4. Final target: POC at 1.0870 (45 pips)
5. Trail stop using VWAP as support

---

### Example 3: VA Breakout Trade

**Setup**:
- Day Type: Trend
- IB Status: Broken early
- Profile Shape: Trending Flat
- Auction Phase: Breakaway
- Participation: Initiative

**Signal**:
```
◎ VA Breakout: ACTIVE Conf: 85%
Entry: 1.0900 (breaking VAH 1.0895)
Stop Loss: 1.0870 (POC support)
Take Profit: 1.0935 (VA height extension)
Risk/Reward: 1:1.2
```

**Trade Management**:
1. Enter long on VAH break with volume
2. Stop at POC (30 pips)
3. Target: Previous VA height above breakout
4. Add to position on pullback to broken VAH
5. Trail using 20 EMA or VWAP

---

## 🔧 Advanced Features

### 1. **Composite Profile Decay**
The indicator maintains a composite profile with a 0.95 decay factor, giving more weight to recent sessions while preserving historical context.

### 2. **Dynamic Position Sizing**
Built-in position size calculator based on:
- Strategy type (VA Fade, POC Attraction, Breakout)
- Distance to POC
- Profile development stage
- Account risk parameters

### 3. **Session Analysis**
Tracks separate profiles for:
- Asian Session (00:00-08:00 GMT)
- London Session (08:00-16:00 GMT)
- New York Session (13:00-21:00 GMT)

### 4. **Volume Delta Calculation**
Proprietary algorithm estimates buying vs selling pressure based on bar close position within range.

### 5. **Smart HVN/LVN Detection**
Automatically identifies:
- **HVN**: Volume > 1.5x average with local peaks
- **LVN**: Volume < 0.5x average with local valleys

### 6. **Profile Development Validation**
Ensures profile reliability by requiring:
- Minimum 24 bars of data
- Positive total volume
- Valid value area height
- Complete price range coverage

---

## 📈 Performance Optimization

### Resource Management

- **Buffer Management**: Uses 12 indicator buffers efficiently
- **Object Cleanup**: Automatic deletion of old profile objects
- **Calculation Optimization**: Processes only necessary bars
- **Memory Efficient**: Minimal array allocations

### Best Practices

1. **Timeframe Selection**:
   - H1-H4: Best for intraday profiles
   - D1: Weekly/monthly composite analysis
   - M15-M30: Scalping with developing profiles

2. **Profile Bars Setting**:
   - Lower (50-75): Faster calculations, recent focus
   - Medium (100-150): Balanced view
   - Higher (200+): Deep history, slower updates

3. **Price Levels**:
   - 100-150: Smooth profiles, less detail
   - 200-250: Standard resolution
   - 300-500: High detail, more computation

---

## 🐛 Troubleshooting

### Common Issues

#### Profile Not Displaying
- **Cause**: Insufficient bars loaded
- **Solution**: Increase chart history (Tools → Options → Charts → Max bars in chart)

#### Dashboard Position Off-Screen
- **Solution**: Reset `InpDashboardX` and `InpDashboardY` to default (20, 50)

#### No Strategy Signals
- **Cause**: Confidence below threshold
- **Solution**: Lower `InpMinConfidence` or wait for better setups

#### ATR Handle Error
- **Cause**: Insufficient price data
- **Solution**: Load more historical data or restart MT5

#### Profile Jumps on New Day
- **Expected Behavior**: Profile resets at 00:00 GMT
- **Solution**: Use composite profile for continuity

---

## 🔬 Technical Details

### Calculation Methods

#### Value Area Algorithm
```
1. Calculate total volume across all price levels
2. Find POC (price level with maximum volume)
3. Start with POC volume
4. Expand up/down alternately, choosing higher volume side
5. Continue until 70% of total volume included
6. VAH = highest price in area, VAL = lowest
```

#### VWAP Formula
```
VWAP = Σ(Typical Price × Volume) / Σ(Volume)
Typical Price = (High + Low + Close) / 3
StdDev = √(Σ(TP² × Vol) / Σ(Vol) - VWAP²)
```

#### Volume Distribution
```
For each bar:
  Bar Range = High - Low
  Levels Touched = Bar Range / Level Size
  Volume Per Level = Bar Volume / Levels Touched
  Distribute across price levels proportionally
```

### Performance Metrics

- **Update Frequency**: Every tick (real-time)
- **Calculation Time**: <50ms per update (typical)
- **Memory Usage**: ~5-10MB (depends on settings)
- **CPU Impact**: Low to Medium (optimized loops)

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

### How to Contribute

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** changes (`git commit -m 'Add AmazingFeature'`)
4. **Push** to branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines

- Follow MQL5 coding standards
- Add comments for complex logic
- Test thoroughly on multiple instruments
- Update documentation for new features
- Maintain backward compatibility

### Feature Requests

Open an issue with:
- Clear description of desired feature
- Use case/trading scenario
- Potential implementation approach

---

## 📜 License

This project is licensed under the **MIT License** - see below for details:

```
MIT License

Copyright (c) 2024 M4DI~UciH4 (github.com/RizkyEvory)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- **Auction Market Theory**: J. Peter Steidlmayer & Market Profile concepts
- **Volume Profile**: Developed from institutional order flow principles
- **Community**: Thanks to all traders providing feedback and suggestions

---

## 📞 Contact & Support

- **GitHub**: [@RizkyEvory](https://github.com/RizkyEvory)
- **Issues**: [GitHub Issues](https://github.com/RizkyEvory/M4DI-UciH4-Auction-Profile/issues)
- **Discussions**: [GitHub Discussions](https://github.com/RizkyEvory/M4DI-UciH4-Auction-Profile/discussions)

---

## ⚠️ Disclaimer

**IMPORTANT**: This indicator is for educational and informational purposes only. Trading forex, futures, and other financial instruments involves substantial risk of loss and is not suitable for every investor. Past performance is not indicative of future results.

- Always use proper risk management
- Never risk more than you can afford to lose
- Practice on demo accounts before live trading
- The indicator provides signals, not guarantees
- Always combine with fundamental analysis and risk management

**The author is not responsible for any trading losses incurred while using this indicator.**

---

## 🔄 Version History

### v4.0 (Current)
- ✅ Complete rewrite with professional architecture
- ✅ Added 3 automated trading strategies
- ✅ Implemented composite profile tracking
- ✅ Enhanced VWAP analysis with bands
- ✅ Added HVN/LVN automatic detection
- ✅ Professional dashboard with real-time metrics
- ✅ Session-based profile analysis
- ✅ Performance optimizations

### v3.0
- Basic volume profile implementation
- POC and value area calculations
- Initial balance tracking

---

## 📚 Additional Resources

### Recommended Reading
- **Mind Over Markets** - James Dalton
- **Markets in Profile** - James Dalton
- **A Complete Guide to Volume Price Analysis** - Anna Coulling
- **Trading with Market Profile** - Peter Steidlmayer

### Video Tutorials
- Market Profile Basics
- Volume Profile Trading Strategies
- VWAP Trading Guide
- Auction Market Theory Explained

### Related Tools
- `MarketProfile.ex5` - Pure Market Profile visualization
- `VolumeProfile.ex5` - Standalone volume profile
- `VWAP_Indicator.ex5` - VWAP with bands

---

<div align="center">

**⭐ If you find this indicator useful, please give it a star! ⭐**

**Made with ❤️ by M4DI~UciH4**

**Happy Trading! 📈**

</div>

