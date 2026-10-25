# Privacy Policy

**Last updated: 2026-10-23**

All AI Learn (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

All AI Learn has no user accounts and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics, lesson history, or bookmarks.

## How AI requests work (no personal API keys)

The app does **not** ask you for your own AI provider API key. Every request to generate a lesson, its illustrations, or narration audio is sent to our own relay server, **aicoin-proxy**, at `proxy.aicoin.oeaio.com`. aicoin-proxy adds its own paid credential for whichever AI provider the request is for, forwards your request to that provider, and returns the response — you never handle or expose a provider credential, and we never see one of yours because there isn't one.

**AI calls are paid for in AICoin, priced by what they cost to run.** Each lesson screen, illustration, or narration clip costs from 1 AICoin — a longer one costs more — debited from your AICoin wallet at the moment of the call.

### What the relay keeps, and what the providers keep

- **The relay does not log or store what you send or get back** — no topics, lesson text, illustrations or audio. For each request it keeps only a line of metadata: the time, the kind of request and the provider's endpoint (without query parameters), which provider, your wallet address, the result status, sizes, timings, and the AICoin charged. Those logs rotate and are capped in size.
- **The AI providers do receive your requests**, and keep them under their own retention policies: [Anthropic](https://www.anthropic.com/legal/privacy), [OpenAI](https://openai.com/privacy), [Google](https://policies.google.com/privacy), [Mistral AI](https://mistral.ai/terms#privacy-policy), [ElevenLabs](https://elevenlabs.io/privacy).
- **Nothing you send is stored on a provider where other users could reach it.** Every user's requests go through the same provider accounts, so the relay only forwards requests to providers' generation endpoints and refuses the provider features that store things on the account — file uploads, batch jobs, stored responses and conversations, caches, and generation history.

## AICoin wallet

Your wallet is identified by a keypair generated and stored on your device (Keychain) — we never see your private key. There are two ways to get AICoin:
- **Buy it**, via an in-app purchase processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing and receipts directly. A successful purchase credits your wallet by contacting `proxy.aicoin.oeaio.com` with Apple's own signed proof of purchase.
- **Receive a transfer** from another AICoin wallet (yours on another device, or someone else's).

Your wallet address and balance are stored server-side at `proxy.aicoin.oeaio.com` (see the [aicoin.oeaio.com](https://aicoin.oeaio.com) site for how the ledger works) — this is necessary for the wallet to function across devices and to debit calls, and is not linked to your name, email, or Apple ID.

## Lesson content

Whatever topic you type in is relayed (via aicoin-proxy) to the AI provider you've chosen — Claude (Anthropic), OpenAI, Gemini (Google), or Mistral — to generate the lesson text and illustrations. If narration is enabled, screen text is also relayed to ElevenLabs to generate spoken narration.

Your subjects, lessons, history, and bookmarks are stored locally on your device only — there is no iCloud sync and no server-side copy. Uninstalling the app, or deleting it from a device, deletes that device's copy permanently.

## Images

To show an illustration alongside a lesson screen, the app either asks the AI provider (via the relay) to generate one, or looks up a real photo via Wikipedia's image search API (`wikipedia.org`), depending on which fits the topic and screen. Only the text needed to generate or find a matching image is sent.

## Achievements export

The Achievements tab can export your learning activity as a file signed using Apple's App Attest, which cryptographically proves the export came from a genuine copy of the app running on your device. This attestation is generated and verified through Apple's own App Attest service and does not include any personal information beyond what's needed for that proof.

## Third parties

The only third parties involved are:
- **aicoin-proxy** (`proxy.aicoin.oeaio.com`, operated by us) — relays every AI request below with its own paid credentials and debits your wallet; see [aicoin.oeaio.com](https://aicoin.oeaio.com) for how it works.
- **Anthropic, OpenAI, Google, or Mistral** — whichever you've chosen, to generate lesson text and illustrations.
- **ElevenLabs** — only if narration is enabled, to generate spoken audio.
- **Wikipedia** (`wikipedia.org`) — to look up illustrative photos and full articles for lesson terms.
- **Apple** — App Attest (for signing achievement exports) and StoreKit (for AICoin purchases), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/learn-it-support/issues).
