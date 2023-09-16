# Introduction

Flag format flagCTF{}

Question:

          We all know John Wick, Don't we?

Attachments:

          problem.jpg

Hint: 
          
          -> What does the file extension say?
          -> Try it the other way.

As we can see that we are given a .jpg file. Which suggests it might be some sort of steganography question (could be something else also).
The question also points to "John Wick", this suggests it might be a theme based question :)).

# Writeup

The file given in the question is as we can see a .jpg file.
But, when we try to open it, it can not be opened.

So, Let's try to put in the .jpg magic numbers in using hexedit feature in the ubuntu terminal

    $ hexedit problem.jpg
    The magic numbers of a .jpg file is FF D8 FF E0  

Then, try to find for the hint in strings, find the solution for the hint given.

    $ strings problem.jpg
    We have the hint "Get this man a __!!"

Use this hint to extract data from the file.
We can use steghide to extract the same!

    $ steghide extract problem.jpg

Open the file extracted and decode the text given to get the flag.
Use the hint while decoding.

    Hint points to: focus, commitment and will
    Use vigenere cipher and apply the words step by step!

All The Best!!
