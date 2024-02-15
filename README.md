# FirstProyect-Steganography
This space houses the code and information to my foray into the fascinating world of steganography, where I explored the ability to hide information within other data to ensure confidentiality and security.
This Python script provides a simple implementation of image steganography, allowing you to encode and decode secret text within an image.

## Features

- **Text Encoding:** Embeds a given text message into the least significant bits of the pixel values of an input image.
- **Text Decoding:** Retrieves the hidden text from an encoded image.

## Usage

1. **Requirements:** Ensure you have OpenCV installed. You can install it using:

   ```bash
   pip install opencv-python
   ```

2. **Encode Text:**

   ```python
   import cv2

   # Load the cover image
   cover_image = cv2.imread("input_image.png")

   # Encode the secret text in the cover image
   secret_text = "This is the secret text"
   encoded_image = encode_text(cover_image, secret_text)

   # Save the encoded image
   cv2.imwrite("output_image.png", encoded_image)
   ```

3. **Decode Text:**

   ```python
   import cv2

   # Load the encoded image
   encoded_image = cv2.imread("output_image.png")

   # Decode the hidden text from the encoded image
   decoded_text = decode_text(encoded_image)

   # Print the decoded text
   print(decoded_text)
   ```

## Important Notes

- **Cover Image Size:** Ensure that the cover image is large enough to accommodate the entire secret text. An error will be raised if the cover image is too small.
