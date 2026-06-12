# Privacy Policy

**Last updated: 2026-06-12**

Stashed is local-first. By default, everything you save lives in your browser's
local storage and never leaves your device. Some optional, clearly-labeled
features (cloud sync, page archive, and AI tagging) do send data off your device
— this policy explains exactly what, when, and to whom.

We have no analytics, telemetry, crash reporters, or advertising trackers. We
never sell your data.

---

## 1. If you don't sign in (default)

Stashed works fully without an account. In this mode:

- Your saved pages, tags, notes, and collections are stored only in your
  browser (`chrome.storage.local`). We cannot see them.
- The only network activity is:
  - **Favicons** — fetched from `https://www.google.com/s2/favicons` so saves
    show a recognizable icon.
  - **Page metadata** — the content script reads the `<title>`, `<meta>`, and
    `<h1>` of pages you visit to suggest tags and surface related saves. This
    is processed **on your device** and is not transmitted anywhere.

That's the entire footprint for signed-out use.

---

## 2. If you sign in (Google)

Signing in is optional and is used for the trial, subscription, and cloud
features. We authenticate with Google via Chrome's identity API and receive a
standard OpenID token. From it we store, on our backend:

- Your Google account identifier (`sub`), and your email and name as provided by
  Google.
- Your subscription state (free / trial / Pro, trial dates).

Signing in **alone** does not upload your saved pages. Your stash stays local
unless you have an active Pro subscription or trial (see below).

Our backend is **Convex** (convex.dev), which hosts our database and server
functions. Data is scoped to your account.

---

## 3. Pro / trial features that send data off your device

These features are only active for Pro or trial users, and only for pages you
choose to save.

### Cloud sync
When you sync, your stash (page URLs, titles, tags, notes, collections, and save
timestamps) is uploaded to our Convex backend so it can be merged across your
devices. Deletions are soft ("Trash") and are removed permanently after 30 days.
This data is stored per-account on our servers; it is **not** end-to-end
encrypted, because the archive and search features below require us to process it
server-side.

### Page archive
For pages you save, Stashed captures the **readable text** of the page (capped in
size) and stores it on our backend so the saved copy survives if the original
link dies, and so you can search inside saved pages. Only the extracted text is
stored — we do not capture passwords, form inputs, or content behind logins
beyond what is visible as page text at save time.

### AI tagging
When you save a page, its title, URL, and a truncated excerpt of its text are
sent — through our Convex backend — to a third-party AI provider (a hosted AI
model proxied through our backend) to generate topic tags. The provider processes this
content to return tags; their handling of that data is governed by their own
terms. We store only the resulting tags, not a separate copy of the request.
This call happens only for Pro/trial users and is rate-limited per account.

---

## 4. Payments

Subscriptions are handled by **Dodo Payments** (dodopayments.com), our Merchant
of Record. Dodo processes your payment details directly — we never see or store
your card information. We retain only Dodo's customer and subscription
identifiers and your subscription status. See Dodo Payments' privacy policy for
how they handle payment data.

Cancelling stops renewal; Pro remains active until the end of the paid period.

---

## 5. Your data, your control

- **Export** your full stash any time (Settings → Export) as JSON or standard
  Netscape bookmark HTML.
- **Uninstalling** the extension removes all local data from your browser.
- **Delete your cloud data** — sign out to stop syncing, or contact us to delete
  your account and the data associated with it on our backend.

---

## 6. Children

Stashed is not directed to children under 13 and we do not knowingly collect
their data.

---

## 7. Changes

We will update this policy and its "Last updated" date before any new
data-handling behavior ships.

---

## 8. Contact

Questions, concerns, or data deletion requests:

- GitHub: https://github.com/toomanybits/stashed-downloads/issues
- Email: toomanybit@gmail.com
