# Semantic Chunking

This project splits documents into semantically coherent chunks by:
- tokenizing text into sentences,
- embedding each sentence with a transformer model,
- splitting where adjacent sentence similarity drops below a threshold.

The main workflow is in `semantic_chunking.ipynb`.

## Repository Contents

- `semantic_chunking.ipynb` - notebook with the full chunking pipeline
- `document*.txt` - input documents used by the notebook
- `requirements.txt` - Python dependencies
- `chunking_output/` - generated chunked text files (after running)

## Quick Start

### 1) Clone the repository

```bash
git clone https://github.com/Bhuwann/semantic-chunking.git
cd semantic-chunking
```

### 2) Install dependencies

```bash
pip install -r requirements.txt
```

### 3) Run the notebook

```bash
jupyter notebook semantic_chunking.ipynb
```

Then run all notebook cells in order.

## Configuration

Inside the notebook, you can adjust:
- `MODEL_NAME` (embedding model),
- `SIMILARITY_THRESHOLD` (chunk split sensitivity),
- `DOC_FILES` (input file list).

## Output

When executed, the notebook writes chunked output files to:

- `chunking_output/<document_name>_chunks.txt`

Each chunk includes a header with sentence count and word count.

## Notes for Reproducibility

- Results can vary slightly across environments and package versions.
- For stricter reproducibility in the future, exact versions in `requirements.txt` will be needed.
