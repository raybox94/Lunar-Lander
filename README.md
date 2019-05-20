# Lunar-Lander

# The complete code for Lunar Lander moved to bit bucket
[https://bitbucket.org/raybox94/lunar-lander/src/master/](https://bitbucket.org/raybox94/lunar-lander/src/master/)

The aim of the simulation is to find the acceleration to which a spacecraft land safely( without crashing )on the lunar surface.

---------

###### At the start the Lander will be at initial height H. We assume Lander velocity is zero
**v=0**

###### There are only two conditions
-----
-  Lander is in free fall its acceleration is

------

**a = -g** (where g is lunar gravitational acceleration)

(Note that a vector is a physical quantity that has both a magnitude and a direction. In our case the direction can only be up (+) or down (-) ).


------
-  Engine of the lander is On

------

This produces a thrust which adds an upward acceleration we will call A.

**A = T / m**

where

T = Thrust produced

m = mass of the lander



The lander has limited fuel **f=F**

(Note: The aim of the simulator of course, is to soft land the spacecraft on the lunar surface before the fuel runs out (ie **f = 0** )).

To implement the simulation we consider the motion of the lander in small segments of time Δt(delta(t)). If we have access to the real-time clock in the computer, then our simulation will be a real-time simulation - that is, everything will happen exactly as it would in real life.

The equations that we must compute for each small amount of time are:

**v = vo + a Δt**      (Equation 1)

**h = ho + vo Δt + a (Δt)2 / 2**       (Equation 2)

If the engine is off we substitue -g for a, and if the engine is on we subtitute A as - g for a, as long as the fuel is not zero. When the engine is on we must subtract a quantity Δf Δt from the remaining fuel f. We must also compute the new time. So altogether we have two more equations:

**f = fo - Δf Δt**     (only if the engine is on)       (Equation 3)

**t = to + Δt**      (Equation 4)

At the end we print current time, height, velocity and fuel, until the lander hits the lunar surface.

if **v>vs** the lander is safly landed else it has crased.

----
#### References :
----
https://www.spaceacademy.net.au/flight/sim/lunasim.htm

