# Experiment 8: Decryption of Ciphertext Using Twofish Algorithm

## Twofish Algorithm Decryption Process

Twofish is a symmetric key block cipher that operates on 128-bit blocks and supports key sizes of 128, 192, or 256 bits. It uses a 16-round Feistel network, combining key-dependent S-boxes, an MDS (Maximum Distance Separable) matrix, modular arithmetic, and XOR operations to provide high security and strong diffusion. While encryption converts plaintext to ciphertext, the decryption process reverses these steps to recover the original data.

The decryption process begins with inverse key whitening, where the ciphertext is XORed with subkeys derived from the original key. Each round applies the inverse Feistel function, reversing the transformations applied during encryption, including operations on key-dependent S-boxes, modular addition, XOR, and rotations. The halves of the data are swapped appropriately, and the F-function is applied in reverse to ensure that all transformations are undone correctly.

Finally, the plaintext is recovered after the last round and post-whitening step. Twofish decryption mirrors the encryption structure, ensuring that only those with the correct key can retrieve the original data. Its design makes it highly resistant to attacks while maintaining efficiency in both software and hardware implementations, making it suitable for secure communication and data storage applications.