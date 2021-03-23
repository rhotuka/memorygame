# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Raunak Hota**

Time spent: **1** hours spent in total

Link to project: (insert your link here, should start with https://glitch.com...)

## Required Functionality

The following **required** functionality is complete:

- [✓] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [✓] "Start" button toggles between "Start" and "Stop" when clicked.
- [✓] Game buttons each light up and play a sound when clicked.
- [✓] Computer plays back sequence of clues including sound and visual cue for each button
- [✓] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [✓] User wins the game after guessing a complete pattern
- [✓] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [ ] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
- [ ] More than 4 functional game buttons
- [✓] Playback speeds up on each turn
- [ ] Computer picks a different pattern each time the game is played
- [ ] Player only loses after 3 mistakes (instead of on the first mistake)
- [ ] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

https://i.imgur.com/JjPcV3u.gif

https://i.imgur.com/4ijPCH4.gif

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.

   I did not use any external resources.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

   The hardest part about this submission was implementing the logic for the guess function as it incorporates several of the variables and functions from the previous parts.
   Most notably, I had to use guessCounter as an index for the pattern array to receive a value that is then compared to the button parameter. This was done to determine
   whether the guess of a given button was correct at the current point in the sequence. I overcame the difficulty thanks to the flowchart which translates well to a series
   of if/else statements, incrementations, and function calls.

   Another challenge I overcame was when I added the additional feature of having the pattern speed up as you go. I had changed clueHoldTime from a constant to a variable and
   decremented it in playClueSequence as per the instructions. However, I had initially put it inside the for loop and noticed that after a certain point the sequence would
   terminate prematurely. I fixed this issue by realizing that the decrement is supposed to occur after every sequence instead of after each step of the sequence, and so I
   moved the clueHoldTime statement outside of the for loop. Additionally, I made sure to set clueHoldTime back to 1000 in the startGame function as it was no longer a constant.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

   One question I have about web development is how security features are implemented into the website. When websites store things such as usernames and passwords and then verify
   them, what kind of code is used? Is this done via JavaScript or using some external server or database? Another question I have is how webpages can differ between desktop and
   mobile views. Can a webpage have two separate sets of HTML depending on the method of access, are there special mobile HTML tags, or are most of the features simply scalable
   by default? My last question is what if the site’s CSS specifies only fonts that the user does not have? What would display then?

4) If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)

   If I had a few more hours to work on this project, I would spend them implementing the remainder of the optional features. Among them, the most interesting to me are the
   randomized secret pattern, which I could implement by populating the pattern array with numbers from Math.random, and the ticking clock, which would require reading into
   the interval methods. I could potentially go beyond the suggestions of the optional features by adding difficulty buttons that configure settings accordingly. For
   instance, easy difficulty could have 3 strikes while hard difficulty has more buttons with faster sequences and time limits.

## License

    Copyright Raunak Hota

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
