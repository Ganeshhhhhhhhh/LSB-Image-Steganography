# LSB-Image-Steganography
LSB (Least Significant Bit) Image Steganography is a method used to conceal secret data within the least significant bits of pixel values in an image. This project involves developing a C program to embed and extract secret messages in BMP (Bitmap) image files, chosen for their simplicity and lack of compression
Key Features

Image Handling:

1.Read and write BMP image files.
2.Extract and modify pixel data to embed the secret message.

Message Encoding:

1.Convert the secret message to a binary format.
2.Embed the binary message into the image's least significant bits of pixels.

Message Decoding:

1.Retrieve the binary message from the image's least significant bits.
2.Convert the binary data back to the original text.

Implementation Steps
Reading the BMP Image:

1.Open the BMP file in binary mode.
2.Read the 54-byte header to understand image dimensions and pixel data offset.
3.Store pixel data in an array.

Embedding the Message:

1.Convert the secret message into a binary string.
2.Loop through pixel data, replacing the least significant bit of each pixel with bits from the binary message.
3.Ensure the message fits within the available pixel data.

Writing the Modified Image:

1.Create a new BMP file.
2.Write the original header and modified pixel data.

Extracting the Message:

1.Open the modified image in binary mode.
2.Read the pixel data.
3.Extract the least significant bit from each pixel to reconstruct the binary message.
4.Convert the binary string back to text.
