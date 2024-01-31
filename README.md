# ASCII Image Converter

This is a small command-line tool to convert an image to ASCII art. It takes an image file as input and generates ASCII art on the console.

## Usage

```bash
go run main.go [image_file_path]
```

Replace `[image_file_path]` with the path to the image file you want to convert.

## Requirements

- Go 1.15 or higher

## How it works

1. The tool loads the specified image file using the `loadImage` function. It supports PNG and JPEG image formats.
2. It iterates over each pixel in the image and converts it to grayscale.
3. The grayscale value is used to determine the density value, which represents the ASCII character to be used.
4. The tool prints the ASCII character corresponding to the density value to the console.
5. The process is repeated for each pixel in the image until the entire image is converted to ASCII art.

## ASCII Density Chart

The following density chart is used to convert grayscale values to ASCII characters:

- `" "` - Lowest density (grayscale value 0)
- `"."` - Low density
- `"="` - Medium density
- `"!"` - High density
- `"░"` - Higher density
- `"▒"` - Even higher density
- `"▓"` - Very high density
- `"█"` - Highest density (grayscale value 255)

## Example

```bash
go run main.go example.png
```

Output:

<img src="assets/output.png" alt="simple output"></a>
...

## Author

- Ali (Real0x0a1)

---
