# Untrusted evidence isolation demo

Runnable educational demo/starter with synthetic examples.

Builds a structured request envelope separating fixed task instructions, the user’s question, and labeled untrusted source text. A conservative pattern scanner adds review flags without deleting source content. A separate tool gate rejects proposals whose provenance is source evidence and accepts only allowlisted trusted-user actions. These structural checks are educational; they do not prove that a language model will resist prompt injection, and the scanner deliberately has false negatives/positives. Trusted provenance must be assigned outside a model or document.

## Run

Python 3.10+; standard library only. From this directory:

```sh
python3 main.py
python3 main.py --help
python3 -m unittest -v
```

No network requests, credentials, or paid services are used. Any model/provider integration would be a separate adapter. Read `main.py` for the public functions and `test_main.py` for success/failure invariants. Fixture content is synthetic.

## Scope

This is an educational implementation with synthetic fixtures. Run the tests and inspect the documented limits before adapting it.

## Repository checks

```sh
python3 verify.py
```

This runs the isolated test suite, synthetic example, and CLI help. The included GitHub Actions workflow repeats these checks when the repository is published. No hosted CI result is claimed by the local verification report.
