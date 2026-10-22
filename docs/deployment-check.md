# Initial deployment check — October 22, 2026

- Published 22 original TXT files totaling 13,039,652 bytes, with edition source records and SHA-256 hashes in `manifest.json`.
- Checked all 22 deployed HTTP file URLs: each returned 200, matched the maintained original SHA-256, and supplied an appropriate cross-origin access header for the library reader.
- Public DNS returns `texts.bibliothecacatholica.com CNAME bibliothecacatholica.github.io`, with a 30-minute TTL. This replaces the earlier Squarespace forwarding rule. Main-domain and email records were preserved.
- At this initial check, GitHub Pages was still checking DNS and HTTPS was not available. An HTTP checksum check is not proof of HTTPS readiness. Recheck `https://texts.bibliothecacatholica.com/manifest.json` and enable Enforce HTTPS in this repository's Pages settings once the certificate is ready.
- Main-site PR #6 is merged and deployed. The reader requests the archive and falls back to its preserved local file; same-origin TXT download links stay available. The Confessions reader was verified in the production browser after deployment; `reader-verification.jpg` records that check. It does not claim that the browser loaded the archive over HTTPS.
- The main repository's `tools/verify_text_archive.py` defaults to HTTPS and checks every hosted file. Run it again after certificate provisioning. See `docs/PROJECT-REVIEW-2026-10-22.md` in the main repository for the project-wide assessment.
