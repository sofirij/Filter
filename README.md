# Filter - BMP Image Filter

This project is a command-line tool for applying various filters to 24-bit uncompressed BMP image files. It supports grayscale, reflection, blur, and edge detection filters.

## Features

- **Grayscale**: Converts the image to shades of gray.
- **Reflect**: Mirrors the image horizontally.
- **Blur**: Applies a box blur to soften the image.
- **Edges**: Detects edges using the Sobel operator.

## Usage

```sh
./filter [flag] infile outfile
```

- `[flag]`:
  - `-b` : Blur
  - `-e` : Edge detection
  - `-g` : Grayscale
  - `-r` : Reflect
- `infile`: Path to the input BMP file.
- `outfile`: Path to save the output BMP file.

**Example:**
```sh
./filter -g images/tower.bmp images/tower-grayscale.bmp
```

## Building

To compile the project, run:

```sh
make
```

This will produce an executable named `filter`.

## File Structure

- `filter.c`: Main program logic and file I/O.
- `helpers.c`: Image processing filter implementations.
- `helpers.h`: Function declarations for filters.
- `bmp.h`: BMP file format structures.
- `images/`: Sample BMP images for testing.

## Requirements

- C compiler (e.g., `clang` or `gcc`)
- Make

## Notes

- Only 24-bit uncompressed BMP 4.0 files are supported.
- The program will report errors for unsupported formats or incorrect usage.