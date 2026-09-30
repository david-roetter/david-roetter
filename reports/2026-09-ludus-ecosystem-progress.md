# Ludus ecosystem: the first playable Flutter build is published

**Progress report · updated 30 September 2026 · David Rötter**

Over the past two weeks, Ludus, Rendert, PeaceGPT, and PeachEx have moved from overlapping ideas toward identifiable components. A private playable Ludus web build is now available to the project owner; the next goal is to gather real playtest feedback. Revenue, water savings, and token use are aims to test; none is an observed outcome yet.

## What exists today

| Project | Evidence-backed status | Next milestone |
| --- | --- | --- |
| **Ludus / LVDVS** | The supplied season game and LVDVS v0.2 Chronicle lab are combined in one Flutter client. Android, iOS and web platform projects are included. With Flutter 3.47.3 / Dart 3.13.3, 14 tests passed, analysis reported no issues, and the release web build compiled and published successfully. Source is pushed in [PR #1](https://github.com/david-roetter/ludus/pull/1). | Playtest the published web version, finish the Android workflow, and arrange Apple signing for native iPhone/iPad testing. |
| **Rendert / GITAGGROECONOMICS** | The public [repository](https://github.com/roetterrorbitics-cpu/GITAGGROECONOMICS) describes a SaaS foundation with account UI, authentication, payments integration, and a planned Apple client. The supplied bundle contains two distinct workspace and arena patches, described there as locally tested but unpushed. Its arena ledger and PCH economy are simulations. | Review and apply the patches in the correct repository, deploy a preview, and validate real account and subscription flows before charging anyone. |
| **PeaceGPT / Inquirize** | A [draft security PR](https://github.com/david-roetter/PeaceGPT-Demo/pull/17) records passing checks for request handling and CI, while explicitly leaving identity, access control, tenant isolation, persistence, monitoring, rollback, and secrets-history review for a production release. | Close one release boundary at a time, starting with authenticated ownership and isolation of stored data. |
| **PeachEx** | Source files supplied on 29 September define a fixed 100 million PCHX supply minted to a treasury and a single Genesis NFT with on-chain SVG metadata. A symbol search through Blockscout returned no PCHX match on Ethereum Sepolia in this session. | Build and test the contracts, identify a treasury and deployment address, and verify any testnet transaction before calling it deployed. Public sale requires a separate legal and product decision. |

These are complementary projects, not one integrated live product. The useful connection is a clear boundary: game clients produce events, trusted services handle accounts and AI provider calls, and any future blockchain component must prove a need beyond the existing simulated ledger.

## Why this matters to testers

LVDVS has a concrete first loop: manage a small school, make a weekly choice, watch a fight resolve, and see the cost in the ledger. That loop can be tested without requiring a subscription, wallet, token, or AI narration. If players enjoy it, Rendert can later offer creation tools and an optional arena experience. PeaceGPT’s security work supplies a reusable discipline for identity and safe releases; it is not a claim that the products already share a production backend.

## A credible route to traction

1. **Playtest the published prototype.** The release web build is published. Start with one in-game week and the Chronicle recruit/fight/save loop, then check the Android build workflow. Native Apple delivery still needs signing or TestFlight.
2. **Ask for observable feedback.** Invite testers to finish one in-game week. Track starts, completed weeks, failures, and an optional short comment. Publish aggregate results only after actual testing.
3. **Test a simple business offer.** Consider optional paid creator tools or an app subscription after the free loop works. State pricing and platform terms clearly. Do not represent simulated PCH as spendable cryptocurrency or promise earnings to players.
4. **Measure the environmental idea.** The aspiration to save water needs a baseline, a causal mechanism, and a measurable unit. A first experiment could compare resource use for a specific workflow before and after a digital alternative; without that evidence, it remains a project goal.

**Invitation:** Developers, designers, playtesters, and prospective partners can follow the linked repositories and help test the game loop as access is arranged. Feedback on the game loop, accessibility, account safety, and viable use cases is especially valuable.

## Evidence and limits

This report uses the attached 29 September project bundle, the newly supplied `ludus_flutter.zip` source snapshot, PeachEx source files, the two public repository descriptions, the draft PeaceGPT PR, the connected Supabase project inventory, Render build notices, and a scoped Ethereum Sepolia token-symbol search. The Flutter ZIP passed an archive integrity check. The combined client passed 14 Flutter tests, clean analysis and release web compilation on 30 September; the private web deployment succeeded. Browser QA on physical devices and native Android/iOS delivery are not yet verified. The Supabase inventory returned no projects for this connected account; that does not establish the absence of projects in other accounts. The Blockscout symbol search is not a definitive deployment search without a contract address. The project bundle includes earlier claims of live services, but the current playable web release is supported by fresh build and deployment results, while other service uptime is not inferred from those older notes.
