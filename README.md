High Level Approach


At a high level, I was trying to create a wordle guesser that would start with the best first word. After doing a bit of research online, I saw that the best first word to guess in Wordle is "slate". So, I guessed with this word and essentially just filtered down the large list of words that was provided. As I filtered, I eliminate words and then the last word in the filtering has to be the correct word.

Challenges


The main challenges that I faced were getting the socket set up as I had never interacted with a socket before and actually set up a relationship between a client and a server. For me, it was a bit challenging to get started and actually learn all the things about a socket and how to open up sockets and ports. Another challenge was with establishing a SSL secured connection. This was difficult because I had to do lots of research on how these are created. The final challenge was working with the command line and the inputs of a command line. This is not something I had experience with before.

Guessing Strategy


As mentioned before, the first thing I did in my guessing strategy is that I guessed the word 'slate'. After this guess, I iterated through the 'marks' that were printed back via the server. If the mark was a 2, then I took note of this and filtered down all of the words in the project1-words list of only words that have the same letter in the same place as the guessed word. If the mark was a 1 in the 'marks' array, I filtered for words in the word list that contained this letter. If after guessing 'slate', there was no 1 or 2 in the 'marks' array, then I set the next guess to be any random word from the word list.
After filtering the word list from the first guess ('slate'), I then guesed a random word from this newly filtered list. I repeated this process of filtering and guessing a random word from the filtered list until I got the 'bye' message. At this point of getting the message, I wrote the message to secret_flags and broke the loop.

Testing Strategy


For my testing strategy, I relied on hardcoding and using print statements. At the begining, I was hardcoding the ports, hostnames, and usernames. I relied on hardcoding to ensure that I was able to get the result to be printed on the intended port, hostname, and username before I started abstracting and using argparse to get these values from the command line. I also heavily relied on print statements throughout and used them when I was writing loops and to see how many tries it took the algorithm to solve Wordle. Initially, I used a more brute-force approach and then eventually utilizied print staements to track the number of tries it took to solve and brought that number down.
