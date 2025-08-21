# ICE_A1_Train_Crossing_Logic_System
<H2>Railway Crossing Safety System</H2>

<H4>Project Overview</H4>
<P>This repository contains the design for a logic-based safety system to control the gates of a railway crossing. The system is engineered to ensure the safety of both vehicular and pedestrian traffic by relying on simple, intuitive logic to manage gate operation. The design assumes a standard two-track railway crossing with a two-way road.</P>

<H4>Key Features</H4>
<UL>Train Detection: The system accurately detects trains that are approaching or currently on the tracks.</UL>
<UL>Clearance Verification: Gates are only raised when all tracks are confirmed to be clear of any trains. Otherwise, gates remain LOWERED.</UL>
<UL>Vehicle Trapping Prevention: The logic includes a mechanism to prevent vehicles from being trapped between the gates during closing, a critical safety consideration for two-way traffic.</UL>

<H4>System Logic</H4>
<P>The system operates on a continuous loop, with the gates remaining lowered by default to ensure maximum safety. The logic flow is as follows:</P>
<OL>Default State: The system is ON, and the gates are DOWN.</OL>
<OL>Road Traffic Check: The system checks for approaching vehicles. If none are present, the gates remain down, and the system loops back to the beginning.</OL>
<OL>On-Track Train Check: If vehicles detected to be approaching, the system checks for any trains currently on the tracks. If a train is on the track, the gates remain down.</OL>
<OL>Approaching Train Check: If no train is on the track, the system checks for any trains approaching. If a train is approaching, the gates remain down, and the system continues to monitor for trains on the track.</OL>
<OL>Gate Raise Condition: Only when no trains are on the track, and no trains are approaching, are the gates raised. A visual light signal and an audio alarm activate to alert drivers.</OL>
<OL>Crossing Clear Protocol: While the gates are raised, the system monitors the crossing area. Once it is clear, the gates are lowered, and the system returns to its default state.</OL>

<H4>Design Assumptions</H4>
<UL>The railway crossing has two tracks (one for each direction of train travel).</UL>
<UL>The road is a two-way road perpendicular to the tracks.</UL>
<UL>The system uses four types of sensors:</UL>
  <OL>A: Detects trains approaching the crossing.</OL>
  <OL>B: Detects trains currently on the tracks.</OL>
  <OL>C: Detects vehicles approaching the crossing</OL>
  <OL>D: Detects vehicles in the crossing area.</OL>
