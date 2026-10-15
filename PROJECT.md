# Kulhudhuffushi Taxi App

# Main plan
Build phases

✅Phase 1: Database and skeleton
Create the requests table (id, name, phone, pickup, destination, status, created_at) and a basic page that connects to it.

Phase 2: Customer page
Request form with pickup and destination dropdowns (a list of the city’s wards and landmarks), then a “Request sent” confirmation.

Phase 3: Driver/dispatcher page
Password-protected page showing live incoming requests, with Accept and Done buttons. Requests update automatically without refreshing.

Phase 4: Customer status
The customer sees “Waiting → Driver accepted → Done,” and the driver’s name and number once accepted.

Phase 5: Alerts
A loud sound on the driver page when a request arrives. Optionally forward each request to a Telegram or Viber group as a backup.

Phase 6: Language and polish
Dhivehi/English toggle, phone-friendly layout, “Add to Home Screen” support, and your branding.

Phase 7: Test and pilot
Test with friends first, then offer a free one-month pilot to one company with 3-5 drivers. Record requests per day and average response time.

Phase 8: Pitch
Show real pilot numbers, then propose a setup fee plus monthly license.

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

## Done
- Phase 1: complete (security tests all passed [date])
- Phase 2: customer page built (index.html, config.js). Tests: [not yet run]

## Decisions added
- Flat fare MVR 35 island-wide, same both directions, shown in MVR
- Luggage fare MVR 50 recorded in fare_settings but NOT offered (v1 = no luggage)
- Placeholder places: Airport, Hospital, Harbour, Restaurant, Guesthouse, Shop (replace with real names later)

## Known issues
- Real place names not supplied
- No rate limiting on request creation
- Customers must keep the token manually (status page is Phase 4)

## Next 3 tasks
1. Test Phase 2 and record results
2. Build driver/dispatcher page (Phase 3)
3. Customer status page using the tracking code (Phase 4)
