# AES-128 symmetric key cipher
--------------------------

this Project Experiments AES-128 symmetric key cipher using Python.
Using AES Python libraries to decrypt an encrypted text in ECB mode using a 128-bit key, ECB mode is the simplest mode of the encryption modes. 

## Requirement 
- Python 3.x or Google Colab
- Module pycrypto 

## Setup
-----------------------------
* #### Installing Dependencies: 
    Install Python Package Installer In case of unavailability
    `sudo apt update`
    `sudo apt install python3-pip`
    `pip3 --version`
    Install the pycrypto Dependency. 
    `!pip install pycrypto`

## Description 
---------------------------
* #### Part 1: decrypt
    a program that uses AES-128 to decrypt a message with 128-bit key. 
    * ##### Usage: 
         Advanced Encryption Standard: is a symmetric block cipher standardized.
        ```
        from Crypto.Cipher import AES 
        cipher = AES.new(key, AES.MODE_ECB)  
        ```
    * ##### Compiling instruction: 
        the compiling instruction work is done on Google Colab.
      1- Open  `decrypt.ipynb`, using the google Colab. by clinking on File in tool bar menu and clicking on upload notebook.
      2- Upload the files `key.dat` and `ciphertext.dat` to google colab, by clicking on left most third option File menu icon on the colab page and get upload browser files, or Upload files by mounting the Drive as  [Here](https://colab.research.google.com/notebooks/io.ipynb).
      3- Run the program, by selecting the cell and press `{Ctlr + ENTER}` keys, or follow the following [instruction](https://colab.research.google.com/github/rpi-techfundamentals/spring2019-materials/blob/master/01-overview/01-notebook-basics/03-running-code.ipynb#scrollTo=c_QmtgdfjFkD).
      4- the code will generate a new `plaintext.dat` file that contain a decrypted text. 


* #### Part 2: findk
    a program that uses "brute force" to decrypt an encrypted message, where the secret key is missing the last 4 bytes. the program will find the missing secret key and decrypt the encrypted text. 
    * ##### Usage: 
         Advanced Encryption Standard: is a symmetric block cipher standardized.
        ```
        from Crypto.Cipher import AES 
        # key is 16 byte secret key
        cipher = AES.new(key, AES.MODE_ECB)  
        ```
         Itertool: is a fast and memory-efficient Python module that provides various functions to produce complex iterators.
         
        ``` 
        import itertools 
        for a, b, c, d in itertools.product(range(255), repeat = 4):
        ```
         timeit: is a module that provides a simple way to measure a program's execution times.
        ``` 
        import timeit
        start = timeit.default_timer() # start Timer 
        # Program
        stop = timeit.default_timer() # stop Timer 
        ```
        
    * ##### Compiling instruction: 
        the compiling instruction work is done on Google Colab.
      1- Open  `findK.ipynb`, using the google Colab. by clinking on File option in tool bar menu and clicking on upload notebook.
      2- Upload the files `partial-key.dat` and `ciphertext2.dat` to google colab, by clicking on left most third option File menu icon on the colab page and get upload browser files, or Upload files by mounting the Drive as  [Here](https://colab.research.google.com/notebooks/io.ipynb).
      3- Run the program, by selecting the cell and press `{Ctlr + ENTER}` keys, or follow the following [instruction](https://colab.research.google.com/github/rpi-techfundamentals/spring2019-materials/blob/master/01-overview/01-notebook-basics/03-running-code.ipynb#scrollTo=c_QmtgdfjFkD).
      4- The missing secret key and the decrypted text and the time it took to solve the program will be displayed asynchronously.

> Note: the program is in python language.
