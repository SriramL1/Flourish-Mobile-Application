# Flourish

A mobile-based application that recommends food and activities based on the luteal phase of women's menstrual cycle.

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React Native (TypeScript), via Expo |
| Backend | Python + FastAPI |
| Database | PostgreSQL |
| AI/ML | Python (LLM-based recommendation engine) |
| Design | Canva |
| Deployment | TBD |

## Project Structure

```
Flourish/
├── backend/     # FastAPI backend
├── mobile/      # React Native (Expo) frontend
└── .github/     # CI workflows
```

## Getting Started

### Backend

```bash
cd backend
pip install -r requirements.txt
```

### Mobile

```bash
cd mobile
npm install
npm start
```

## CI

Pull requests to `main` automatically run:
- **Backend**: Python syntax check + lint (`ruff`)
- **Mobile**: TypeScript type check + lint (`expo lint`)

See `.github/workflows/ci.yml` for details.

## Contributing

Work is tracked on our Jira board (project key **FLR**). Each ticket maps to one branch and one PR.

### Branch naming

```
FLR-<ticket-number>-short-description
```

Example: `FLR-7-add-more-checking-code`

### Workflow

1. Pick up a ticket from the Jira board and move it to **In Progress**.
2. Branch off `main` using the naming convention above.
3. Commit and push your work.
4. Open a PR into `main`. Reference the Jira ticket number in the PR title or description.
5. Make sure CI passes (`python-backend` and `mobile-frontend` checks) before requesting review.
6. Once approved and merged, move the ticket to **Done** on the board.

### Code style

- **Backend**: linted with `ruff`. Run `ruff check .` from `backend/` before pushing.
- **Mobile**: linted with ESLint via `npm run lint`, and type-checked with `npx tsc --noEmit` from `mobile/` before pushing.