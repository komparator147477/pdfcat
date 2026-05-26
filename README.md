# pdfcat

A tiny script to concatenate PDF files without recompression. Just glues them together.

## Install

Requires `uv`. Add this to `~/.zshrc`:

```zsh
pdfcat() {
    uv run --script ~/coding/pdfcat/pdfcat "$@"
}
```

## Usage

```bash
pdfcat output.pdf input1.pdf input2.pdf ...
```

The output extension is optional:

```bash
pdfcat merged part1.pdf part2.pdf
```

Progress is printed to stderr. Inputs are copied as PDF pages without rasterizing or recompressing page contents.

You can also run the script directly:

```bash
uv run --script ~/coding/pdfcat/pdfcat merged.pdf part1.pdf part2.pdf
```
