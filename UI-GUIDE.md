# Aiutopia UI/UX Reference — Branding, Look, and Frontend Style

**Last updated:** July 2025

---

## Core Visual Style

- **Vibe:** Next-gen, monopoly-level intelligence platform; “elite but accessible.”
- **Brand Message:** “Cut through data noise.”  
  Use this phrase on landing and dashboard as a subtle but clear statement.
- **Palette:**  
  - Deep indigo, silver, electric blue (AI/futuristic)
  - Black and white base for clarity, not busy or over-saturated
  - Occasional green/gold for profit/causal callouts
- **Typography:**  
  - Strong sans-serif headlines (think IBM Plex Sans, Inter, or SF Pro)
  - Slightly softer, readable body text
  - Large, clear stats—numbers should “pop”

---

## Dashboard & Page Layout

- **Header:**  
  - Aiutopia logo (vector or simple wordmark)
  - Main navigation: Dashboard | Models | History | Team | Support
- **Hero Section:**  
  - “Cut through data noise with Aiutopia” as headline or subhead
  - Quick profit/cashflow stat or animation (“$123,000 profit modeled”)
- **Core Cards/Widgets:**  
  - “Action Simulator” card: select action/amount/industry, press “Simulate,” see instant results
  - “Causal Path” visual: chart/graph showing *why* Aiutopia made that recommendation
  - “Risk/Reward Bands”: colored bands, histogram, or sparkline for quick risk profile
- **Responsive:**  
  - Looks clean on desktop and mobile
  - Don’t crowd—leave breathing room

---

## Interaction/UI Components

- **Primary Button:**  
  - Electric blue background, white text, bold and slightly rounded
- **Input Fields:**  
  - Light outline, subtle placeholder
  - Icons for “action,” “amount,” “industry”
- **Results Display:**  
  - Large profit/loss number with badge
  - Short, clear “Causal Explanation” under results
  - Visual graph or mini chart for scenario spread

---

## Bonus Features / Ideas

- **Simulation History:**  
  - Table or timeline of previous runs, clickable for details
- **Dark Mode:**  
  - Deep gray background, neon/blue accents for numbers and cards
- **Mobile Menu:**  
  - Slide-out menu with same core links

---

## Frontend Tech Notes

- **Suggested Stack:**  
  - React or Next.js for frontend
  - Tailwind CSS or shadcn/ui for rapid, modern design
  - Recharts or Victory for graph/chart components
  - API calls to FastAPI backend at `/money_model` and `/quantum_money`

---

## Example Component Layout (React/JSX pseudo-code)

```jsx
<Card>
  <h2>Profit Simulation</h2>
  <InputGroup>
    <Input icon="💡" placeholder="Action (e.g. Launch Product)" />
    <Input icon="💲" placeholder="Amount" />
    <Input icon="🏭" placeholder="Industry" />
    <Button>Simulate</Button>
  </InputGroup>
  <div>
    <BigNumber>$8,900</BigNumber>
    <Tag color="green">Expected Profit</Tag>
    <p>Causal explanation: Strategic expansion + historical ROI</p>
    <Chart data={simulationSpread} />
  </div>
</Card>
