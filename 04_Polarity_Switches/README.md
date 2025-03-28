# PolaritySwitches

<!DOCTYPE html>
<head>

</head>
<body>
     <p>If you only run your train in a circle - no need to take polarity switching into consideration<br/>
	 BUT if you try to make a loop where you turn the outgoing track into a loop and make it come back as incomming track to connect to the outgoing track - you'll see that the 'outside' rail suddenly will have to connect to the 'inside' rail - i.e. you create a SHORT CIRCUIT ! (and may have to say goodbuy to your power supply :-(  )</p>
	 <p>To avoid this you'll have to cut the tracks so that no connection is possible all way round at the same time. Unfortunately doing so will course you trouble when you run your train - because the wheels on the train may short the 'cuts' you have made</p>
	 <p>The solution to this is to isolate a piece of track (cut the rails more places) and connect a few switches to the isolated part of the track.<br/> When the train is outgoing you connect the isolated parts to the outgoing track. As the train drives into the isolated part - you disconnect the outgoing supply connection to the isolated part and switch it to the ingoing supply.<br/> Now your train can pass nicely.</p>
	 <p>You can make a manual system, if you like to be kept busy while driving your trains - or you can insert some automation electronics to help you.<br/>
	 <h2>Polatiry Switching electronics</h2> 
	 Here we make an isolated piece of track as an automatic switching section. The isolated piece of track is divided into 3 part - 1,2,3.<br/>
	 Part1 is normally connected (through a relay) to the outgoing track.<br/>
	 Part2 is normally not connected to anything (relays are off) - but is used the the polarity must be changes...we will describe this shortly.<br/>
	 Part4 is normally connected (through a relay) to the incomming track.
	 </p>
	 <p>When an outgoing train reach part1 a current sensor1 'feels' the train on part1 - and connects part2 to the outgoing supply too. This allows the train to continue driving throug part1 and into part2.<br/>
	 At the same time we disconnect the supply for part3 (to avoid any shorts)</p>
	 <p>When the train drives into part2 a current sensor2 feels the train on part 2. As the train leaves part1 the sensor1 displays 0 current and we can turn off the supply for part1 as we now know the train is in part2.</p>
	 <p>While the train is in part2 we change the relay-setting for part2 so the supply for part2 is shifted from outgoing supply to incomming supply<br/>
	 At the same time we disconnect the supply for part1 and connects the supply to part3 - now our train can continue running from part2 into part3 and forward.
	 </p>
	 <p>Finally when the train has left part3 we wait a while before we reestablish the 'ready for a train to arrive' status</p>
	 <br/>
	 <h2>Benefit and disadvantage of automatic polarity change</h2>
	 <p>The automatic polarity change works well when the train is run at allmost CONSTANT speed through the polarity change sections (wether it is fast,medium or slow speed does not matter - just constant).</p><p>In order to keep the isolated sections short a timing has been build into the arduino program - arduino expects the train should to run at allmost constant speed during the section. This allows arduino to 'forecast' when the train is going into one section and leaves another section...thus provide the polarity switching fast and efficient (i.e. only use a short piece of track only to do so)</p>
	 <p>Unfortunately - if you stop the train on it's way through the polarity change section arduino might be confused and you will need to help the train (push it) through the section and Arduino must be reset ! ... based upon experience I plan to make a reset wire from my control unit to each polarity switch circuit</p>
	 <p>I have 4 places in my system where I use polarity change - in generel it works nicely</p>
	 <br/>
	 <p>TODO: drawings of circle,loops,part1,2,3 supply situations...circuit diagrams etc</p>
	 <p><a href="../#ModelTrain">back to Model Train overview</a></p> 
</body>
</html>