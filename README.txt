FARMPro Survey v0.8.4 - Supabase Data API auth fix

Changes:
- Correct Supabase project URL retained.
- Publishable key only; NO secret/service-role key.
- Sends both apikey and the unauthenticated Authorization header behavior used by the Supabase JS Data API client.
- Uses a normal INSERT instead of upsert/on_conflict.
- Duplicate submission_id (23505/409) is treated as already synced.
- New service-worker cache: farmpro-survey-v084.

Replace in the ROOT of FarmPro-Survey:
1. index.html
2. manifest.webmanifest
3. sw.js

Then wait for GitHub Pages deployment, reload, login with the same enumerator,
and press Sync Now on the existing failed interview.
