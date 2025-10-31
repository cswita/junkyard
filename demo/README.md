# SRE Agent - Alert Triage & Diagnosis Demo

An interactive, generative user experience demonstrating how an autonomous SRE agent triages and diagnoses production alerts.

## Overview

This demo showcases an intelligent SRE agent responding to a critical production alert. The agent autonomously:

- **Analyzes** incoming alerts and assesses severity
- **Investigates** system metrics and recent changes
- **Diagnoses** root causes with high confidence
- **Recommends** remediation steps with prioritization

## Features

### 🎨 Generative UX
- Real-time thought stream showing agent reasoning
- Progressive disclosure of investigation steps
- Animated transitions and visual feedback
- Terminal-inspired aesthetic with modern styling

### 🤖 Intelligent Triage Process
The demo simulates a realistic incident response workflow:

1. **Alert Analysis** - Parse and prioritize incoming alerts
2. **Context Gathering** - Query metrics, logs, and system state
3. **Change Correlation** - Identify recent deployments or config changes
4. **Deep Dive Analysis** - Examine application-level metrics and profiling data
5. **Root Cause Identification** - Synthesize findings into actionable diagnosis
6. **Remediation Planning** - Generate step-by-step recovery plan

### 📊 Key Metrics Display
- Confidence level in diagnosis
- Time to diagnose (MTTD)
- Impact severity assessment
- Affected infrastructure components

## Usage

### Running the Demo

Simply open the HTML file in any modern web browser:

```bash
# Using Python's built-in HTTP server
cd demo
python3 -m http.server 8000

# Then navigate to:
# http://localhost:8000/sre-agent-triage.html
```

Or open directly:
```bash
open sre-agent-triage.html  # macOS
xdg-open sre-agent-triage.html  # Linux
start sre-agent-triage.html  # Windows
```

### Interactive Controls

1. Click **"Start Triage Process"** to begin the demonstration
2. Watch as the agent progressively analyzes the alert
3. Observe the thought process, investigations, and conclusions
4. Review the final diagnosis and remediation plan
5. Click **"Restart Demo"** to run again

## Demo Scenario

**Alert:** Critical memory usage (94.3%) on production API gateway

**Investigation Flow:**
- Queries Kubernetes pod metrics
- Reviews deployment history
- Analyzes heap profiling data
- Examines code changes

**Diagnosis:** Unbounded memory cache introduced in recent deployment

**Remediation:** Rollback + fix implementation + add memory tests

## Technical Details

### Technologies Used
- Pure HTML/CSS/JavaScript (no dependencies)
- CSS animations for generative reveal effects
- Async/await for progressive content display
- Responsive design for various screen sizes

### Customization

The demo scenario can be easily customized by modifying the `triageSteps` array in the JavaScript:

```javascript
const triageSteps = [
    {
        type: 'thought',  // or 'action'
        icon: '💭',
        title: 'ANALYZING ALERT',
        content: 'Your analysis text...',
        delay: 1000  // milliseconds
    },
    // Add more steps...
];
```

### Styling

The design uses a dark terminal-inspired theme with:
- Monospace fonts for technical authenticity
- Color-coded severity levels (red=critical, yellow=warning, green=success)
- Glowing effects for active elements
- Smooth animations for content reveal

## Use Cases

This demo is ideal for:

- **Product Demonstrations** - Showcase AI-powered SRE capabilities
- **Training & Education** - Teach incident response best practices
- **Customer Presentations** - Illustrate autonomous operations value
- **Internal Demos** - Inspire engineering teams with automation possibilities
- **Documentation** - Visual guide for SRE workflows

## Future Enhancements

Potential additions to make the demo even more powerful:

- [ ] Multiple alert scenarios (DB slowdown, API errors, etc.)
- [ ] Interactive decision points where users can guide the agent
- [ ] Real-time metrics visualization with charts
- [ ] Integration with actual monitoring APIs
- [ ] Export triage reports as PDF/Markdown
- [ ] Voice narration of agent thoughts
- [ ] Collaborative mode with multiple agents
- [ ] Historical playback of actual incidents

## Architecture Concepts

The demo illustrates key SRE agent capabilities:

1. **Multi-source Analysis** - Combining metrics, logs, traces, and config data
2. **Temporal Correlation** - Linking alerts to recent system changes
3. **Hypothesis Testing** - Iteratively narrowing down root causes
4. **Confidence Scoring** - Quantifying diagnostic certainty
5. **Action Prioritization** - Ordering remediation steps by impact
6. **Knowledge Application** - Using best practices and runbooks

## License

Part of the New Relic Developer Toolkit Template

---

**Note:** This is a demonstration/prototype. For production SRE automation, consider integrating with actual observability platforms, incident management systems, and deployment tools.
