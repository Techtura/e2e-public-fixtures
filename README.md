# e2e-public-fixtures

Static, synthetic fixture files that Techtura's end-to-end test suites must fetch over
public HTTPS, because the system under test downloads them itself from an allowlisted
host (`raw.githubusercontent.com`).

Nothing in this repository is a real standard, control, credential, or customer
artifact. Every file is synthetic test data, safe to be public by construction.

| File | Consumer | Purpose |
|---|---|---|
| `oscal/e2e-catalog-4140.json` | InfraObserver dev — one-time OSCAL import into the dedicated `E2E-CATALOG-4140` framework | Provides a single synthetic control used as a reversible reclassification target by the platform-admin compliance E2E tests |

Files here are referenced by URL from test/infra code. Do not delete or move a file
without checking its consumers.
