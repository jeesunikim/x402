---
'@x402/stellar': minor
---

Accept CAP-71 V2 address credentials (`SOROBAN_CREDENTIALS_ADDRESS_V2`) in the facilitator's auth-entry validation and in `gatherAuthEntrySignatureStatus`. Stellar Protocol 28 (testnet 2026-08-27, mainnet vote 2026-09-16) activates the V2 arm on the network, so clients can submit V2-signed auth entries; previously the facilitator rejected them (`invalid_exact_stellar_payload_unsupported_credential_type`) and signature-status gathering silently skipped them, so any V2 payment failed verification. Source-account and delegated (`addressWithDelegates`) credentials remain rejected.
