Auth API - Node.js + MySQL
   API Authentication using JWT


> Setup

1. Clone the repo
2. Run `npm install`
3. Create a `.env` file (see `.env.example`)
4. Set up MySQL DB and run the provided table creation SQL
5. Start server: `npm run dev`


> Endpoints

| Method | Endpoint         | Description                      |
|--------|------------------|--------------------------------- |
| POST   | /auth/signup     | Register new user                |
| POST   | /auth/login      | Login, get token                 |
| POST   | /auth/logout     | Logout, revoke token             |
| GET    | /profile         | Get user profile (auth required) |


 > Notes
- Passwords hashed with bcrypt
- Tokens are JWT with `jti` for logout support
- Revoked tokens are blocked via middleware
