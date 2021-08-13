As the above quote from Marcus Buckingham inquires, who actually likes cleaning? With my floor cleaning robot, you'll never have to clean the house again...at least not the floors!

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Sterling Kalogeras | Pine Crest School | Computer Science | Incoming Senior
  
# My First Milestone
Where to begin? Well, before we can even begin discussing making my robot clean the floor, we have to actually build the robot! My first major goal was to finish building the base of the robot. I am going to refer to this base as the "car" since that's basically what my robot's base is.

My first step was to wire the car and this was _painfully_ slow. My car has four motors, with one being utilized for each wheel. To wire my car, I had to attach one red wire and one black wire to each motor by wrapping them around two miniature hooks. I then had to fasten the motors in place with screws and hex nuts. The process was "painful" because my wires would keep falling out of the holes they were wrapped around, so I had to continously unscre the motors from their place, re-wire the motors, and then re-screw them back into place.

Once I was finished with the main part of the wiring, I fastened the roof of the car into place by attaching it with the base via mini support beam. Afterwwards, I slid my wires through two holes on the roof of the car. I tied two pairs of red wires together as well as two pairs of black wires together. Next, I hot glued my battery pack and motor driver onto the roof of the car. It was then time to wire the top of the car.

I inserted a pair of red wires into the "OUT1" and "OUT4" connections of the motor driver and a pair of black wires into the "OUT2" and "OUT3" connections of the motor driver. I then connected six multi-colored wires to my ESP32 microcontroller. Finally, after applying wheels onto the car, I plugged in the microcontroller to my computer, ran a piece of sample code in Arduino to mensure that I wired my car correctly, and watched the car rotate left and right.

![IMG_9223 2](https://user-images.githubusercontent.com/88210009/128563141-b7ec282a-331b-4330-9486-fceb1e2ed4ce.jpg)

Check out a video version of this recap below!

<iframe width="560" height="315" src="https://www.youtube.com/embed/3VCPCNkzXvE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# My Second Milestone
The next part of this project would be to get the car to move. As shown above, as part of my first milestone, the car was successfully able to rotate. Thus, the main part of this milestone was to get the robot to avoid obstacles.

The way I did this was by using an ultrasonic sensor. For this to work, I had to connect the four pins of the sensor to four un-used pins on the ESP32. After the pins were connected, I started to fasten the different parts of the car to their "final" positions. My battery pack remained at the top of the robot, but I pushed back the motor driver, taped down my ESP32 and miscellaneous wires, and installed a portable charger so that my robot could run without the use of a computer. Afterwards, I taped my ultrasonic sensor to the front of the battery pack.

![IMG_9258 2](https://user-images.githubusercontent.com/88210009/129096125-63c0fac7-d161-4c7f-832c-fd2a345c9c00.jpg)

The last part of this milestone was the programming. First, I found code on the Internet to get the ultrasonic sensor to start reading distances. My vision was that if the sensor noticed it was within fifty centimeters of an object, it would turn from the object. Otherwise, the robot would continue going straight. Thus, I implemented code that did exactly that. Below is a screenshot of some of the code, and you can see the rest of it in my video!

![Screen Shot 2021-08-11 at 4 12 05 PM](https://user-images.githubusercontent.com/88210009/129096620-81b7b256-c4b7-4580-823d-0bd2f08769ad.png)

After modifying some of the code (e.g. changing the turning direction from left to right), I noticed that there was one huge remaining issue: the robot did not turn at all! However, after figuring out that it was not my code that was the problem but rather the hardware itself, I wrapped tape over all of the wheels to increase their traction. Once I did that, the robot was working as intended.

Here's a video recap of my second milestone!

<iframe width="560" height="315" src="https://www.youtube.com/embed/G6Q558XEjX8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# My Final Milestone

For my final milestone, it was time to bring everything together. I had to create a program that would serve as the primary code for the robot's functioning. I first designed an app on MIT App Inventor to serve as the user interface. My app contains a button for Bluetooth connection, a D-Pad to manually control the car, and a button to turn "autonomous mode" on or off.

I programmed a little bit with the block code of App Inventor, like changing the color of different buttons depending on which mode is activated, but most of my code is in Arduino. I explain my code in depth in the video below, but for the most part, the program is split into two different sections. The autonomous mode code is virtually the same as in my second milestone. The second part is the code for the D-Pad.

When testing my robot, one thing was obvious: the battery pack was doing its job, but not well. I decided to remove the battery pack entirely and use the ESP32 the power the motor driver. I took a wire from the VIN pin on the microcontroller and connected it to the 12V connection of the motor driver. Then I took another wire, attached one end to that same 12V connection and connected the other end to the VCC pin on the ultrasonic sensor.

Finally, it's time to address the elephant in the room: how does the robot clean the floor? I had originally planned on using a brush to sweep the floor, but the brush I had planned on using was too big for the robot. Instead, I attached a blue duster in order to trap dust on the floor. Since I taped the duster on, it is easy to replace after each cleaning.

![IMG_9312](https://user-images.githubusercontent.com/88210009/129418615-4c63c400-ac7f-45ad-82e5-585378dfe989.jpg)

Check out my final milestone video here!

<iframe width="560" height="315" src="https://www.youtube.com/embed/ys06tNTKmu0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

