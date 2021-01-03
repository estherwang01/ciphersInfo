# Ciphers
Program which allows encryption and decryption with caesar shift ciphers, random substitution ciphers, vigenere ciphers, and RSA public/private key encryption.
This project was written as a part of Cornel University's CS2112. 
To view the full contents of the code, please email estherwang01@hotmail.com. Due to academic integrity concerns, I am not able to publically post the full repository.

# Cipher files
Ciphers can be saved to files in the following format: 
`
MONO \n
bcdefghijklmnopqrstuvwxyza
` 
For Caesar and monoalphabetic ciphers. 
`
VIGENERE \n
key
`
For Vigenere ciphers and
`
RSA \n
n \n
e \n
d
`
For RSA ciphers. 


# Running the program 
The basic format of the command is: 
java -jar <YOUR_JAR> <CIPHER_TYPE> <CIPHER_FUNCTION> <OUTPUT_OPTIONS>
Here, <YOUR_JAR> is a2main.jar. 

Cipher type: 
--caesar <shift_param>: Create a new Caesar cipher with the given integer shift parameter.
--random: Create a new monoalphabetic substitution cipher with a randomly chosen permutation of the alphabet.
--vigenere <key>: Create a new Vigenere cipher with the given keyword. The keyword is
given as a string of maximum length 128 characters.
--rsa: Create a new RSA cipher.
--monoLoad <cipher_file>: Load a monoalphabetic substitution cipher (caesar or random)
from the file specified.
--vigenereLoad <cipher_file>: Load a Vigenere cipher from the file specified.
--rsaLoad <file>: Create an RSA encrypter/decrypter from the public/private key pair stored
in the file specified.


Cipher functions: 
Next, at most one of the following options may also be specified by the user.
--em <message>: Encrypt the given string using the specified cipher scheme.
--ef <file>: Encrypt the contents of the specified file using the specified cipher scheme.
--dm <message>: Decrypt the given string using the specified cipher scheme.
--df <file>: Decrypt the contents of the specified file using the specified cipher scheme.


Output options: 
Finally, the user may add as many of the following output flags as they wish.
--print: Print the result of applying the cipher (if any) to the console.
--out <file>: Print the result of applying the cipher (if any) to the specified file.
--save <file>: Save the current cipher to the specified file.
