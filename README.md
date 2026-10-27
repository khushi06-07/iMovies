# IMovies – Movie ticket booking (MERN)
Browse movies, pick a showtime, reserve seats with live availability, manage bookings. JWT auth, bcrypt, atomic MongoDB seat locking (no double booking).

## Setup
Requires Node 16+ and MongoDB running locally.
```
cd server && cp .env.example .env && npm install && npm run seed && npm start   # API on :5000
cd client && npm install && npm run dev                                          # UI on :5173
```
Demo login after seeding: demo@imovies.com / demo123

## API
POST /api/auth/register | /api/auth/login
GET /api/movies, /api/movies/:id (with upcoming shows)
GET /api/shows/:id (seat availability)
POST /api/bookings {showId, seats[]} (auth) | GET /api/bookings/mine (auth) | DELETE /api/bookings/:id (auth, cancels)
