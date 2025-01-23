java c
MENG 4019 -   Practical 5 –   2022
Task: design and simulate the operation   of      a   hydraulic   curcuit.   Activate   the   thermal   option,   monitor   and   control   the   thermal   regime
First, we   build the conceptual circuit,   introducing a few   hydraulic   resistances   and   different   paths   for   the   oil   to   flow:1.          Open Automation studio, select and   insert the following   components   from   the   Hydraulic   set   of   components.  2.          Connect all elements as   shown   below   and   check   all   is   connected   correctly   it works.   We   are   interested   in   studying the thermal effects, so the circuit will   not   be   set   for   other   tasks:  
3.         To   determine the thermal   regime, we can   use thermometers. An alternative   is   using the   node   Dynamic   Measuring   Instruments: 4.         The   usual   linking of the thermometers does   not work well:  
5.          From Simulation Options   in the Simulation   menu,   Activate the   Thermal   Evolution   in   the   Fluid   Simulation   tab 6.          Set the thermometers to   directly connect with the   measuring   points  7.          Run   the   simulation

We see that the thermal option works, the temperature   increases.   The   max   power   for   the   default   values   (120   l/min   = 0.002   m3/s,   at 80   bar)   means a   heating   power   of   16   kW.
8.          We can change the   reservoir with a   multi-port   reservoir,   to   have   a   better   control   of   the   ports:


9.          Running the simulation, we   realise that   something   is   not   quite   right. The temperature   increases, then   reaches   a   plateau. Examining the   results, we can see that the   oil   enters the   circuit   at   25   deg   C,   which   means that   the   thermal inertia of the   reservoir   is   unrealistic. On the other   hand, we   see that   the   two   major   resistances –   the   orifice and the variable   relief valve –   have a temperature   increase, as expected.   Settings   below:   relief valve:   250   bar   (to   protect the   pump and circuit), the variable   relief valve 80   bar   and   3.5   mm   orifice   opening 


10.    If we check the   reservoir   properties, we see that the   infinite volume   option   is   true.   This   is   not   realistic,   so   we   set the option to false and the volume   of the   reservoir at   150   l 

11.   We see that the temperature starts   rising   in the whole   circuit

12.   The temperature   increases fast   if w代 写MENG 4019 - Practical 5 – 2022
代做程序编程语言e change the settings of the   variable   relief valve   to   200   bar,   displacement   to   200 cm3/rev:  

13.       If we   leave   it too   long, we see that the   system   evolves   towards   destruction:


14.   We   need to   provide a   means to cool the circuit.   We   insert   a   cooler   and   a   valve,   plus   a   couple   of   thermometers: 


The oil   returns to the   reservoir   until   it   reaches the desired temperature, when,   by   switching the   valve,   we   can   direct   the oil through the   cooler
15.   We   run the circuit to   check all   is correct.   Because the   cooler   is   off-line   (oil   diverted   directly   to   the   reservoir),   the temperature   in and out of the cooler   is   25   deg   C,   which   is   the   default   temperature   for   simulation 


16.    Running the oil through the cooler   seems to   work,   but   it   is   not   much   help

17.   We   need to set the   parameters of the cooler.   With   the   last   settings,   we   have   a   flow   of   240   l/min   at   200   bar,   with the   return of the oil at atmospheric   pressure. This   means   that   the   circuit   needs   to   dissipate   80   kW 
The cooler   has a switching temperature of   50   deg   C   and   a   deactivation temperature   of 40   deg   C   We set the   maximum dissipation from   2 to   100   kW 


18.    Even with the   max   dissipation set, the   results are   not   much   better. We   can   adjust the   valve   details   to   indicate   correct flow: 


19.      We   need to set the folowing characteristics of the   dissipation   curves:  

20.   We check   if it works.   Below 50   deg   C   - the   switching temperature –   the   cooler   is   not   active.   This   is   normal:
21.

22.   Running for a   long time, we see that the temperature   reaches   a   plateau   and   stops   increasing  

23.   To   note –   real systems 
- are generally   less thermally stressed – this circuit   was   set   to   produce   and   dissipate   80   kW   of thermal   power.   This   is   highly   unusual   in   practice, as sytems are   designed   (and optimised) for   the   task   they   need   to   fulfill 
- dissipate extra   heat to the atmosphere – the   piping,   various   components,   pump,   etc. we   did   not   set   this,   but   it   is   possible 


Save the circuit.   Explore alternatives. Add functionality and test.   Document   your   work. 







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
