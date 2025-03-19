# ECE243_ImageConverter
Convert an image into C code and draw it on the VGA.

# User Guide for This Program

## 1. Install Dependencies
Before running this program, ensure the following Python libraries are installed:
- numpy
- opencv-python
- pyperclip

You can install them using the following command:
```bash
pip install numpy opencv-python pyperclip
```

## 2. Prepare the Input Image
Place the image file you want to convert in the `images` folder within the program directory. Ensure the file path and name match the `file_name` parameter in the `convert_img` function.

## 3. Modify Parameters
Open the program file `/c:/path/to/your/folder/convert_img.py`. In the `if __name__ == '__main__':` block, modify the following parameters:
- `file_name`: Path to the input image (relative to the program directory).
- `img_name`: Name of the C-language array after conversion.
- `width`: Adjusted width of the image (in pixels).
- `height`: Adjusted height of the image (in pixels).

## 4. Run the Program
Run the program in the terminal or command line:
```bash
python convert_img.py
```

## 5. Get the Output
After running, the program will copy the generated C-language array and drawing function code to the clipboard. Open any text editor (e.g., Notepad) and paste the clipboard content to view the generated code.

## 6. Use the Generated Code
Copy the generated C-language code into your project. Use the `plot_image_<img_name>` function to draw the image and the `erase_image_<img_name>` function to erase it.

### Notes:
- The input image will be resized to the specified width and height, which may cause distortion.
- The generated C-language array uses 16-bit unsigned integers to represent colors in RGB565 format.
