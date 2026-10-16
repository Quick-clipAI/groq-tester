# Groq & web search checker
Updated: tests `openai/gpt-oss-120b` with the `browser_search` tool (Groq retired `groq/compound` and `compound-mini` on 21 Sep 2026) and has a free "List models my key can use" button.

One static page, no server. Tests the models Creator Booth uses for web research and backup answers.

1. Make a new public GitHub repo, upload `index.html` and this README, then Settings -> Pages -> Deploy from a branch -> main / root.
2. Open the page. Tap "Check my site's Groq proxy" (free, sends nothing to Groq).
3. Tick the models, tap Run tests. Optionally paste a Groq key to also test Groq directly (the key stays in the page and goes only to api.groq.com).
4. Send a screenshot of Results, or tap "Copy results".

Each research test uses 1 Groq request, a plain test 1 more. The page waits up to 90 s per test and marks anything over 30 s as slow, because the app stops waiting at 30 s (Short) or 50 s (Deep).
