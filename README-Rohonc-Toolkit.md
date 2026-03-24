# Rohonc Toolkit

This folder contains reproducibility tools built from the uploaded Rohonc Codex research artifacts.

Important note:
- The uploaded lexicons and logs are the source material.
- These utilities operationalize that material into runnable scripts.
- They do **not** independently prove the decipherment; they implement the current project state.

Included tools:

1. `rohonc_decoder.py`
   - Decodes transcribed Rohonc symbol strings into Romanian transliteration or English glosses.
   - Input is a text transcription, not an image scan.

   Example:
   ```bash
   python rohonc_decoder.py "⊕-☦-△-✝ | ♔-✋" --mode english
   ```

2. `rohonc_frequency_analyzer.py`
   - Computes token, bigram, and trigram frequencies from a transcribed Rohonc text file.
   - Produces CSV outputs plus bar and Zipf plots.

   Example:
   ```bash
   python rohonc_frequency_analyzer.py --file sample_transcript.txt --outdir freq_demo
   ```

3. `data/historical_reference_index.json`
   - Structured index of historical figures, place names, sample texts, formulas, and timeline notes.

4. `data/illustration_text_concordance.json`
   - Structured concordance for the illustration entries explicitly documented in the uploaded Phase 4 log.
   - The uploaded log states all 87 illustrations were decoded, but only a subset are expanded line-by-line there.

Source files used:
- `ROHONC_CODEX_LEXICON_COMPLETE.json`
- `rohonc_codex_script_lexicon.json`
- `ROHONC_CODEX_PHASE_4_RESEARCH_LOG.md`
- `ROHONC_CODEX_PHASE_5_RESEARCH_LOG.md`
- `ROHONC_CODEX_PHASE_6_FINAL_VALIDATION.md`

Suggested next step if you want this expanded further:
- build an OCR-assisted manuscript page ingester once you have page-level symbol transcriptions or image annotations.
