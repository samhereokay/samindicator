# Sam V2 LTF - Advanced Trading Indicator

A comprehensive Pine Script indicator combining higher timeframe analysis, liquidity levels, macro tracking, and technical analysis tools.

## 📋 Features

### 1. **Higher Timeframe (HTF) Candles**
- Displays HTF candles on your current chart
- Configurable number of candles (0-20)
- Customizable colors for up/down candles and wicks
- **Auto-mapping by chart timeframe:**
  - 5m chart → 60-min HTF candles
  - 15m chart → 240-min HTF candles
  - 60m chart → Daily HTF candles

### 2. **HTF Countdown Timer**
- Real-time countdown showing **Minutes:Seconds** until HTF candle closes
- Positioned above the HTF candles for easy visibility
- Automatically updates each bar
- Toggle: `Enable All New Features` > `HTF Candle Countdown`

### 3. **Auto-Change HTF & Separators**
- Automatically adjusts HTF candles based on your chart timeframe
- Separators (period dividers) also auto-adjust to match the HTF
- **Mapping:**
  - 5m → 60 min
  - 15m → 240 min
  - 60m → Daily
- Toggle: `Enable All New Features` > `Auto-change HTF & Separators`

### 4. **Range High/Low/Mid**
- Draws range levels on chart
- Configurable colors and display options
- Shows range mid-point for optimal trading zones

### 5. **Liquidity Levels**
- Identifies supply and demand zones
- Detects swing highs and lows
- Customizable lookback periods
- Display as lines or boxes
- Auto-removes mitigated levels or shows them in faded color

### 6. **Macro Features** (On-Chart & New Pane)
- 24+ pre-configured macros for intraday trading
- Time-based macro detection
- **Auto-disables when chart timeframe > 15 minutes**
- Visual representation with labels and boxes
- Memory management to prevent lag

### 7. **Separators**
- Period dividers on chart (hourly, daily, etc.)
- Customizable color, style (solid/dashed/dotted), and width
- Auto-adjusts with HTF mapping

### 8. **SMT Divergences**
- Swing-based divergence detection
- Multi-symbol comparison (e.g., ES1! vs YM1!)
- Dashboard display option

### 9. **Additional Tools**
- **Higher Timeframe Liquidity Levels** - Liquidity analysis on multiple timeframes
- **Table Display** - Summary table with customizable position and colors
- **Alert System** - Get notified on key events

---

## 🎛️ Settings

### Higher Timeframe Candles
- **Timeframe** - Default: 60 (1-hour)
- **Amount of Candles** - How many HTF candles to display (0-20)
- **Colors** - Customize up/down candle and wick colors
- **Location** - Offset from chart edge

### Range Settings
- **Range High/Low** - Toggle range display
- **Range Mid** - Show mid-point of range
- **Colors** - Customize line colors

### Extras (New Features)
- **Enable All New Features** - Master toggle for all new additions
- **Auto-change HTF & Separators** - Auto-map based on chart timeframe
- **HTF Candle Countdown** - Show timer above HTF candles
- **Auto-disable macros >15m** - Hide macros on higher timeframes

### Table Settings
- **Show Table** - Toggle summary table display
- **Size** - Table size options
- **Position** - Location on chart
- **Colors** - Text and background colors

### Separator Settings
- **Separator Color** - Divider line color
- **Separator Style** - Solid, dashed, or dotted
- **Separator Width** - Line thickness
- **Separator Timeframe** - Auto-adjusted based on HTF mapping

---

## 📊 Chart Timeframe Behavior

### ✅ Recommended Timeframes (Macros Active)
- 1m - All features active
- 5m - All features active
- 15m - All features active

### ⚠️ Higher Timeframes (Macros Disabled)
- 30m and above - Macros disabled, all other features active
- HTF candles, countdown, liquidity levels, and separators still work
- Prevents performance issues on larger timeframes

---

## 🎯 How to Use

### Basic Setup
1. Add indicator to chart with your preferred timeframe (5m, 15m recommended)
2. Adjust HTF candle colors to match your theme
3. Enable/disable features in the "Extras" group as needed

### Auto-HTF Mode (Recommended)
1. Enable "Auto-change HTF & Separators"
2. Indicator automatically adjusts HTF and separators based on your chart
3. Switch between timeframes without reconfiguring

### Manual HTF Mode
1. Disable "Auto-change HTF & Separators"
2. Manually set the timeframe and separator timeframe inputs
3. Use for custom timeframe combinations

### Macro Trading
1. Ensure chart is 15m or lower for macros
2. Select preferred macro visualization (On Chart or New Pane)
3. Enable specific macros using toggles (show1-show24, showPM1)
4. Macros auto-disable on higher timeframes

---

## ⚙️ Technical Details

### HTF Auto-Mapping Function
```
5m chart  → 60 (1h)
15m chart → 240 (4h)
60m chart → D (1d)
Other     → Default tf value
```

### Macro Auto-Disable Logic
- **Enabled:** Chart timeframe ≤ 15 minutes
- **Disabled:** Chart timeframe > 15 minutes (30m+)
- Gracefully hides macros without throwing errors

### Memory Management
- Line and box cleanup for macro arrays
- Prevents indicator lag on long-running charts
- Automatic array pruning (>300 lines, >100 labels)

---

## 📝 Notes

- Indicator works best on **1m-15m timeframes** with full features
- **Higher timeframes (30m+)** automatically disable macros but keep all analysis tools
- Use "Enable All New Features" toggle to turn on/off all new additions at once
- Separators and HTF candles auto-adjust when "Auto-change HTF & Separators" is enabled

---

## 🔧 Version Info

**Name:** Sam V2 LTF  
**Version:** 5  
**Overlay:** Yes  
**Max Bars Back:** 500  
**Max Elements:** 500 boxes, 500 lines, 500 labels  

---

## 📦 Credits

- **HTF Candles & Macro System:** Original script architecture
- **Liquidity Levels:** Based on Sonarlab concepts
- **SMT Divergences:** Based on LuxAlgo divergence detection
- **Enhanced Features:** Auto-mapping, countdown timer, macro auto-disable

---

## 🚀 Quick Start Checklist

- [ ] Add indicator to 5m or 15m chart
- [ ] Enable "Auto-change HTF & Separators" for automatic timeframe mapping
- [ ] Enable "HTF Candle Countdown" to see timer
- [ ] Select preferred macro display mode (On Chart or New Pane)
- [ ] Customize colors and settings to your preference
- [ ] Save template for future use

---

**Happy Trading! 📈**
