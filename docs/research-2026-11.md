# tvzup: market and landscape notes (2026-11-25/26)

Desk research only. Vendor figures are the vendors' own claims and are **unverified**. No shopkeeper or advertiser has been interviewed.

## Landscape
- **Gloo** (glooclub.com): store-owner SaaS. TV signage app (Android TV, phone control), local SEO, AI content; menus, offers and reviews on the shop TV. It serves the shop, not an advertiser marketplace. Candidate partner (screens, signage) or competitor. Team, scale and funding not verified. Unknown: whether it already offers reel-based menus or third-party ads.
- **Smiirl**: hardware social-follower counters. No jingle or celebration feature found. tvzup's version would be software.
- **Self-serve digital out-of-home in India already exists** (vendor claims): AdOnMo (about 66k screens), Pixelspot Connect (about 63k), The Hype Loop (about 39k, from 999 rupees). Their screens are in apartments, offices, gyms and malls. Possible gap: very small neighbourhood shops, low per-hour ad prices, QR recall. Unproven.
- **In-store TV networks often fail** (Tesco, Cooler Screens with Walgreens): weak audience attention and hard-to-prove results. Foot-traffic lift must be provable or advertisers leave.
- **Clean Your TV** (open source): debloats Android TV / Google TV only; Samsung and LG are mostly unsupported. Useful for the player on Android TV hardware.

## Strategy conclusions so far
1. Do not rebuild what a partner already does (shop signage, menus, offers). Check Gloo's real product before any partnership pitch; partner only with proof (screens plus paying advertisers).
2. Internal media (own content on the shop's TV) is the hook. External ads are the revenue.
3. Own the missing parts: ad demand and autonomous ad-agency flow, the reel pipeline (owner reels become the TV menu), the trendy Instagram-like menu design, QR recall and measurement.
4. Restaurants and cafes first for the menu use case.

## Business model (illustrative, from the original brief)
Advertiser rate about 20 rupees per hour per screen; partner payout 500 to 1,000 per month for the first 15 to 20 partners. Pilot: 5 to 10 partners in one neighbourhood and the first paying advertisers within 2 to 4 weeks. Example: 20 screens x 12 hours x 20 rupees x 30 days = 144,000 per month at **100% fill**; real fill rate and viewer attention are unknown.

## Ethics (not a ruling; a qualified scholar should confirm)
Keep a platform-level allowlist of ad categories (food, education, health, retail); doubtful categories stay out; shop approval does not remove the platform's own responsibility. Ask a scholar about ad content and the income model before launch.

## Open questions
- Can reels be read from an owner's connected Instagram (Graph API, business accounts) or must owners upload them?
- What does Gloo offer today; would they partner?
- Will neighbourhood advertisers pay for shop-TV slots; at what price and fill?
- Which player hardware (Android TV stick, Fire TV)?

## Technology decision: no Google Sheets as the database
An earlier prototype read menus from Google Sheets/CSV. Dropped: Sheets has low API quotas, no real access control, no realtime updates, no media handling and no schema safety (an owner can break a column), and it is poor UX for owners and slow for a TV player. Use a real database with a simple owner interface, and meet owners where they already are (Instagram reels, WhatsApp) instead of asking them to maintain a spreadsheet. The TV player should cache content for offline use.
