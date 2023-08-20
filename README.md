# Untrusted evidence isolation demo

> **Disclosed reconstruction prepared on 24 October 2026.** The recorded Git dates are synthetic, not dates of past development. See [HISTORY.md](HISTORY.md).

This is an incomplete stage in a tutorial reconstruction of an already-completed reference implementation. Source, fixtures, tests, command-line behavior and verification are introduced in later stages. Only the final branch tip contains the complete documented package.

## Intended scope of the final example

Builds a structured request envelope separating fixed task instructions, the user’s question, and labeled untrusted source text. A conservative pattern scanner adds review flags without deleting source content. A separate tool gate rejects proposals whose provenance is source evidence and accepts only allowlisted trusted-user actions. These structural checks are educational; they do not prove that a language model will resist prompt injection, and the scanner deliberately has false negatives/positives. Trusted provenance must be assigned outside a model or document.

All examples are synthetic and educational. This reconstruction does not establish historical employment, deployment, usage, or production benchmarks.
