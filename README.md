![Up-to-date Screenshot](https://github.com/abbaselmas/tradingview-indicator-combination/assets/28142617/fc8b3058-6743-4eb6-be19-50fd95a90e13)

![Example Screenshot](https://github.com/abbaselmas/tradingview-indicator-combination/assets/28142617/e5908ea5-1aa1-417f-b44c-4a85ac541030)

# TradingView Indicator Suite

A professional collection of optimized Pine Script v6 indicators for comprehensive market analysis. This suite combines multiple powerful trading tools designed for serious traders who need precise levels, market structure, and volume analysis.

**Why two indicators?** TradingView's free (Basic) plan allows only two indicators on a chart at the same time. Abbas1 and Abbas3 each bundle several public tools into one script so that both fit within that limit.

---

## 📊 Abbas1 - Multi-Indicator Trading System

**Range | Blocks | NYOpens | Weekendicator | CME | BPR**

### Overview
A comprehensive all-in-one indicator that combines 6 powerful trading tools for enhanced market analysis. Perfect for traders who want key levels, market structure, and price ranges in a single clean indicator.

### Features

#### 1. 📈 Bollinger Bands
- Customizable BB settings (length: 21, multiplier: 2.8)
- Adjustable source and deviation calculations
- Visual basis line with upper and lower bands
- Identifies volatility and potential reversal zones

#### 2. 📅 Weekendicator
- Weekend price projection tool with automatic detection
- Extends price levels during Saturday/Sunday
- Adjustable multiplier (0-10%) for projection range
- Anticipates Monday opening gaps using high/low ratios

#### 3. 📦 Range Blocks (Market Structure)
Advanced order flow visualization featuring:
- **Order Blocks**: Untested and tested supply/demand zones with color coding
- **Breaker Blocks**: Failed order blocks that indicate reversals
- **MSB Lines**: Market Structure Break lines for trend changes
- **Range Detection**: Identifies consolidation ranges with 0.25, 0.5, 0.75 levels
- Real-time pivot high/low tracking
- Automatic cleanup of invalidated blocks

#### 4. 🗽 New York Opens
Two NY session markers, defined in New York local time (DST-aware on any symbol):
- **Midnight Open (00:00 New York)**: the New York midnight opening price
- **8:30 AM Open (08:30 New York)**: opening price at the US economic data release time
- Customizable line styles (Solid, Dotted, Dashed)
- Optional labels and historical lines
- Individual color settings and session configuration

#### 5. 🎯 Balanced Price Range (BPR)
- Fair Value Gap (FVG) analysis for balanced price ranges
- Detects both bullish and bearish BPR zones
- "Clean" BPR filter (price doesn't interfere before completion)
- Adjustable threshold for minimum range size
- Configurable lookback period (default: 50 bars)
- Real-time extension tracking

#### 6. 📈 CME Gap Show & Fill
CME Bitcoin Futures (`CME:BTC1!`) weekend gap with 3 modes:
1. Close from current symbol with CME trading hours
2. Direct CME original close price
3. CME settlement price
- Draws the Friday close line while CME is closed (Friday 16:00 to Sunday 17:00 Chicago time)
- Background fill: green when price is above the Friday close, red when below
- Time zone handling in America/Chicago (DST-aware), works on any chart timeframe
- Meant for BTC charts; modes 2 and 3 always read `CME:BTC1!`

### Settings & Customization

**Input Groups:**
- **BB**: Length, Source, Multiplier
- **Weekend**: Multiplier percentage
- **Range Blocks**: Toggle switches for MSB lines, Order Blocks, Breaker Blocks, Range lines, color customization
- **New York Opens**: Separate settings for Midnight and 8:30 opens, display toggles, line styles
- **Balanced Price Range**: Threshold, lookback period, clean BPR filter, delete old BPR option
- **CME Gap**: Mode selection, automatic gap tracking

### Performance
- **Pine Script v6** with modern optimized syntax
- Cached calculations to reduce redundant computations
- Optimized array operations with size caching
- Early loop exits for improved efficiency
- Clean, organized code with section headers

### Usage Tips
- **Day Traders**: Focus on NY Opens and BPR for intraday setups
- **Swing Traders**: Use Range Blocks and Bollinger Bands for structure
- **Weekend Planning**: Monitor Weekendicator and CME gaps
- **Order Flow**: Combine Order Blocks with BPR zones for high-probability entries
- Best used on 15m-1H timeframes for cleaner signals

### Technical Specifications
- **Version**: Pine Script v6
- **Overlay**: True
- **Precision**: 4 decimal places
- **Max Bars Back**: 1000
- **Max Lines**: 500
- **Max Boxes**: 50 (TradingView default; oldest boxes are removed first)

---

## 📊 Abbas3 - Volume Profile & Key Levels System

**PVP | nPOCs | Key Levels | Fair Value Gaps | Smart Money Concepts**

### Overview
An advanced indicator combining Periodic Volume Profile (PVP), multi-timeframe key levels, Fair Value Gaps (FVG), and Smart Money Concepts (SMC) for institutional-grade market analysis. Perfect for traders who need precise volume-based levels and market structure.

### Features

#### 1. 📊 Periodic Volume Profile (PVP)
- **Any periodic timeframe**: e.g. 4H, Daily, Weekly (default), 2W, Monthly, 3M, 6M, 12M
- **Dynamic volume analysis** with customizable number of rows (default: 200, range 50-400)
- **Point of Control (POC)**: Highest volume price level
- **Value Area High (VAH)** and **Value Area Low (VAL)**: default 68% of period volume (adjustable)
- **Profile placement options**: Left, Right, or Next Period
- **Visual customization**: Profile width, colors for total volume and value area
- **Background fill** option for enhanced visibility
- **Developing profile** (optional) with DPOC/DVAH/DVAL path plots
- **Previous period** POC/VAH/VAL lines (optional)

#### 2. 📍 Naked POCs (nPOCs)
- Each completed period's POC extends right until price touches it, crosses it, or the last bar (configurable)
- Optional cross (✕) and touch (▲/▼) markers on the chart
- Alerts: "nPOC Crossed" and "nPOC Touched"

#### 3. 🎯 Key Levels - Multi-Timeframe
Comprehensive level tracking across all major timeframes:

**4-Hour Levels** (off by default):
- Previous 4H High, Low, Open, and Mid

**Monday Range:**
- Monday High, Low, and Mid (special session focus)

**Daily Levels:**
- Previous Day High (PDH), Previous Day Low (PDL)
- Daily Open (DO), Previous Day Mid (PDM)

**Weekly Levels:**
- Previous Week High (PWH), Previous Week Low (PWL)
- Weekly Open (WO), Previous Week Mid (PWM)

**Monthly Levels:**
- Previous Month High (PMH), Previous Month Low (PML)
- Monthly Open (MO), Previous Month Mid (PMM)

**Yearly Levels:**
- Current Year High (CYH), Current Year Low (CYL)
- Yearly Open (YO), Current Year Mid (CYM)

**Key Level Features:**
- Individual toggle switches for each timeframe
- Customizable line styles (Solid, Dashed, Dotted)
- Adjustable line width (Small, Medium, Large)
- Text labels with two format options (Compact: "PDH" or Full: "Prev Day High")
- Global color override option for unified appearance
- Display style: Standard (line starts at the level's origin) or Right Anchored
- Automatic label merging when two levels have exactly the same price
- Display distance configuration (bars to extend right)

#### 4. 📉 Fair Value Gaps (FVG)
- **Bullish and Bearish FVG detection** using 3-candle patterns
- **Auto Threshold**: Filters insignificant gaps automatically
- **Custom timeframe support**: Analyze FVGs on any timeframe
- **Box visualization**: FVGs drawn as boxes with transparency
- **Auto-mitigation tracking**: Boxes are removed once price fully fills the gap
- **Extend FVG**: Configure how many bars to extend boxes (default: 50)
- Color-coded: Green for bullish, Red for bearish FVGs

#### 5. 🧠 Smart Money Concepts (SMC)
Advanced institutional trading concepts:

**Market Structure:**
- **Internal Structure**: Faster, more sensitive structure breaks
- **Swing Structure**: Major trend structure breaks
- **BOS (Break of Structure)**: Trend continuation signals
- **CHoCH (Change of Character)**: Trend reversal signals
- Separate controls for bullish and bearish structure
- Confluence filter for internal structure (reduces false signals)

**Swing Point Detection:**
- Configurable swing length (default: 50)
- High/Low pivot labels on chart
- Strong/Weak High and Low identification
- Real-time swing tracking

**Trend Coloring:**
- Color candles based on current trend
- Two style options: Colored or Monochrome
- Helps identify trend at a glance

#### 6. ⚙️ Advanced Customization

**Volume Profile Settings:**
- Profile levels, period type, placement options
- POC color and width, VAH/VAL colors
- Value area percentage, background options
- Developing profile, previous-period levels, and nPOC extension mode

**Key Levels Settings:**
- Individual timeframe enables/disables
- Global vs individual coloring
- Text label format and size options
- Line style, width, and extension distance
- Display style (Standard or Right Anchored)
- Level merging option

**Fair Value Gaps Settings:**
- FVG display toggle
- Auto threshold or manual filtering
- Custom timeframe selection
- Bullish/Bearish color customization
- Extension bar configuration

**Smart Money Concepts Settings:**
- Mode: Historical or Present (clean chart option)
- Style: Colored or Monochrome themes
- Structure display toggles (Internal/Swing)
- Bullish/Bearish structure filters (All, BOS only, CHoCH only)
- Label size options (Tiny, Small, Normal)
- Swing length and detection sensitivity

### Performance Optimizations
- **Pine Script v6**
- **Range-limited volume binning**: each bar only updates the profile rows it overlaps
- **Developing profile** is drawn only on the last bar and computed per bar only when path plots are enabled
- **Period detection** via `timeframe.change()` instead of extra security requests
- **Mitigated FVGs** are pruned from memory, so per-bar work does not grow over time

### Usage Tips
- **Volume Traders**: Use PVP to identify high-volume nodes and value areas for support/resistance
- **Level Traders**: Key levels provide precise entry/exit points across all timeframes
- **Smart Money Followers**: SMC features reveal institutional order flow and structure
- **Gap Traders**: FVG boxes show unfilled gaps that price tends to revisit
- **Multi-Timeframe Analysis**: Combine daily levels with weekly/monthly for confluence
- Best used on 5m-1H for intraday, 4H-D for swing trading

### Trading Applications
1. **Support/Resistance**: Use POC, VAH, VAL, and key levels as S/R zones
2. **Entry Setups**: Look for FVG + Key Level confluence for high-probability entries
3. **Trend Confirmation**: SMC structure breaks confirm trend changes
4. **Volume Nodes**: POC lines show where most trading occurred (strong S/R)
5. **Gap Fills**: Trade FVG fills with confluence from key levels
6. **Range Trading**: Use value area boundaries for range-bound strategies

### Technical Specifications
- **Version**: Pine Script v6
- **Overlay**: True
- **Max Bars Back**: 500 (5000 for the high/low/volume series used by the volume profile; profile length is capped at 4999 bars)
- **Max Lines**: 500
- **Max Boxes**: 500
- **Max Labels**: 500

---

## 🚀 Installation

1. Open TradingView chart
2. Click "Indicators" at the top
3. Click "Pine Editor" at the bottom
4. Copy the code from `Abbas1.pine` or `Abbas3.pine`
5. Paste into the editor
6. Click "Add to Chart"
7. Configure settings to your preference

### Upgrading from an earlier version
- **Abbas1 New York Opens**: the session inputs are now in New York local time (defaults `0000-0005` and `0830-0835`). If you added Abbas1 to a chart before this change, the chart keeps the old values (`0400-0405`, `1230-1235`). Reset both session inputs to their defaults (or re-add the indicator).

## 📝 Notes

- Both indicators are written in Pine Script v6
- Code is organized with clear section headers
- Customizable colors, sizes, and display options
- Most tools work on any market; the CME gap uses `CME:BTC1!` and is meant for BTC charts, and the Weekendicator is most useful on 24/7 markets such as crypto
- Volume Profile needs volume data; on symbols without volume it has nothing to show
- Can be used together or separately depending on your trading style

## ⚠️ Disclaimer

These indicators are for educational purposes only. Always practice proper risk management and conduct your own analysis before trading. Past performance does not guarantee future results.

## 👨‍💻 Author

**Abbas Elmas**
- Repository: [tradingview-indicator-combination](https://github.com/abbaselmas/tradingview-indicator-combination)

## 📄 License

Open source - Feel free to modify and use for personal trading.