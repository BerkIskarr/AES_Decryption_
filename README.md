# AES_Decryption

## Overview
This project contains a Python program that decrypts an encoded message using a method based on the AES algorithm. The program takes a list of encrypted integers and a decryption key, then applies several steps to decrypt the message. The code contains helper functions to manipulate byte-level operations such as XOR operations, nibble extraction, and S-Box transformations.

## Files in the Project
### dec_decrypt_aes_part.py: The main Python script containing the decryption logic.
### README.md: Documentation for using and understanding the decryption program.
## How to Run the Program
The decryption script can be run from the command line with the following syntax:

```bash
python dec_decrypt_aes_part.py [option]
```
Where [option] can be one of the following values:

a: Decrypt the given text using the provided key.
b: Demonstrates the dec_xor function, showing the XOR operation between two byte values.
c: Demonstrates the dec_swap_last_two function by swapping the last two nibbles of a byte.
d: Demonstrates the dec_s_box function by applying the S-Box transformation to a byte.
e: Demonstrates the dec_subtract_last_two_first_two function by subtracting the last two nibbles from the first two.
## Example Execution
``` bash
python dec_decrypt_aes_part.py a
```
The above command will decrypt the provided list of integers (text) using the given key and output the decrypted string.

## Decryption Process Overview
### XOR Operation:

The list of encrypted integers (text) is XORed with the key to initiate the decryption process.
### Nibble Manipulation:

Each byte (8-bit) is split into four nibbles (2-bit each) for processing. These nibbles are manipulated with operations like swapping, S-Box transformations, and subtraction.
### S-Box Transformation:

The nibbles are passed through an S-Box transformation function that replaces specific values based on predefined rules to enhance security.
### Swapping and Subtracting:

Swapping and subtracting operations are performed on the nibbles to further reverse the encryption process.
### Reconstruction of Decrypted Message:

Once the nibbles are manipulated, they are combined back into bytes, which are then converted into readable characters, resulting in the final decrypted string.
## Functions Breakdown
dec_decrypt(): Main function that orchestrates the decryption process using the helper functions.

dec_convert_bytes_to_nibbles(): Splits a byte into four nibbles.

dec_byte_to_nibbles(): Converts a byte into a 4-element bytearray where each element represents a nibble.

dec_convert_nibbles_to_bytes(): Combines four nibbles back into a single byte.

dec_convert_nibbles_to_byte(): Converts a quadruple of nibbles into a single byte.

dec_decrypt_byte_as_nibbles(): Performs the decryption for a byte by manipulating the nibbles with XOR, swap, S-Box, and subtraction operations.

dec_xor(): XORs two sets of nibbles and returns the result.

dec_swap_last_two(): Swaps the last two nibbles in a byte.

dec_s_box(): Performs S-Box transformation on the nibbles.

dec_subtract_last_two_first_two(): Subtracts the last two nibbles from the first two using modulo 4.

dec_convert_bytes_to_string(): Converts a list of bytes into a readable string.
