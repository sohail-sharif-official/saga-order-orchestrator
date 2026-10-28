# Security & Isolation Model — Saga-Based Order Orchestrator (.NET 9)

## Security Controls
1. **Strict Tenant & Context Validation:** Every operation validates caller and tenant context before mutating or returning state.
2. **Idempotency & Replay Protection:** Mutating workflows guard against duplicate message replay and race conditions.
3. **Zero Embedded Secrets:** Repository contains strictly domain logic and synthetic test vectors with zero credentials or sensitive payloads.
