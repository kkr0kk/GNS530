<H1>GNS530 - Simulation GPS - for Cessna 172 - DIY</H1>

<H1>WORK IN PROGRESS, don't build this for now, NOT TESTED YET</H1>
Build your own GPS GNS530 for simulation cockpit.<BR />
Format for 6.25" stack<BR />
Electronics are design with EasyEDA.<BR />
3D parts are design with SolidWorks.<BR />
Parts printed with ANET A8 and CURA 15.04.6<BR />
PCB are sold by JLCPCB, you can use directly Gerber files --> <a href='https://jlcpcb.com/'>JLCPCB</a><BR />
Only electronics, you can choose the microcontroller of your choice, the base design have addtionnal card for Mega2560R3.
For mine i use Mega2560R3 and Mobiflight on MSFS2020--> <a href='https://www.mobiflight.com/en/index.html'>MOBIFLIGHT</a><BR />
For others controllers you need to design the support for the card, or add wires to link them.
<img src='https://github.com/kkr0kk/GNS530/blob/main/images/gns530-3D-front.png?raw=true' />
<H2>ELECTRONICS</H2>
<img src='https://github.com/kkr0kk/GNS530/blob/main/images/gns530-shematic.png?raw=true'></img>
<img src='https://github.com/kkr0kk/GNS530/blob/main/images/gns530-pcb.png?raw=true'></img>
<table class="table table-bordered table-hover table-condensed">
<thead><tr><th title="Field #1">Controller PIN</th>
<th title="Field #2">Header PIN</th>
<th title="Field #3">Description</th>
</tr></thead>
<tbody><tr>
<td>5V</td>
<td align="right">1</td>
<td>5V</td>
</tr>
<tr>
<td>22</td>
<td align="right">2</td>
<td>LEFT Encoder double</td>
</tr>
<tr>
<td>23</td>
<td align="right">3</td>
<td>LEFT Encoder double</td>
</tr>
<tr>
<td>24</td>
<td align="right">4</td>
<td>LEFTEncoder double</td>
</tr>
<tr>
<td>25</td>
<td align="right">5</td>
<td>LEFT Encoder double</td>
</tr>
<tr>
<td>26</td>
<td align="right">6</td>
<td>LEFT Encoder double push button</td>
</tr>
<tr>
<td>27</td>
<td align="right">7</td>
<td>RIGHT Encoder double</td>
</tr>
<tr>
<td>28</td>
<td align="right">8</td>
<td>RIGHT Encoder double</td>
</tr>
<tr>
<td>29</td>
<td align="right">9</td>
<td>RIGHT Encoder double</td>
</tr>
<tr>
<td>30</td>
<td align="right">10</td>
<td>RIGHT Encoder double</td>
</tr>
<tr>
<td>31</td>
<td align="right">11</td>
<td>RIGHT Encoder double push button</td>
</tr>
<tr>
<td>32</td>
<td align="right">12</td>
<td>Button CDI</td>
</tr>
<tr>
<td>33</td>
<td align="right">13</td>
<td>Button OBS</td>
</tr>
<tr>
<td>34</td>
<td align="right">14</td>
<td>Button MSG</td>
</tr>
<tr>
<td>35</td>
<td align="right">15</td>
<td>Button FPL</td>
</tr>
<tr>
<td>36</td>
<td align="right">16</td>
<td>Button VNAV</td>
</tr>
<tr>
<td>37</td>
<td align="right">17</td>
<td>Button PROC</td>
</tr>
<tr>
<td>38</td>
<td align="right">18</td>
<td>Button ENT</td>
</tr>
<tr>
<td>39</td>
<td align="right">19</td>
<td>Button CLR</td>
</tr>
<tr>
<td>40</td>
<td align="right">20</td>
<td>Button MENU</td>
</tr>
<tr>
<td>41</td>
<td align="right">21</td>
<td>Button Direct-to</td>
</tr>
<tr>
<td>42</td>
<td align="right">22</td>
<td>Button Zoom-</td>
</tr>
<tr>
<td>43</td>
<td align="right">23</td>
<td>Button Zoom+</td>
</tr>
<tr>
<td>44</td>
<td align="right">24</td>
<td>Button COM swap</td>
</tr>
<tr>
<td>45</td>
<td align="right">25</td>
<td>Button VLOC swap</td>
</tr>
<tr>
<td>46</td>
<td align="right">26</td>
<td>Encoder volume COM</td>
</tr>
<tr>
<td>47</td>
<td align="right">27</td>
<td>Encoder volume COM</td>
</tr>
<tr>
<td>48</td>
<td align="right">28</td>
<td>Encoder volume VLOC</td>
</tr>
<tr>
<td>49</td>
<td align="right">29</td>
<td>Encoder volume VLOC</td>
</tr>
<tr>
<td>GND</td>
<td align="right">30</td>
<td>GND</td>
</tr>
<tr>
<td>50</td>
<td align="right">31</td>
<td>Encoder volume COM - push button</td>
</tr>
<tr>
<td>51</td>
<td align="right">32</td>
<td>Encoder volume VLOC - push button</td>
</tr>
</tbody></table>
<H2>3D Printing</H2>
<H3>Materials</H3>
- HEAD : 0.2mm and 0.6mm<BR />
- PLA BLACK and PLA WHITE<BR />
<H3>CURA  configuration</H3>
With CURA you need plugin PauseAtZ, i modified the plugin to add 2 pauses (printing buttons by example) download and install it--> <a href='https://github.com/kkr0kk/c172-autopilot/blob/main/Gcode/pauseAtZ.py'>Here</a><BR />
<H3>Printing Buttons</H3>
The first pause is set to 0.25mm height and the second is set to 0.45mm height with a config layer height 0.1mm.<BR />
I'm printing buttons with 0.2mm head<BR />
The process for buttons is to start with WHITE PLA for printing text and the printer will go pause, change to PLA BLACK, Drop down the head directly on Z motors by ONE CLICK (so the Z axis return back to 0 but printer think is 0.2mm), purge the color, and resume.<BR />
It will be printing the black layer (fast), and the printer go pause again, Change to PLA CLEAR, purge and resume.<BR />
Now we have perfect buttons with 3 different color.<BR />
<img src='https://github.com/kkr0kk/c172-autopilot/blob/main/images/buttons.png?raw=true'></img>
<H3>Printing Main Parts</H3>
I use a 0.2mm head for the first part, and 0.6mm for the last big part.<BR />
I made 2 STL file, "main.STL" for the first part and "main - second layer printing.STL" for the second part.<BR />
Create 2 gcode files with their parts, parts need to be at the same place (use center platform function).
First Start with 0.2mm head and PLA CLEAR, and when the printer go pause, cancel the print<BR />
Change the head to 0.6mm and PLA BLACK, and start the second part "main - second layer printing.STL".<BR />
GCODE files are on github.<BR />
<H2>SUPPORT for controller</H2>
<H3>Support for Mega2560 pro mini</H3>
<img src='https://github.com/kkr0kk/c172-autopilot/blob/main/images/support_mega2560-pro-mini_PCB.png?raw=true'></img>
<H2>Other Projects</H2>
Build transponder KT76C for Cessna172 -> <a href='https://github.com/kkr0kk/c172-xpndr'>Transponder</a><BR />
Build AutoPilot KAP140 for Cessna172 -> <a href='https://github.com/kkr0kk/c172-autopilot'>AutoPilot</a><BR />
