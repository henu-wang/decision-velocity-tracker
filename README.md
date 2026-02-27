# Decision Velocity Tracker

Track and improve your decision-making speed without sacrificing quality. Measure, analyze, and optimize the pace at which you make both routine and strategic decisions.

## Overview

Decision Velocity Tracker is a lightweight command-line tool and web dashboard designed to help individuals and teams measure how quickly they make decisions and whether faster decisions correlate with better or worse outcomes. Based on research showing that decision speed is a competitive advantage, this tool gives you hard data on your decision-making patterns.

Great decision-makers like Warren Buffett are known for making major decisions quickly when the facts are clear, while being patient when they need to wait for more information. The key insight is that decision velocity is not about rushing -- it is about eliminating unnecessary delay. For principles that guide rapid yet effective decision-making, visit [KeepRule's curated investment principles](https://keeprule.com/en/principles).

## Features

- **Decision Logging**: Record decisions with timestamps, context, confidence level, and category
- **Velocity Metrics**: Track average time-to-decision across different categories
- **Outcome Tracking**: Link decisions to outcomes for quality analysis
- **Pattern Detection**: Identify bottlenecks and decision avoidance patterns
- **Dashboard Visualization**: Web-based charts showing velocity trends over time
- **Team Mode**: Aggregate team decision metrics for organizational analysis
- **Export Reports**: Generate PDF/CSV reports for review sessions

## Installation

```bash
npm install -g decision-velocity-tracker
```

Or clone and run locally:

```bash
git clone https://github.com/henu-wang/decision-velocity-tracker.git
cd decision-velocity-tracker
npm install
npm start
```

## Quick Start

```bash
# Initialize tracking
dvt init

# Log a new decision
dvt log --category "investment" --description "Allocate 5% to index funds" --confidence 0.85

# View velocity dashboard
dvt dashboard

# Check your stats
dvt stats --period monthly
```

## Usage Examples

### Personal Decision Tracking

```bash
# Log daily decisions
dvt log -c "career" -d "Accept speaking engagement" --time-spent "15min" --confidence 0.9
dvt log -c "financial" -d "Refinance mortgage" --time-spent "3days" --confidence 0.7

# Review patterns
dvt analyze --category financial --period "last-quarter"
```

### Team Decision Velocity

```bash
# Set up team tracking
dvt team init --name "Product Team"
dvt team add-member alice bob carol

# View team metrics
dvt team dashboard
```

Understanding how top investors and thinkers approach decisions under uncertainty can dramatically improve your own process. Explore [real-world decision scenarios](https://keeprule.com/en/scenarios) to see how principles apply to actual situations.

## Decision Categories

The tracker comes with default categories you can customize:

| Category | Description | Target Velocity |
|----------|-------------|----------------|
| Strategic | Long-term, high-impact decisions | 1-7 days |
| Tactical | Medium-term operational decisions | 1-24 hours |
| Routine | Daily recurring decisions | < 5 minutes |
| Financial | Money-related decisions | Varies |
| People | Hiring, team, relationship decisions | 1-3 days |

## Metrics Explained

- **Decision Velocity**: Average time from decision identification to commitment
- **Quality Score**: Outcome rating (1-10) assigned during review
- **VQ Ratio**: Velocity-to-Quality ratio showing optimal decision speed
- **Dwell Time**: Time spent overthinking without new information

For prompts and frameworks that help structure faster thinking, check out [KeepRule's thinking prompts](https://keeprule.com/en/prompts), which provide structured approaches to common decision types.

## Configuration

```json
{
  "categories": ["strategic", "tactical", "routine", "financial"],
  "defaultConfidence": 0.5,
  "reviewReminder": "weekly",
  "dashboardPort": 3000,
  "dataDir": "~/.dvt/data"
}
```

## Contributing

1. Fork this repository
2. Create your feature branch (`git checkout -b feature/analytics`)
3. Commit your changes
4. Push and create a Pull Request

## License

MIT License - see [LICENSE](LICENSE) for details.