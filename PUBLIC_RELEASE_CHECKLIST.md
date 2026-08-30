# OnRecord public-release checklist

**Release verdict: HOLD — documentation-only public staging.**

The repository is public with README documentation and referenced public-facing assets only. The application source remains local and must not be pushed until the source-release gates below are complete.

## Evidence already present

- [x] Separate local Git boundary; it no longer inherits the parent home-directory repository.
- [x] Plain-language product framing and sponsor roles.
- [x] System map with no embedded script, external image, or local file reference found in the scanned SVG.
- [x] `.gitignore` excludes real environment files, generated runs, private indexes, transcripts, and video/audio.
- [x] `.env.example` contains names only; no credential values.
- [x] Reusable `video-vault-studio` baseline reverified: 37 tests passed and the fixture demo completed on 30 Aug 2026.
- [x] Reused source repositories and pinned commits named in the README.

## Required before a public source-code push

- [ ] Import the smallest reviewed application slice into this repository; do not copy `.git`, `.env`, outputs, private media, or local indexes.
- [ ] Reconcile any concurrent source edits before pinning or copying. `video-vault-hacksprint/app/models.py` was modified during this audit.
- [ ] Add a synthetic multi-episode fixture that contains no third-party media or transcript text.
- [ ] Make `make setup && make demo` pass from a clean clone with no SSD and no credentials.
- [ ] Make `make run` start the local UI at the documented address.
- [ ] Run OpenAI + Parallel once and commit a redacted receipt containing model IDs, timings, costs, citations, validation, and failure/abstention state—never secret values.
- [ ] Run Daytona live once and commit a current redacted receipt proving parent/children lifecycle, execution source, fork semantics, cleanup, and reconcile-to-zero.
- [ ] Capture one reviewed screenshot with no browser chrome, filesystem paths, emails, account names, tokens, private media, or unrelated windows.
- [ ] Record and verify the 90-second demo link in a logged-out/private browser session.
- [ ] Replace every HOLD or pending statement in `README.md` only when matching evidence exists.
- [ ] Verify the public claims and add direct source links for the 20VC episode count and Harry Stebbings' public asks.
- [ ] Complete a human media-rights review for screenshots, clips, quotes, transcripts, guest names, and logos.
- [ ] Choose a license deliberately; do not add one by default.
- [ ] Add contributor and reused-code attribution, including exact source commits and material changes.
- [ ] Run a final secret scan over tracked files and Git history.
- [ ] Check the exact repository root, branch, status, remote, upstream, GitHub visibility, and collaborator access before push.

## Public usability gate

A judge with a clean machine must be able to answer all five questions in under two minutes:

1. What does OnRecord do?
2. Why does the catalogue-wide input matter?
3. Why are Daytona, OpenAI/Codex, and Parallel causally necessary?
4. What was built during the event versus reused?
5. Can I run the synthetic demo without private media, an SSD, or API keys?

If any answer is unclear or unverified, keep the release on HOLD.
