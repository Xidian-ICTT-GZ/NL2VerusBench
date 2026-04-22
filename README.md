# Anonymized Benchmark Dataset for Verified Program Synthesis

This repository contains an anonymized benchmark dataset for research on program verification and natural language to verified code generation.

Each sample in the dataset includes:

- a unique sample identifier,
- a natural language problem description,
- a target function signature,
- a difficulty category,
- and a Verus implementation that has been verified successfully.

This repository is prepared for anonymous review. No author-identifying information is included.

## Purpose

The dataset is intended for academic research on:

- verified program synthesis,
- formal verification,
- natural language to code generation,
- benchmark construction and analysis,
- and evaluation of models that generate or reason about verified code.

## Data Format

Each benchmark instance is stored as a structured record with the following fields:

- **sample_id**: a unique identifier for the task
- **description**: a natural language specification of the task
- **function_signature**: the target function signature
- **category**: the task category or difficulty label
- **verified_verus**: a Verus implementation that satisfies the specification

A typical record has the following structure:

```json
{
  "sample_id": "DAFNY2VERUS-COLLECTION_1",
  "description": "Given a non-empty array of 32-bit signed integers, return an index of a maximal element. ...",
  "function_signature": "fn max(a: &Vec<i32>) -> usize",
  "category": "Loops",
  "verified_verus": "use vstd::prelude::*; ..."
}
