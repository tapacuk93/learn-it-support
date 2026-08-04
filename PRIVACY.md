# Privacy Policy

**Last updated: 2026-08-04**

Learn Its (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Learn Its has no backend server of its own for lesson content, no user accounts, and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics, lesson history, bookmarks, or API keys.

## Your API keys

The app can use your own API key for Anthropic (Claude), Google Gemini, or an OpenAI-compatible provider — whichever you choose in Settings. You can also optionally add a key for ElevenLabs (spoken narration). Each key is:
- Stored only on your device, in the iOS/macOS Keychain — never synced or sent to any server we control.
- Sent only directly to that provider's own API (e.g. `api.anthropic.com`, `generativelanguage.googleapis.com`, `api.elevenlabs.io`, or the OpenAI-compatible endpoint you configure), never to us.

Usage of each key is billed directly by that provider to your own account.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [Google's privacy policy](https://policies.google.com/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)

Each provider publishes its own privacy policy on its website; check there for details on how it handles API traffic.

## aicoin Wallet (optional alternative to your own key)

Instead of a personal API key, you can choose "aicoin Wallet" in Settings and pay per lesson generation from a wallet balance. When this option is selected, your lesson-generation request is routed through our proxy at `aicoin.oeaio.com`, tagged with which AI provider it's for and your wallet ID, before being forwarded to that provider. If your wallet balance is insufficient, the app automatically retries the same request using your personal API key instead, if you've configured one.

## Lesson content

Whatever topic you type in is sent to your chosen AI provider (directly, or via the aicoin Wallet proxy above) to generate the lesson text. If you've added an ElevenLabs key, screen text is also sent to ElevenLabs to generate spoken narration.

Your subjects, lessons, history, and bookmarks are stored locally on your device only — there is no iCloud sync and no server-side copy. Uninstalling the app, or deleting it from a device, deletes that device's copy permanently.

## Images

To show an illustration alongside a lesson screen, the app either asks your configured AI provider to generate one, or looks up a real photo via Wikipedia's image search API (`wikipedia.org`), depending on which fits the topic and screen. Only the text needed to generate or find a matching image is sent — never your API key.

## Achievements export

The Achievements tab can export your learning activity as a file signed using Apple's App Attest, which cryptographically proves the export came from a genuine copy of the app running on your device. This attestation is generated and verified through Apple's own App Attest service and does not include any personal information beyond what's needed for that proof.

## Third parties

The only third parties involved are:
- **Anthropic, Google, or an OpenAI-compatible provider** — whichever you configure, to generate lesson text.
- **ElevenLabs** — only if you add a key, to generate spoken narration.
- **aicoin Wallet proxy** (`aicoin.oeaio.com`) — only if you choose that payment method, to relay generation requests to the underlying AI provider.
- **Wikipedia** (`wikipedia.org`) — to look up illustrative photos and full articles for lesson terms.
- **Apple** — App Attest, for signing achievement exports.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/learn-it-support/issues).
