---
'@x402/stellar': minor
---

Accept CAP-71 V2 address credentials (`SOROBAN_CREDENTIALS_ADDRESS_V2`) in the facilitator's auth-entry validation and in `gatherAuthEntrySignatureStatus`. From Stellar Protocol 28 (testnet vote 2026-08-27, mainnet vote 2026-09-16), recording-mode simulation returns V2 credentials by default; previously the facilitator rejected V2 entries (`invalid_exact_stellar_payload_unsupported_credential_type`) and signature-status gathering silently skipped them, breaking exact-scheme Stellar payments on upgraded networks. Delegated (`addressWithDelegates`) credentials remain rejected.
