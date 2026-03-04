# pdfcat

A tiny script to concatenate PDF files without recompression. Just glues them together.

Usage:

```bash
uv run --script pdfcat output.pdf input1.pdf input2.pdf ...
```

Or add a shell function to make it available as a command:

```zsh
pdfcat() {
    uv run --script /path/to/pdfcat "$@"
}
```

Then:

```bash
pdfcat merged.pdf part1.pdf part2.pdf part3.pdf
```

Requires uv. Uses pypdf internally.
