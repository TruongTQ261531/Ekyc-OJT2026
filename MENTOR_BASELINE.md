# eKYC course project baseline

Project snapshot: 2026-10-28.

- Application source: `ekyc/` and `web/`.
- Baseline validation: 110 Python tests and 15 frontend tests passed. One Python test requires the external MIDV images.
- On a source-only clone, run `python -m pytest --ignore=tests/test_manifest.py -q`; this does not replace the dataset integration check.
- Dataset metadata and quality labels are included. Raw document/selfie images, session data, caches, and personal debug images are excluded.
- The active quality checkpoint and its training report are included. Download the other public weights with `python -m ekyc.download_models` and `python -m scripts.setup_identity_models`.
- Third-party code and weights retain their source terms. See `models/*sources.json` and `docs/ocr_and_pad.md`; the repository MIT license does not relicense upstream assets.

This is a development prototype, not PAD certification. The legacy quality checkpoint has uncertain historical training provenance, so its reported metrics should be interpreted with that limitation.
