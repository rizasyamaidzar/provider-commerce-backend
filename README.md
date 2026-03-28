# Provider Commerce Backend

Mock backend API for provider commerce using `json-server`.

## Requirements

- Node.js `>= 22.12.0`
- npm

## Local Setup

1. Clone repository

```bash
git clone https://github.com/rizasyamaidzar/provider-commerce-backend.git
cd provider-commerce-backend
```

2. Install dependencies

```bash
npm install
```

3. Run the API locally

```bash
npm start
```

The server will run at:

```text
http://localhost:3000
```

## Available Endpoints

- `GET /users`
- `GET /users/:id`
- `GET /packages`
- `GET /packages/:id`
- `GET /transactions`
- `GET /transactions/:id`
- `GET /topups`
- `GET /topups/:id`

## Example Requests

```bash
curl http://localhost:3000/users
curl http://localhost:3000/users/2
curl http://localhost:3000/packages
curl "http://localhost:3000/users?email=john@example.com"
curl "http://localhost:3000/transactions?user_id=2"
```

## Available Data

The API data source is stored in `db.json` and currently includes:

- `users`
- `packages`
- `transactions`
- `topups`

## Useful Scripts

- `npm start` runs the API with `db.json`
- `npm test` runs the test suite
- `npm run typecheck` runs TypeScript type checking

## Notes

- The local start command uses `0.0.0.0` so it also works on hosting platforms.
- If you use Node 20, the app may still start, but the test command requires newer Node support.
- Husky pre-commit is configured to skip tests automatically when the local Node version is below `22.12.0`.

## Deployment

Public Railway URL:

```text
https://provider-commerce-backend-production.up.railway.app
```

Example:

```text
https://provider-commerce-backend-production.up.railway.app/users
```
