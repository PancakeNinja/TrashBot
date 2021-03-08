## Welcome to TRASH-Bot's Page!

TRASH-Bot is basically a GPT2-medium model fine-tuned on English Light Novel Titles!

# The Model

The model itself can be found [here](https://huggingface.co/Fabby/gpt2-english-light-novel-titles/tree/main)!

# The Program

Before you download the program, read the disclaimer!

DISCLAIMER: The generator is a 1.6GB .exe tested on Windows 10, that's it. I never designed it to be publicly released originally.
The user interface is not influenced by resizing the window for example. If you feel uncomfortable with downloading an .exe that is 1.6GB in size, I can completely understand that. **Normally** you'd do all the "heavy lifting" on a server and have users (you) interact with a website instead. **If** people really want TrashBot to be an online service that they can play around with in their browser instead of downloading a big .exe that contains the entire AI-model, let me know on Twitter.

If you execute the program, a terminal window will open and you will see it unpacking a lot of stuff into a temporary folder (which deletes itself once you close the program.). I kept that in __intentionally__ so users can see that the program is currently in start-up mode (and I couldn't be arsed to replace it with a simple loading bar, gome!).
The initial start-up will take around 30-60 seconds, depending on your computer.

Again, if you have any questions, feel free to message me and I will try to answer them!

The .exe can be downloaded [here](https://mega.nz/folder/BCZE3bxT#UbxrxNt4BfOheOQ2rLNRiA)!

# The Source Code

I will upload the source code to a Github repository once I cleaned it up a bit and made it easier to use with a terminal. You know what they say... _it works on my machine_

# Explanation Time!

## Input Fields
- Minimum Length (a number from 0 to 50) - The shortest possible letter combination(e.g. YUI = 3 letters)
- Maximum Length (a number from 50 to 250) - The longest possible letter combination
- TOP K (a number from 1 and 200) - Explanation below (6.)
- TOP P (a decimal from 0,01 and 1,00) - Explanation below (7.)
- Number of Titles Generated (a number from 1 and 100) - The amount of titles you want to generate
- Begin Titles With (A text) - The beginning word/sentence-piece you want the title to start with (e.g. Sword; Sword Art; Sword&Art)
- Generate Title - Hit that button to generate titles (After clicking you will have to wait around 10 seconds, there is no loading bar so don't panic!)

## TOP K
On average, your phone recommends you 3 word choices. That is a TOP-K value of 3. Those three choices on your mobile phone are the 3 MOST likely words to continue the sequence of words you have already typed into your phone (statistically speaking.).
For our AI it means that TOP-K represents the amount of words it will look at for every single step of the way (sorted by probability) and will pick one of these words (Just because a word has the highest probability from a statistical point of view, doesn’t necessarily mean that it’s the best choice. Language is a difficult topic after all).
In Layman’s terms, the higher the TOP-K value is, the more likely it is that the AI will go off-topic.

## TOP P
This is another way of determining which words to pick from. In addition to limiting/expanding the amount of choices the AI has with TOP-K, TOP-P sort limits the quality of the words. TOP-P is a value between 0.01 and 1.00(1% - 100%), and we are defining a cut-off probability. For example, if TOP-P is set 0,50, then all potentially chosen words have a cumulative probability of 50%.
Look at it this way: The higher the TOP-P value is, the more nonsensical and grammatically incorrect the generated sentences may become.

