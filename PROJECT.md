# Kulhudhuffushi Taxi App

## What it is
Web app (works in phone browser) where customers request a taxi
without calling a call centre. Drivers see requests live and accept.

## Stack
Plain HTML/CSS/JS + Supabase (database, auth, realtime).
Hosted on Netlify/Vercel from GitHub.

## Decisions
- Fixed fares, no luggage, cash only (no payments in v1)
- Pickup/destination picked from a fixed list of city places
- English first, Dhivehi toggle added in Phase 6
- Customers don't log in; drivers do (Supabase Auth)

## Database
Table `requests`: id, name, phone, pickup, destination,
status (waiting/accepted/done/cancelled), driver_name,
driver_phone, created_at.
Function `get_request_status(request_id)` for customer status.
Customers can only INSERT; logged-in drivers can SELECT/UPDATE.

## Done
- Phase 0: GitHub, Supabase, hosting connected
- Phase 1: database table + security created

## Next 3 tasks
1. Connect a test page to Supabase
2. Build customer request form (Phase 2)
3. Build driver page (Phase 3)

## Known bugs
None yet
