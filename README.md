# Hacktoberfest-project
This is an old microbit project of mine and i would really appreciate if anyone could maybe take a look at it and try to improve my code in any way. Thanks! :>(Btw sorry if its really flawed haha its my first project)


L.A.S(Lap Assist System)


In Motorsport events such as F1 or the WRC, drivers drive constantly at high speeds and are distracted by looking away from the front to see what lap of the race they are on. This distracts them and as every millisecond matters in events like F1, their times may be compromised or even worse, they might crash and cause injury to spectators and themselves. This is especially true as most of the time the place where they show laps are in the long straights just before a sharp bend. This means that these are the areas where they have to look out and pay attention the most, especially due to the fact that they are travelling at extremely high speeds. So, what I propose is that they install a microbit onto the cockpit of the car, where the driver can easily see it. And back where the crew is, they have another microbit that is connected to the microbit in the car that is racing via radio. And every time the driver finishes a lap, someone in the crews section clicks on button A, which adds one to the number of laps(originally 0) and this number is displayed on the micro bit in the car 3 times, to alert the driver. Also, the microbit is compact and light, so weight will not be an issue, and there is plenty of space to place it. And at the final lap, it shows a smiley face for 3 seconds. At all other times, the microbit in the car shows nothing on the screen. 




So here is my code for the project:


from microbit import *
import radio

radio.on()
score = 0
while True:
if button_a.was_pressed():
    radio.on()
    score = score + 1
    radio.send(str(score))
    display.show(str(score))
if button_b.was_pressed():
    display.show(Image.HAPPY)
    radio.send(Image.HAPPY)
else:
  display.clear()
#This is the first part of the code(first microbit in pits with crew)

from microbit import *

import radio

radio.on()
while True:
  message = radio.receive()
  if message:
    display.scroll(message)
#This is the 2nd part of the code(second microbit in car with driver)



*Feel free to edit my code :)*


This will only require TWO microbits and practically nothing else.


Some general info on this project:

The main problem i am trying to solve is the problem that in Motorsport events such as F1, drivers drive constantly at high speeds and are distracted by looking away from the front to see what lap of the race they are on. This distracts them and as every millisecond matters in events like F1, their times may be compromised or even worse, they might crash and cause injury to spectators and themselves. This is especially true as most of the time the place where they show laps are in the long straights just before a sharp bend. This means that these are the areas where they have to look out and pay attention the most, especially due to the fact that they are travelling at extremely high speeds . I broke it down into a few problems. The first problem is where to place the microbit in the car, the second problem is how the driver will know what lap he is on on the microbit. The final problem is whether the driver would have to look in another direction to see the lap number.The main problem i am trying to solve is the problem that in Motorsport events such as F1, drivers drive constantly at high speeds and are distracted by looking away from the front to see what lap of the race they are on. This distracts them and as every millisecond matters in events like F1, their times may be compromised or even worse, they might crash and cause injury to spectators and themselves. This is especially true as most of the time the place where they show laps are in the long straights just before a sharp bend. This means that these are the areas where they have to look out and pay attention the most, especially due to the fact that they are travelling at extremely high speeds . I broke it down into a few problems. The first problem is where to place the microbit in the car, the second problem is how the driver will know what lap he is on on the microbit. The final problem is whether the driver would have to look in another direction to see the lap number.I used functions that I have learnt(not much haha) , and kept the program as simple as possible. I also made sure that the programmer required minimal effort from the people using it, keeping it as simple as possible.




CONTRIBUTIONS ARE GREATLY ENCOURAGED AND IF YOU HAVE CONTRIBUTED< TYSM! :))
