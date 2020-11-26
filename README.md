# topdf

`topdf` is a wrapper around [pandoc](https://pandoc.org/) that makes it even easier to convert various document formats to PDF from the command line. I created this because I prefer to do most of my writing in Markdown, but PDFs are easier to turn in for school assignments.

## Requirements

You'll need to install [pandoc](https://pandoc.org/installing.html) and [wkhtmltopdf](https://wkhtmltopdf.org/) to use `topdf`.

## Installation

Just download the `topdf` script and start using it! If you want to easily use it from anywhere, just add the directory containing `topdf` to your path. (Don't know how? Check out [these instructions](https://gist.github.com/nex3/c395b2f8fd4b02068be37c961301caa7).)

## Usage

```bash
$ topdf [OPTIONS] INPUT_FILE -- [PANDOC_OPTIONS...]'
```

Options:

- `--html`: Use wkhtmltopdf as the PDF engine
- `--latex`: Use pdflatex as the PDF engine

`PANDOC_OPTIONS` will be passed directly to `pandoc`.

> This assumes you've added `topdf` to your path, as explained in the installation section.

Check out [pandoc's documentation](https://pandoc.org/MANUAL.html) for information about available options. Also note that `topdf` already uses some options by default - take a look inside the script to see which ones.

> Handy tip: `topdf` will detect a `style.css` file in the working directory and pass it to `pandoc` with the `--css` option.

