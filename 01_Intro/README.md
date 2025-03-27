# Introduction
<!DOCTYPE html>
<lang:html>
<head>
    <meta charset="UTF-8" />
    <title>Introduction to DCC++ DIY</title>
</head>
<body>
<p>
An old fashioned dc-model-train system running one train at a time on DC, has been updated to a modern DCC++ train system, where 6 trains can run simultainously at different speeds and in different directions on the same time on one track.
</p>     
<p>A detailed description of a full DCC system upon which DCC++ is based, can be found at <a href="https://www.nmra.org/index-nmra-standards-and-recommended-practices">National Model Railroad Association</a></p>

<h2>Skills neede to make my project</h2>
<p>In order ot make a project like the one described here you should be familiar with electronics theory and construction. </p>
</p>The hardware is fairly simple to implement - but may call for some knowledge if you need to troubleshoot the circuits on your way.</p>
<p>The software is more complex and some experience working with arduino programming is a must...</p>

<h2>What 'do you get'?</h2>
<p>A <b>Controlunit</b> is used to set each train on/off, set the desired train driving direction as well as the desired speed.</p>
The controlunit could have realised in software - with an on screen control - but it is much more fun to have a 'real' steering device to make the usage less computerbased and more physical. So: 
<p>I choose to make the Controlunit unit for 6 trains in hardware with 6x on/off and 6x direction switches, 6x sliding speed potmeter and a 3x 'speed-LCD-display' (each displaying the status of 2 trains), using an arduino to generate the LCD-display information and the nessecerry pulse-sequences for the power amplifier feeding the tracks.</p>
<p><b>6 trains can be controlled - running independently.</b></p>
<p>PLEASE TAKE NOTE: only part of the official specifications are implemented in order to turn the train on/off, set the speed and direction...You CANNOT program the trainnumber from a separate programming track etc....its 'being born' with a trainnumber specified in the the arduino program code at compilation time.</p>
<p>BUT if you are good at programming you can yourself change the arduino programs to suit your purpose.</p>

<p>The train picks up power from the track together with the signal-information sendt by the controlunit.</p>
<p>Inside the train a<b>Decoder</b> pick out the information for 'my trainnumber' to be used for actual control of the train speed and direction.</p>
<p>This decoder is implemented with an optocupler feeding the controlsignal to an arduino-nano for decoding and controlling the train dc-engine through a power driver. TAKE NOTE: with some of the small trains I have, I had to place the electronics in the first wagoon placed after the train...If you are good at building electronics you may be able to squezze it all in!.. </p>


</body>
</html>