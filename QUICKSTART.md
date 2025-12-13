# Complete End-to-End Workflow

# 1. Start UI server (keep running)
npm run ui

# 2. Create journey prototype
npm run gen:journeys

# 3. Generate test criteria  
npm run gen:stories

# 4. Generate Playwright tests
npm run gen:tests -- --journey=dbs-check

# 5. Validate/run tests
npm run gen:validate

# Alternative: Run specific test
cd playwright-poc-qa && npm run test -- tests/generated/dbs-check.spec.ts

# or

cd playwright-poc-qa && npx playwright test --ui tests/generated/dbs-check.spec.ts

# Quick test fix: Manually edit JOURNEY_PATH in generated test if URL is wrong
# const JOURNEY_PATH = '/correct/path/from/journey-config';