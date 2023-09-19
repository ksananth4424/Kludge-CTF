## GetTheSequenceRight

Description - Get it right, and also try to see through!

# Walkthrough

So, we are given two files one an image and the other an exectable file.

First we check the image which seems like a maze.
When we try the following command:

        $ strings Test.png 

We find two sentences which are legible, whch are:

        Did you get the sequence?
        RC2 it!!

Which suggests that we need to get the sequence of directions of the maze and encrypt it in RC2.

Proceeding, we have the executable file which on running we get:

        Enter the solution:

Where we provide our encrypted answer to the maze.
Doing which we get:

        Flag?? not so fast :))

Hmm, interesting.
Next we open the same executable file in ghidra and analyse the same
we find that it is calling the wrong function which we correct and run the file again doing which we get a key which seems like encrypted in base64.
Which we can decrypt and get the flag. :))