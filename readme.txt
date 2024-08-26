DayZ Chernarus Big Oil Rig By EZ Rich & Sea Platform By Expansion Team, Converted By Don Sibley, For Console and PC xml json Mod Instructions & Terms Of Use

These files spawn a large oil rig, with loot, in the sea 1.4km South of the Light-House thats on the Coast West of Chernogorsk 

AND a Sea Platform South of Storzh Prison Island.

Limited Testing on PC Chernaus Local Server DAYZ Version 1.26 Aug 2024.

Created by AND BIG THANKS TO: EZ Rich ( terrellerich91#2154 on Discord).

AND the Expansion Team, AND Don Sibley who converted the expansion files.

Expasion on Steam: https://steamcommunity.com/sharedfiles/filedetails/?id=2116151222

Dons YouTube Channel: https://www.youtube.com/channel/UCI9Wh1Nl1i_Sfz_AT3PTVcg

Many Thanks To Inclement Dab for his amazing DayZ Editor that makes this all possible: https://steamcommunity.com/sharedfiles/filedetails/?id=2250764298

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

The DayZ Editor Mod .dze files are included for those who are familiar with the mod & how to create custom objects: sea-platform2.dze and oil-rig.dze

Instructions:

Click the "Code" button and "Download Zip" on the Github Repository and extract the files on your local PC for access.

Ensure your DayZ Server has activated the cfggameplay.json. For console users on Nitrado Servers, go to "General Settings" on your server and tick "Enable cfggameplay.json".

On PC Servers add the following line to your serverDZ.cfg:

enableCfgGameplayFile = 1;

(On some PC servers, including Nitrado, the serverDZ.cfg is "hidden", so you need to enable "expert mode" in settings,
then go to "expert settings", which is the serverDZ.cfg. Stop the server before making changes this way.)

Upload "ez-rich-oil-rig.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Upload "sea-platform-2-objects.json" from the extracted files to inside the "custom" folder of the mission directory on your server. This file places the structures on your map.
(If you haven't got a "custom" folder, create one.)

Open the cfggameplay.json file in the correct mission file for your server and look for the "objectSpawnersArr" line.

This file tells your server to access your custom file.

Edit it to look like this if you just want the oil rig: 

	"objectSpawnersArr": ["custom/ez-rich-oil-rig.json"],
	
Edit it to look like this if you just want the Sea Platform: 

	"objectSpawnersArr": ["custom/sea-platform-2-objects.json"],	
	
Edit it to look like this if you want both: 

	"objectSpawnersArr": ["custom/ez-rich-oil-rig.json","custom/sea-platform-2-objects.json"],
	
If you already are calling custom jsons to spawn items, seperate the files like this:

	"objectSpawnersArr": ["custom/ez-rich-oil-rig.json","custom/sea-platform-2-objects.json","custom/differentfile.json"],
	
Save your changes & upload if you need to.
	
Next we add loot to the structures by adding the following code snippet to the top of your mapgrouppos.xml file, after <map> 

	<!--big oil rig loot-->
	  <group name="Land_Construction_Building" pos="6030.310059 32.535400 553.257019" rpy="0.000000 0.000000 144.000000"/>
	<group name="Land_Construction_Building" pos="5991.520020 32.000000 514.164978" rpy="0.000000 0.000000 54.499996"/>
	<group name="Land_Container_1Aoh" pos="6058.689941 26.000000 554.330994" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="5999.470215 7.500000 526.145020" rpy="0.000000 0.000000 -34.000000"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="6025.870117 7.500000 541.375977" rpy="0.000000 0.000000 54.999992"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="6022.299805 7.500000 496.196991" rpy="0.000000 0.000000 145.999969"/>
	<group name="Land_Tisy_RadarPlatform_Top" pos="6049.520020 7.500000 520.278015" rpy="0.000000 0.000000 144.000000"/>
	<group name="Land_Construction_Building" pos="6041.709961 32.472599 518.786987" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Ship_Big_FrontA" pos="6045.930176 14.599500 583.523010" rpy="0.000000 0.000000 18.000000"/>
	<group name="Land_Ship_Big_FrontB" pos="6026.250000 13.000000 587.299988" rpy="0.000000 0.000000 18.000000"/>
	<group name="Land_Ship_Big_BackB" pos="5955.240234 11.100000 575.135986" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Ship_Big_BackA" pos="5971.350098 12.512600 586.206970" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Ship_Big_Castle" pos="5964.879883 20.986099 582.085999" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Construction_House2" pos="6036.709961 42.369801 518.234985" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Container_1Aoh" pos="5989.240234 -0.434310 611.523987" rpy="0.000000 -11.499999 0.000000"/>
	<group name="Land_Mil_Tent_Big2_3" pos="6014.680176 27.400000 527.208008" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Mil_Tent_Big1_2" pos="5995.870117 25.299999 538.046997" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Mil_Tent_Big2_4" pos="6006.990234 27.400000 535.741028" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Mil_Tent_Big4" pos="6047.549805 39.299999 560.872986" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Mil_Tent_Big2_5" pos="6022.629883 16.900000 500.329987" rpy="0.000000 0.000000 144.000000"/>
	<group name="Land_Mil_Tent_Big1_4" pos="6021.209961 14.800000 510.740997" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Mil_Tent_Big1_5" pos="6009.979980 14.800000 503.756989" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Mil_Tent_Big1_3" pos="6002.379883 14.800000 512.286987" rpy="0.000000 0.000000 144.500000"/>
	<group name="Land_Mil_Tent_Big2_2" pos="6008.790039 16.799999 526.315979" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Mil_Tent_Big1_1" pos="5992.370117 14.800000 523.978027" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Mil_Tent_Big2_1" pos="6020.109863 16.799999 546.382996" rpy="0.000000 0.000000 -27.000000"/>
	<group name="Land_Mil_Tent_Big4" pos="6016.850098 16.000000 531.806030" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Mil_Tent_Big1_4" pos="6034.830078 14.800000 528.593994" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Mil_Tent_Big1_3" pos="6039.879883 14.973500 522.249023" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Mil_Tent_Big1_4" pos="6044.580078 14.800000 515.893005" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Mil_Tent_Big2_2" pos="6051.149902 16.799999 530.239014" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Container_1Mo" pos="6043.939941 15.993400 537.916016" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Container_1Mo" pos="6035.799805 16.008301 545.013977" rpy="0.000000 0.000000 63.000000"/>
	<group name="Land_Container_1Mo" pos="6033.919922 15.993400 547.463989" rpy="0.000000 0.000000 53.999996 "/>
	<group name="Land_Container_1Mo" pos="5994.850098 15.993400 535.169983" rpy="0.000000 0.000000 -27.000000"/>
	<group name="Land_Container_1Mo" pos="6012.620117 15.993400 493.470001" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Aoh" pos="6020.990234 26.484501 503.264008" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Bo" pos="6021.100098 29.073000 503.309998" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Aoh" pos="6017.479980 26.714399 508.066010" rpy="0.000000 0.000000 144.000000"/>
	<group name="Land_Container_1Bo" pos="6039.979980 26.335300 534.659973" rpy="0.000000 0.000000 -125.999992"/>
	<group name="Land_Container_1Mo" pos="5984.540039 38.656502 510.105011" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Mo" pos="6026.549805 39.128601 501.199005" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Aoh" pos="6027.379883 39.088600 504.101990" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Mil_Tent_Big1_4" pos="6036.580078 37.990002 548.783997" rpy="0.000000 1.000000 144.000000"/>
	<group name="Land_Pier_Crane_A" pos="5955.640137 16.229799 556.620972" rpy="0.000000 0.000000 144.000000"/>
	<group name="Land_Container_1Mo" pos="6027.970215 39.201099 563.663025" rpy="0.000000 0.000000 53.999996"/>
	<group name="Land_Container_1Bo" pos="6010.419922 -0.714860 626.773010" rpy="0.000000 -15.499998 18.000002"/>
	<group name="Land_Container_1Moh" pos="6002.100098 0.009390 609.734009" rpy="0.000000 0.000000 45.000000"/>
	<group name="Land_Container_1Mo" pos="6000.450195 1.802210 612.924011" rpy="0.000000 -19.000000 -35.999996"/>
	<group name="Land_Container_1Bo" pos="5996.089844 -0.148810 614.643005" rpy="0.000000 0.000000 45.000000"/>
	<group name="Land_Container_1Mo" pos="5962.290039 12.074900 540.823975" rpy="0.000000 0.000000 -35.999996"/>
	<group name="Land_Container_1Mo" pos="5964.759766 12.074900 544.007996" rpy="0.000000 0.000000 -18.000000"/>
	<group name="Land_Container_1Mo" pos="5983.250000 12.074900 542.171997" rpy="0.000000 0.000000 0.000000"/>
	<group name="Land_Container_1Aoh" pos="5981.029785 14.615000 537.140015" rpy="0.000000 0.000000 -125.999992"/>
	
	<!-- Sea Platform Loot -->
	
	<group name="Land_CementWorks_ExpeditionB" pos="2765.177979 -0.431763 640.364258" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="Land_CementWorks_ExpeditionB" pos="2765.199463 -0.433167 611.464233" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="Land_Tower_TC3_Grey" pos="2771.031494 -5.844392 600.416992" rpy="0.000000 0.000000 -0.061520" a="90.0615"/>
	<group name="Land_Airfield_ServiceHangar_L" pos="2789.075439 0.858245 575.845703" rpy="0.000000 0.000000 -90.000000" a="-180"/>
	<group name="Land_Airfield_ServiceHangar_R" pos="2739.103760 0.858245 575.845337" rpy="0.000000 0.000000 -90.000000" a="-180"/>
	<group name="StaticObj_Pier_Concrete2" pos="2783.516846 -23.000793 664.608276" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2783.497314 -23.000763 683.280762" rpy="0.000000 0.000000 -0.060251" a="90.0602"/>
	<group name="StaticObj_Pier_Concrete2" pos="2743.506104 -23.000763 683.280273" rpy="0.000000 0.000000 -0.071025" a="90.071"/>
	<group name="StaticObj_Pier_Concrete2" pos="2743.547119 -23.000763 664.608276" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2823.461182 -23.000763 664.608276" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2823.405518 -23.000763 683.287476" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2863.466064 -23.000763 664.614197" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2863.399658 -23.000763 683.294312" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2703.715088 -23.000763 683.262634" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2663.735596 -23.000763 683.274780" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2703.612549 -23.000763 664.611328" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2663.689697 -23.000763 664.614441" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2903.364502 -23.000763 683.293701" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2" pos="2903.260986 -23.000763 664.603882" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete2_End" pos="2638.821533 -23.000763 683.280151" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Pier_Concrete2_End" pos="2638.853760 -23.000763 664.625977" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.473877 1.377441 656.774170" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.473877 1.368224 665.117065" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.473877 1.368224 662.266907" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.473877 1.368224 659.516724" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.497314 1.384917 691.514404" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.497314 1.384917 683.334473" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.497314 1.384917 686.084656" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Misc_ConcreteBlock2_Damaged" pos="2635.497314 1.384917 688.784851" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2643.003174 -23.000763 649.266235" rpy="0.000000 0.000000 30.009630" a="59.9904"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2636.507080 -23.000763 635.532837" rpy="0.000000 0.000000 59.999992" a="30"/>
	<group name="Land_Wreck_C130J" pos="2650.440674 6.183379 673.822876" rpy="0.000000 0.000000 90.000000" a="0"/>
	<group name="Land_Mil_ATC_Small" pos="2643.481689 11.417327 637.758972" rpy="0.000000 0.000000 -59.993351" a="149.993"/>
	<group name="Land_Container_1Aoh" pos="2634.476807 2.196014 626.466431" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2626.325439 -23.000763 579.515625" rpy="0.000000 0.000000 148.007599" a="-58.0076"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2621.313721 -23.000763 621.596191" rpy="0.000000 0.000000 -120.999939" a="-149"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2615.179932 -23.000763 607.511230" rpy="0.000000 0.000000 -151.999985" a="-118"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2616.982666 -23.000763 592.012878" rpy="0.000000 0.000000 178.000000" a="-88"/>
	<group name="StaticObj_Pier_Concrete2" pos="2648.333252 -23.000763 566.855713" rpy="0.000000 0.000000 -151.996338" a="-118.004"/>
	<group name="StaticObj_Pier_Concrete2" pos="2683.616455 -23.000763 548.073425" rpy="0.000000 0.000000 28.008430" a="61.9916"/>
	<group name="StaticObj_Pier_Concrete1_L" pos="2710.965088 -23.000763 536.116455" rpy="0.000000 0.000000 117.045601" a="-27.0456"/>
	<group name="StaticObj_Pier_Concrete2" pos="2734.891846 -23.000763 534.114746" rpy="0.000000 0.000000 3.999999" a="86"/>
	<group name="StaticObj_Pier_Concrete2" pos="2774.581299 -23.000763 530.981079" rpy="0.000000 0.000000 4.930748" a="85.0693"/>
	<group name="StaticObj_Pier_Concrete2_End" pos="2799.331299 -23.000763 528.963379" rpy="0.000000 0.000000 -86.000031" a="176"/>
	<group name="Land_Container_1Moh" pos="2615.553955 2.146026 625.016357" rpy="0.000003 -0.000002 -1.000000" a="91"/>
	<group name="Land_Wreck_Uaz" pos="2629.365479 1.829955 617.368286" rpy="-1.000000 9.999996 -17.000004" a="107"/>
	<group name="StaticObj_Wreck_BRDM" pos="2614.214111 1.534118 614.739380" rpy="0.000000 0.000000 42.999989" a="47"/>
	<group name="StaticObj_Container_2E" pos="2611.101807 3.581268 600.143860" rpy="0.000000 0.000000 28.000010" a="62"/>
	<group name="StaticObj_Container_2C" pos="2622.569580 3.581268 596.577026" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Wreck_V3S" pos="2613.268799 2.470184 587.202026" rpy="0.000000 -0.000003 0.000000" a="90"/>
	<group name="Land_Container_1Moh" pos="2625.843018 2.196014 581.354004" rpy="-0.000002 -0.000003 0.000000" a="90"/>
	<group name="Land_Container_1Aoh" pos="2633.622314 2.208495 567.869385" rpy="0.000000 0.000000 -106.999969" a="-163"/>
	<group name="StaticObj_Misc_RoadBarrier" pos="2640.977783 1.577544 578.718262" rpy="0.000000 0.000000 -154.999985" a="-115"/>
	<group name="StaticObj_Misc_RoadBarrier" pos="2641.824463 1.445709 562.632751" rpy="-0.195198 -1.456310 25.004955" a="64.995"/>
	<group name="StaticObj_Wreck_HMMWV" pos="2635.362549 1.893890 576.690552" rpy="0.000026 0.000041 -85.000015" a="175"/>
	<group name="Land_Wreck_Volha_Grey" pos="2646.777588 1.736175 563.079651" rpy="0.000000 0.000000 127.999939" a="-37.9999"/>
	<group name="Land_Container_1Moh" pos="2658.725830 2.208495 565.832520" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Container_1Aoh" pos="2663.994385 2.208495 552.613525" rpy="0.000000 0.000000 79.999985" a="10"/>
	<group name="StaticObj_Container_2C" pos="2652.615479 3.593719 570.815674" rpy="0.000000 0.000000 -33.000008" a="123"/>
	<group name="StaticObj_Container_1C" pos="2671.028564 2.141418 562.418579" rpy="-0.306720 -1.775419 -36.990498" a="126.99"/>
	<group name="StaticObj_Roadblock_CncBlocks_Long" pos="2676.734619 1.777160 558.801270" rpy="0.000000 0.000000 17.000004" a="73"/>
	<group name="Land_Container_1Aoh" pos="2679.331299 2.208495 543.304077" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Container_1Moh" pos="2687.414307 2.208495 551.304565" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Container_2B" pos="2693.421143 3.548888 536.879700" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="StaticObj_Wreck_BMP1" pos="2692.119385 1.953124 545.881592" rpy="-0.532027 -1.956749 0.000000" a="90"/>
	<group name="StaticObj_CementWorks_SiloBig1Bridge" pos="2788.248291 -0.291810 546.575867" rpy="0.000000 0.000000 -90.000000" a="-180"/>
	<group name="StaticObj_CementWorks_SiloBig1Bridge" pos="2729.153564 -0.291749 550.714111" rpy="0.000000 0.000000 -90.000000" a="-180"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2718.369385 2.219909 543.921265" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2717.074463 2.219909 543.921265" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Pier_Crane_B" pos="2731.318604 9.058227 520.264221" rpy="0.000000 0.000000 92.000031" a="-2.00003"/>
	<group name="Land_Pier_Crane_B" pos="2787.211182 9.058227 515.964294" rpy="0.000000 0.000000 93.000023" a="-3.00002"/>
	<group name="StaticObj_Container_2E" pos="2740.727783 3.593719 528.879395" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Container_1Aoh" pos="2725.242432 2.208495 540.576294" rpy="0.000000 0.000000 -30.000000" a="120"/>
	<group name="Land_Wreck_Volha_Grey" pos="2739.661377 1.731872 543.345276" rpy="0.000000 0.000000 -15.000000" a="105"/>
	<group name="Land_Container_1Moh" pos="2750.063721 2.208495 538.832703" rpy="0.000000 0.000000 -23.000008" a="113"/>
	<group name="Land_Guardhouse" pos="2759.678955 2.068877 526.307007" rpy="0.000000 0.000000 94.000015" a="-4.00002"/>
	<group name="Land_Wreck_S1023_Beige" pos="2762.895752 1.998382 538.797668" rpy="0.000000 0.000000 -26.000010" a="116"/>
	<group name="Land_Container_1Aoh" pos="2771.428955 2.208495 524.136719" rpy="0.000000 0.000000 113.999954" a="-24"/>
	<group name="Land_Wreck_Uaz" pos="2718.805908 1.842437 531.340027" rpy="0.000000 0.000000 -37.999996" a="128"/>
	<group name="Land_Container_1Mo" pos="2714.678955 2.267120 536.884644" rpy="0.000000 0.000000 -24.000006" a="114"/>
	<group name="StaticObj_Container_2A" pos="2748.670166 3.546752 527.064026" rpy="0.000000 0.000000 46.999992" a="43"/>
	<group name="StaticObj_Container_1C" pos="2798.512939 2.267120 524.705566" rpy="0.000000 0.000000 -34.000000" a="124"/>
	<group name="Land_Container_1Bo" pos="2783.732666 2.208495 536.099731" rpy="0.000000 0.000000 -37.999996" a="128"/>
	<group name="StaticObj_Container_1C" pos="2773.419189 2.267120 534.281555" rpy="0.000000 0.000000 -140.999939" a="-129"/>
	<group name="Land_Mil_Tent_Big1_1" pos="2739.696777 0.956978 578.058411" rpy="-0.000000 0.000000 175.927505" a="-85.9275"/>
	<group name="Land_Mil_Tent_Big1_2" pos="2752.496094 0.937890 579.584045" rpy="-0.000000 0.000000 177.015228" a="-87.0152"/>
	<group name="Land_Mil_Tent_Big2_1" pos="2785.161133 2.972294 587.256714" rpy="-0.000000 0.000000 0.000000" a="90"/>
	<group name="Land_Mil_Tent_Big1_5" pos="2770.500732 0.994331 579.601257" rpy="0.000000 0.000000 -179.980972" a="-90.019"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2724.779053 2.155109 568.008484" rpy="0.000000 0.000000 -95.464859" a="-174.535"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2724.625488 2.130129 569.402466" rpy="-0.000000 0.000000 -96.138672" a="-173.861"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2802.280029 2.144990 587.544006" rpy="-0.000000 0.000000 89.791649" a="0.208351"/>
	<group name="Land_Misc_Toilet_Mobile" pos="2802.449951 2.116727 585.643005" rpy="-0.000000 0.000000 90.682487" a="-0.682487"/>
	
Save your changes & upload if you need to.

Restart your server and the new structures will appear immediatly, and then they will slowly stock with loot. If you do a wipe, loot will start to appear immediatly.

At the time of uploading these files you cannot spawn infected zombies over water, so you can't add infected to these locations.

Orig File Created by Your EZ Rich & Expansion Team, with conversion by Don Sibley. For more help files for DayZ come visit us at http://bhaalshad.com 
If you upload this to another Discord or webpage, please leave filename intact and dont take credit
as your own. Thank you and enjoy :)  

Thanks, Rob.



