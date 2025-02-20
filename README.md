# Sticker Grid Generator

This Python script generates a `.pptx` file with a grid of images (stickers) from a specified folder. The images are arranged in a grid layout while maintaining their original aspect ratio. The script automatically adds new slides if the number of images exceeds the grid size.

## Features

- **Grid Layout**: Arrange images in a customizable grid (e.g., 3x4, 5x5, etc.).
- **Aspect Ratio Preservation**: Images are resized to fit within the grid cells while maintaining their original aspect ratio.
- **Multiple Slides**: Automatically adds new slides if there are more images than can fit on a single slide.
- **Flexible Input**: Works with any folder containing images (e.g., `raw_pictures/cats/`).

## Requirements

- Python 3.x
- Libraries: `python-pptx`, `Pillow`

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/yourusername/sticker-grid-generator.git
   cd sticker-grid-generator
   ```

2. **Install Dependencies**:
   Install the required Python libraries using `pip`:

   ```bash
   pip install python-pptx pillow
   ```

   If using poetry `poetry`:

   ```bash
    poetry shell
    poetry install
   ```

3. **Prepare Your Images**:

   - Place your images in a folder inside `raw_pictures`.
     The Repo comes with its own images too.

   For example:

   ```
   raw_pictures/
   ├── cats/
   │   ├── image1.jpg
   │   ├── image2.png
   │   └── ...
   ├── dogs/
   │   ├── photo1.jpeg
   │   ├── photo2.bmp
   │   └── ...
   └── ...
   ```

## Usage

Run the script from the command line with the following arguments:

```bash
python create_sticker_grid.py <columns> <rows> <folder_name> <output_file>
```

### Arguments

- `<columns>`: Number of columns in the grid (e.g., `3`).
- `<rows>`: Number of rows in the grid (e.g., `4`).
- `<folder_name>`: Name of the folder inside `raw_pictures` containing the images (e.g., `cats`).
- `<output_file>`: Name of the output `.pptx` file (e.g., `output.pptx`).

### Example

To create a 3x4 grid of images from the `raw_pictures/cats/` folder and save it as `cats_stickers.pptx`:

```bash
python create_sticker_grid.py 3 4 cats cats_stickers.pptx
```

This will generate a `.pptx` file with the images arranged in a 3x4 grid. If there are more than 12 images, additional slides will be created.

## Output

The script generates a `.pptx` file with the following structure:

- Each slide contains a grid of images.
- Images are resized to fit within the grid cells while maintaining their aspect ratio.
- New slides are added automatically if there are more images than can fit on a single slide.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## Support

If you have any questions or need help, feel free to open an issue or contact me.

---

Enjoy creating your sticker grids! 🎉
