Program source reference URL:
https://stackoverflow.com/questions/42651623/microbit-python-rock-paper-scissors-debugging


Program (made by Trevon and Aidan)  description:


Modifications made:

          -Changed the images created when rock, paper or scissors were output (represents what was played by Microbit while you authentically play your move using your hand or simply on your head) to animations.
           -Output a sound when you lost or sound when you won the game

BBC sensors used:

            -The A&B buttons were used to input to the computer whether you won or lost
            -accelerometer 


Testing information:

          - Played game ourselves, and had a volunteer play our game then give feed-back, it worked perfectly as planned on our test runs. 
-most of the errors came from mistakes with syntax, primarily when calling a function such as a sound effect or one of the animations we designed, these all had to be spelled, copied and used correctly, to fix these errors we placed the code into Mu editor where thee software then helped identify syntax errors. 


Ideas for extending the project:
           -Could have the Microbit display instructions (for how to play the game) when first run. 
            -Could have Microbit play sound effects for the various choices it plays (rock, paper or scissors) in order to make the animations even more clear and realistic. 


Final working code:
```python

from microbit import *
import random
import music
count = 0

paper1 = Image("00000:"
              "00000:"
              "00900:"
              "00000:"
              "00000")

paper2 = Image("00000:"
              "00300:"
              "03930:"
              "00300:"
              "00000")

paper3 = Image("00000:"
              "09990:"
              "09990:"
              "09990:"
              "00000")

paper4 = Image("33333:"
              "39993:"
              "39993:"
              "39993:"
              "33333")

paper5 = Image("99999:"
              "99999:"
              "99999:"
              "99999:")
   
paper6 = Image("00000:"
              "00000:"
              "00000:"
              "00000:")   

rock1 = Image("00099:"
              "00999:"
              "00000:"
              "00000:"
              "00000")

rock2 = Image("00000:"
              "00990:"
              "00992:"
              "00090:"
              "00000")

rock3 = Image("00000:"
              "00000:"
              "09990:"
              "09900:"
              "00000")

rock4 = Image("00000:"
              "00000:"
              "90000:"
              "99000:"
              "99000")

rock5 = Image("00000:"
              "00000:"
              "00000:"
              "00000:"
              "90000")

rock6 = Image("00000:"
              "00000:"
              "00000:"
              "00000:"
              "00000")

scissor1= Image("00900:"
                "00900:"
                  "00900:"
                  "09090:"
                  "00000")

scissor2= Image("90009:"
                  "09090:"
                  "00900:"
                  "09090:"
                "00000")

all_scissors= [scissor1, scissor2, scissor1, scissor2, scissor1, scissor2, scissor1, scissor2]
all_rocks= [rock1, rock2, rock3,rock4, rock5, rock6]
all_papers= [paper1,paper2,paper3, paper4, paper5, paper6,paper1,paper2,paper3, paper4, paper5, paper6]
while True:
    while True:
        if accelerometer.is_gesture("shake"):
            display.clear()
            choice = random.randint(0, 2)
            if choice == 0:
                display.show(all_rocks)
                break
            elif choice == 1:
                display.show(all_papers)
                break
            else:
                display.show(all_scissors)
                break
    while True:
        if button_a.is_pressed():
            count = count + 1
            music.play(music.POWER_UP)
            display.scroll(str(count))
            break
        elif button_b.is_pressed():
            count = count - 1
            music.play(music.POWER_DOWN)
            display.scroll(str(count))
            break
```
Program source reference URL:
https://stackoverflow.com/questions/42651623/microbit-python-rock-paper-scissors-debugging


Program (made by Trevon and Aidan)  description:


Modifications made:

          -Changed the images created when rock, paper or scissors were output (represents what was played by Microbit while you authentically play your move using your hand or simply on your head) to animations.
           -Output a sound when you lost or sound when you won the game

BBC sensors used:

            -The A&B buttons were used to input to the computer whether you won or lost
            -accelerometer 


Testing information:

          - Played game ourselves, and had a volunteer play our game then give feed-back, it worked perfectly as planned on our test runs. 
-most of the errors came from mistakes with syntax, primarily when calling a function such as a sound effect or one of the animations we designed, these all had to be spelled, copied and used correctly, to fix these errors we placed the code into Mu editor where thee software then helped identify syntax errors. 


Ideas for extending the project:
           -Could have the Microbit display instructions (for how to play the game) when first run. 
            -Could have Microbit play sound effects for the various choices it plays (rock, paper or scissors) in order to make the animations even more clear and realistic. 
