##  Step-by-Step Workflow

# 1. Start UI server (keep running)
npm run ui

# 2. Generate index of available journeys
npm run ai:index

# 3. Create journey prototype
npm run ai:journeys

# 4. Generate test stories/criteria
npm run ai:stories

# 5. Generate Playwright tests
npm run ai:tests

# 6. Run tests in Playwright UI
npm run ai:check -- <journey-id>
