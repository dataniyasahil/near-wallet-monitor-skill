# NEAR Wallet Monitor Skill

## Purpose
Monitor NEAR wallet balances, track price changes, and send automated alerts when thresholds are met.

## Commands

### `check-balance`
Check current wallet balances for all tokens.

**Example:**
```
check-balance
```

**Output:**
```
📊 Wallet Balance Report
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Token     Balance        Price (USD)    Value (USD)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
NEAR      4.1710         $2.08          $8.67
USDC      1.9831         $0.9998        $1.98
AURORA    0.000286       $0.0281        $0.01
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

💰 Total Portfolio Value: $10.66 USD
```

### `set-alert <token> <condition> <price>`
Set a price alert for a token.

**Examples:**
```
set-alert NEAR above 4.00
set-alert USDC below 0.99
```

### `list-alerts`
List all active price alerts.

### `remove-alert <id>`
Remove an alert by ID.

### `daily-report`
Generate a daily summary report of wallet balances and price changes.

## Installation
```
skill_install wallet-monitor
```

## API Integration
This skill uses the NEAR DCA Agent API to fetch real-time balance data.

## License
MIT