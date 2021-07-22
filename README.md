# RF-Cable-and-Component-Testing

## Ojectective:
To provide the field and construction team with a standard testing guide for common components.
 
While experience, root cause analysis, and efforts to continually improve trumps lecture and "learning by the book", below is an outline of a collection of general knowledge and use cases.
 
While the spreadsheet is located on SharePoint, and available for anyone to add to, please open a  "change request" in the post section. Once approved, the requester can make the change, assuming uniformity of formatting remains the same.
File Location:
The file can be accessed via the Excel, in-window, App or with the Following link: Testing Matrix
Sweep Testing: Introduction
## Overview:
The Return Loss (RL) and VSWR measurements are key field team measurements
These measurements show the impedance match of the system and if it's within spec
 
If problems show up during this test, there is a very good likelihood that the system has problems that will affect the end user.
Sweep Testing: Types
There are two types of return loss tests, relative and absolute.
 
### Absolute Return Loss:
Absolute RL (VSWR) tests are taken with a known calibrated load...
At the end of the RF network to ensure a match in independence
On a calibrated machine; Connect your spectrum analyzer on one end of the cable, and with the calibrated load in place of the antenna...
Most reflections which occur are the result of impedance mismatches within the network
This test allows the network to be compared to manufacturer specifications
 
### Relative Return Loss:
Relative RL is taken with the final antenna connected and installed, in place of the known load
Shows the delivery return loss of the system
Shows installation distortions
This test will discover irregularities such as mounting too close to metal objects
Distortions can also occur due to:
Movement
Proximity to other objects like people
RF signals and other systems
 
You can also run a third test, one with a short attached to the end of the cable. Cell site insertion loss is measured with a short on one end of the cable, and a site master at the bottom end. 100% should reflect back. The signal travels up once, and then back down. I.e., it travels the distance twice. Because of this, if your final figure is 4 dB, you will divide by two to see the insertion loss is 2 dB's.
 
NOTE: The quality of your measurements is only as good as the quality of your calibration. Reference the calibration section of this Wiki or refer to your Anritsu Online Help Tool.
## Return Loss: Expected Values
If your return loss figure is:
20 dB, indicates that 1% of the transmitted signal is being reflected back to the transmitter
I.e., 99% is reaching the antenna
10 dB, indicates that 10% of the signal is being reflected back
This is poor performance
0dB, 100% of the power would be reflected back
This would likely be an open or short circuit
Return loss can be masked by high insertion losses, which drives the request of DTF plots.
High insertion loss not only affects the transmit power's coverage, but also poses a problem on the UL. High insertion losses drive up the UE's Tx power to reach the BTS receiver. This will drain the battery of the UE.
 
## Return Loss: Table
RL [dB]	Losses [%]	VSWR Value
0	100% reflection, no power into the antenna	17
1	80% reflection, 20% power into the antenna	9
2	63% reflection, 37% power into the antenna	6
3	50% reflection, 50% power into the antenna	3.5
5	32% reflection, 68% power into the antenna	3
6	25% reflection, 75% power into the antenna	2.3
8	16% reflection, 84% power into the antenna	2
10	10% reflection, 90% power into the antenna	2
15	3% reflection, 97% power into the antenna	1.4
20	1% reflection, 99% power into the antenna	1.2
 
## Return Loss: Expected Traces
The return losses plotted from a sole cable and one with an antenna will vary. Typical patterns are show below. 
 
The image below shows a combined cables across a 80' length. You can see an average of ~4.5 dB loss.

 
This image below not only shows the loss at the antenna, but also considered the system loss as shown above.
 

 
 
## Distance-to-Fault (DTF)
DTF maps the RL (or VSWR) over the length of the complete network. This test is known as DTF-RL.
 
This test is used for both troubleshooting and quality analysis.
It is possible that DTF will fail even after RL measurements pass. See Appendix A1 for an example.


# Appendix A1: RL-DTL Use Case 1:
Back to Distance-to-Fault (DTF)
 
A new reel of cable arrived at warehouse and the project team conducted absolute line sweeping to verify the "As Received" cable.
Testing the reel showed good RL sweep tests, however the RT-DTF  measurement showed an issue ~125' into the half reel.
See images below.
 
RL sweep tests show passing, and below the limit.

 
However, the RL-DTF measurement shows a large spike of ~-35 dB near the 125' mark.
A closer visual inspection of the cable shows a dent in the cable.

 
Dented cable shown below.

 
This is a good example as to why inspecting cable and performing line sweep tests prior to the installation is a good practice.
Completions Above, Work In Progress Below:

_______________________________________________________________________
PIM Testing Parameters
Add table with parameters of common parts
CW Testing Parameters
Add table with parameters of common parts
OTDR Testing Parameters
Add table with parameters of common parts
Appendix B1: Return Loss and the Reflection Coefficient
The reflection coefficient is the ratio of the reflected wave to the incident wave, at a point of reflection.
The values vary from the short load represented as "-1" to an open load, +1.
A zero (0) is reserved for defining a matched impedance load.
 
 

ZL defines the impedance toward the load, and ZS defines the impedance toward the source.
 
Return Loss, would be twenty times the base ten logarithm of the coefficient.
