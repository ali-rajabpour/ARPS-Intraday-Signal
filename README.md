# ARPS Intraday Signal
**Originally created: August 05, 2020**
*(Note: This script was created in 2020 but is being shared on GitHub on 2025-04-25)*

---

# ARPS Intraday Signal

## Overview

The "ARPS Ultimate Intraday Signal" is a versatile Pine Script designed for TradingView to plot and analyze multiple types of moving averages across various timeframes, detect significant price movements, and highlight crossovers between moving averages. This tool facilitates a comprehensive technical analysis strategy for intraday and swing traders by providing flexible configuration options and advanced features.

This script empowers traders to identify key market trends, optimize entry/exit points, and customize indicators to match their trading style.

---

## Key Features

- **Multi-Timeframe Moving Averages:** 
  Plot moving averages (MA) based on the current chart resolution or an alternate resolution for deeper analysis.
  
- **Customizable Moving Averages:**
  Supports 8 types of moving averages:
  - SMA (Simple Moving Average)
  - EMA (Exponential Moving Average)
  - WMA (Weighted Moving Average)
  - HullMA (Hull Moving Average)
  - VWMA (Volume Weighted Moving Average)
  - RMA (Running Moving Average)
  - TEMA (Triple Exponential Moving Average)
  - Tilson T3
  
- **Multi-MA Crossover Detection:**
  Identify crossover points between two customizable moving averages. Display these crossovers with visual markers (dots) on the chart.

- **Directional Color Coding:**
  Dynamically color-code MA lines to reflect market direction:
  - Green (`lime`) for upward trends
  - Red (`red`) for downward trends
  - Optional smoothing to reduce noise in MA direction detection.

- **Price Crossing Alerts:**
  Highlight bars when the price crosses above or below the first or second moving average. Optionally customize this behavior.

- **Automated Alerts:**
  Real-time alerts for MA crossovers, enabling traders to act quickly on trend changes:
  - `Cross_LONG` alert for bullish crossovers.
  - `Cross_SHORT` alert for bearish crossovers.

- **Visual Customization:**
  Configure the appearance of plotted MAs, price crosses, and alerts. Options include choosing line width, bar colors, and smoothing factors to match trading preferences.

---

## How It Works

The script operates by leveraging the Moving Averages framework to calculate and plot multiple types of MAs on your chart, comparing price movements relative to these MAs. 

It includes powerful mechanisms to detect and visually mark when price or other MAs cross the calculated baseline moving averages. For example:
- **Price Crosses MA:** Highlights bars on your chart when the closing price crosses above or below an MA.
- **MA Crossovers:** Identifies and marks intersections of two MAs defined by different parameters.

Alerts can help you catch these events even when you're not looking at your charts.

---

## Input Parameters

### General Settings
- **Use Current Chart Resolution:** Enable/disable current timeframe for MA calculations.
- **Alternate Timeframe (`resCustom`):** Define an alternate resolution (timeframe), such as `45` minutes.
  
### Moving Average 1 Settings
- **Length (`len`):** Lookback period for the first MA (default: `20`).
- **Type (`atype`):** MA type (default: `8`, Tilson T3).
- **Tilson T3 Factor:** Custom Tilson T3 smoothing factor.

### Moving Average 2 Settings (Optional)
- **Enable 2nd MA (`doma2`):** Toggle the second MA calculation.
- **Length (`len2`):** Lookback period for the second MA (default: `50`).
- **Type (`atype2`):** MA type for the second MA (default: `4`, HullMA).
- **Tilson T3 Factor:** Custom Tilson T3 smoothing factor.

### Visual and Alert Customization
- **Show Price Crosses:** Enable plotting of bars when price crosses an MA.
- **Crossover Marker:** Show visual dots on MA crossovers.
- **Bar Colors:** Enable price-based bar coloring for crossovers.
- **Line Smoothing:** Adjust smoothing factor for MA direction signals.

---

## Usage Instructions

1. Add the script to your TradingView chart by navigating to the "Pine Script Editor" and pasting the provided code.
2. Configure the input parameters as per your trading strategy. You can tailor settings such as the moving average lengths, types, and display resolution.
3. Enable/disable visual highlights for price/MA and MA/MA crossovers.
4. Set up alerts to get notified for potential trading opportunities.

---

## Alerts

Create alerts in TradingView for:
- **`Cross_LONG`:** Triggered when the first MA crosses above the second.
- **`Cross_SHORT`:** Triggered when the first MA crosses below the second.

These alerts can give you real-time notifications on critical trend shifts in the market.

---

## Example Configurations

### Intraday Setup
- **Input Timeframe:** Use `15-minute` resolution for high-frequency trading.
- **MA Parameters:**
  - First MA: SMA, Length `14`
  - Second MA: EMA, Length `50`
  
### Swing Trading Setup
- **Input Timeframe:** Use `4-hour` resolution for better trend stability.
- **MA Parameters:**
  - First MA: HullMA, Length `21`
  - Second MA: TEMA, Length `55`

---

## Future Enhancements

Planned updates for the ARPS Ultimate Intraday Signal include:
1. Adding support for additional moving average types.
2. More advanced alert options, such as thresholds for crossover angles.
3. Integration with external indicators for confluence-based strategies.

---

## Contact

- Author: **Ali Rajabpour-Sanati**
- Email: [ali.poursanati@gmail.com](mailto:ali.poursanati@gmail.com)

Feel free to reach out for inquiries or suggestions! 

---

## License

This script is licensed under the MIT License. Customizations and enhancements are allowed with proper attribution to the author.
