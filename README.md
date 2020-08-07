# AWOS-weather-display
Project to adapt a Raspberry Pi to display on a discarded National Weather service Wind Direction and Speed display

This project will pole the internet for aviation weather, allow the pilot to select an airport to see the current weather from the Automated Weather system, and then drive the needled on a discarded National Weather Service Wind Direction and Speed indicator.

I have purchased a Pi-4B for this project, a 7" touch screen monitor for the pilots to input the airport, a 4 channel D to A converter, and have tested the displays to see if they work and how.

The F420C0WD wind direction indicator has three coils on the indicator pointer to allow it to be driven via three wires from an Anemometer. I plan on working some python code to drive this three wire interface from the D to A converter. During my testing, these coils draw about 30ma. The I2C D to A converter can handle about 20ma. so I am planning on attaching an op amp as a null gain buffer to handle the extra current draw. It runs between 1 to 3 volts. I need to figure out the math for the trig to drive this indicator.

The Wind Speed indicator has several impedance inputs and we pre-wired to the 500 ohm input. I found it would take between .25 to 5 volts full scale at about 30ma. I have not tried the higher impedance inputs. yet.

So, parts needed.

Poll internet to find airport METAR repots. Parse that to a screen output.
Interface for pilot's to input the desired airport
interface to drive wind direction
interface to drive wind speed indicator
box to put this all in
setup and display for our pilot friends
If you see this and have any ideas, let me know!!

Cheers,
Mark
