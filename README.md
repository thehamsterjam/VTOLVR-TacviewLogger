![enter image description here](https://media.discordapp.net/attachments/722102189597655150/722217625379274752/image1.png?width=1204&height=677)
Hello and welcome to the VTOL VR Tacview Data Logger mod! It's been long time in the making and a fairly significant undertaking for me. The Tacview data log allows players to record their flights in real time and save all enemy, allied and player vehicle flight data. The data log (in ACMI format) can then be opened within the Tacview software for review, tactical analysis and determination as to why exactly the carrier did not clear you to land!

Just a couple of notes to start off with. I'm not a game developer and I don't work in C#, so I may have taken some shortcuts. I'm well aware this mod is not as well optimized as it could and should be. On large maps with numerous actors this mod *could* introduce significant lag as it loops through and collects all the necessary data. Future iterations will be able to handle this a bit better.

## Usage
To use the mod simply install the mod, launch the game, and enable the mod. At the time of writing it is important that you enable the mod every time you start the game. Once you begin a flight scene the data logger will automatically begin recording, as of now there is no positive indication of the recording in flight.

All flight recordings are stored in the VTOL VR Game Folder under TacViewDataLogs. Within this folder multiple folders with the datetime stamp of the flight will be created. Within this flight folder three files should be created.
 - datalog.acmi
	 - This is the primary datalog created for viewing in Tacview. With Tacview installed, you should simply be able to double click this and open it.
 - customHeightMapXML.txt
	 - This is custom XML used to display the exported heightmap. This data must be copy and pasted into the file C:\ProgramData\Tacview\Data\Terrain\Custom\CustomHeightmapList.xml under the \<CustomHeightmapList\> node. If this file doesn't exist, copy the version from C:\Program Files (x86)\Tacview (beta)\Data\Terrain\Custom. The data within CustomHeightmapList.xml must be formatted properly otherwise Tacview will silently fail to load the terrain data. See Height Maps/Terrain for more details.
 - heightmap_MAPName.data
	 - This is the heightmap data. Copy this file into C:\ProgramData\Tacview\Data\Terrain\Custom\. See Height Maps/Terrain for more details.

### Logged Parameters
All active actors (vehicles and projectiles) within a scene are logged.
The following parameters are generally all logged. Some ground and water vehicles may not contain all applicable data.
 - AOA
 - IAS
 - Altitude
 - AGL
 - Location
 - Callsign/Designation

### Models
Models in Tacview can be added via the following steps:
 1. Copy the vtolvr.xml file to C:\ProgramData\Tacview\Data\Database\Default Properties
 2. Copy all the .obj files from the assets folder into C:\ProgramData\Tacview\Data\Meshes

### Height Maps/Terrain


## Reporting Bugs


## Contributors/Resources/Special Thanks

 - BahamutoD, of Boundless Dynamics LLC.
	 - The creator of VTOL VR has been supportive and a great resource in my development efforts. Of course without his significant undertaking VTOL VR wouldn't exist in the first place.
 - KetKev and Marsh.Mello
	 - The developers of the VTOL VR modloader have been essential to helping me dive into creating mods, debugging, and optimizing. Without their support I would have given up long ago.
 -  Frantz Raia, of Raia Software inc.
	 - The developer of Tacview patiently supported my endeavors as I learned the Tacview tool and its capabilities. 
 - The guys on the VTOL VR Modding Discord Channel!
	 - GentleLeviathan, Temperz87,  THE GREAT OVERLORD OF ALL CHEESE, and many more people. Everyone has supported me in someway or another - whether it is through long and late nights of debugging, feedback on videos and GIFS, or just supportive commentary when the rough got rougher.
 - F/A-26B on the VTOL VR Discord Channel
	 - He provided guidance and a couple of custom plane models to use within Tacview.