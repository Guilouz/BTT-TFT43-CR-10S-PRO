
Si vous aimez mon travail, n'hésitez pas à me soutenir en me payant une 🍺 ou un ☕. Merci 🙂

<img align="right" width=400 src="https://user-images.githubusercontent.com/12702322/115151934-61597a00-a06f-11eb-89db-372e3d1e4647.jpg" />

 [ ![Download](https://user-images.githubusercontent.com/12702322/115148445-e5a40100-a05f-11eb-8552-c1f5d4355987.png) ](https://www.paypal.me/CyrilGuislain)


![GitHub](https://img.shields.io/github/license/bigtreetech/bigtreetech-TouchScreenFirmware.svg)
[![Build Status](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/workflows/Build%20Test/badge.svg?branch=master)](https://github.com/bigtreetech/bigtreetech-TouchScreenFirmware/actions)


Firmware pour écran BigTreeTech TFT43 3.0 configurée pour Creality CR-10S Pro.
  
  
  
## Connection de l'écran à la carte mère

![Câblage TFT43](https://user-images.githubusercontent.com/12702322/115152362-10e31c00-a071-11eb-80db-e5554de2c958.png)

**Note : Le mode "Marlin" n'est pas disponible sur la Creality CR-10S Pro en raison des limitations de la carte mère.** 



## Mise à jour du firmware

La mise à jour du firmware TFT se fait en trois étapes décrites ci-dessous et comprend jusqu'à quatre éléments :

**ÉLÉMENTS :**

**Élément 1 :** Le firmware binaire (`BIGTREE_TFT*_V*.*.*.bin`). Exemple : `BIGTREE_TFT43_V3.0.27.bin`:

- `BIGTREE_TFT_43`: modèle
- `V3.0`: version matériel
- `27`: version logicielle


**Élément 2 :** Polices et Icônes (dans le dossier `TFT43`) :

Le dossier ROOT pour les polices et les icônes est le dossier TFT43.

Structure du dossier des polices et des icônes :
- `TFT43/font`: polices
- `TFT43/bmp`: icônes


**Élément 3 :** Le fichier de configuration `config.ini`

**Élément 4 :** Un ou plusieurs fichiers de langue **(optionnel)**

**ÉTAPES :**

**Étape 1 :** Copiez le firmware compilé BIGTREE_TFT*_V*.*.*.bin, le dossier TFT43 et le fichier config.ini à la racine d'une carte SD vierge inférieure à 8 Go et formatée en FAT32 :

![Firmware](https://user-images.githubusercontent.com/54359396/100600549-b6cffd00-3301-11eb-8b57-d56b7a4422f1.jpg)

**Optionnel**, copiez un ou plusieurs fichier(s) de langue à la racine de la carte SD. Cela vous permettra de basculer entre l'anglais et la ou les langues téléchargées, en utilisant la fonction Langue dans les menus de l'écran. Il est recommandé de télécharger le minimum de langues afin de limiter l'utilisation de la mémoire.

![Language Pack](https://user-images.githubusercontent.com/54359396/100600564-b9caed80-3301-11eb-8997-d376f05323f6.jpg)

**Étape 2 :** Insérez la carte SD dans le port SD de l'écran et réinitialisez ce dernier (ou redémarrez votre imprimante) pour démarrer le processus de mise à jour.

⚠️ Ne pas mettre à jour les icônes et / ou les polices entraîneront des icônes manquantes et / ou du texte illisible ⚠️



## Processus de mise à jour affiché sur l'écran TFT

Une mise à jour réussie ressemble à ceci sur l'écran :

![Screenshot 2020-09-26 at 22 10 04](https://user-images.githubusercontent.com/54359396/94349526-5abcd400-0045-11eb-993a-afc5b241f4d7.png)

... et le nom des éléments sur la carte SD change comme suit :

![After Update](https://user-images.githubusercontent.com/54359396/94349755-dc156600-0047-11eb-9b1e-a1334bc5675f.png)


En cas d'échec d'une ou plusieurs parties de la mise à jour, une erreur s'affichera. Suivez les informations à l'écran pour mettre à jour les éléments manquants ou obsolètes.

![Screenshot 2020-10-23 at 14 37 36](https://user-images.githubusercontent.com/54359396/97004894-002c7000-153e-11eb-9951-f493be46af3e.png)

⚠️ Les erreurs lors de la mise à jour ne peuvent pas être ignorées et doivent être résolues avant d'utiliser l'écran ⚠️



**Étape 3 :** Retirez la carte SD de l'écran et redémarrez l'imprimante.




## Configuration

Bien que déjà configuré pour la Creality CR-10S Pro, le fichier **config.ini** peut être modifié en utilisant un simple éditeur de texte (assurez-vous d'utiliser le codage UTF).

Une fois modifié et enregistré, le fichier config.ini peut être installé sans qu'il soit nécessaire d'installer à nouveau le firmware ou le dossier TFT43, à condition que le firmware et le fichier config.ini soient de la même version.



### Editing configuration (config.ini) file

To edit the **config.ini** file follow the instruction here: [Detailed Instructions here](config_instructions.md)

### Updating Firmware Configuration

To update the Firmware configuration:

1. Edit the settings in **config.ini**.

2. Copy the **config.ini** file to the root of the SD card. (The SD card capacity should be less than or equal to 8GB and formatted as FAT32)

3. Insert the SD card into the TFT's SD card slot and restart the printer or press the reset buttion of the TFT.

4. The TFT will update and store the configuration from **config.ini** file.

5. Make sure to remove the SD card from the TFT and restart the printer.

6. On the TFT click on Menu - Settings - Feature and navigate to the last page. Click on

   "Reset default settings ..."

7. Restart the printer to finish the update of the config.ini


## Menus

|                    Status Screen DISABLED                    |                    Status Screen ENABLED                     |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| ![status screen 0](https://user-images.githubusercontent.com/54359396/103319145-09035b80-4a31-11eb-91d0-dd761a48b6f5.png) | ![Unified Material Main Screen](https://user-images.githubusercontent.com/54359396/98742038-03cd4d00-23ae-11eb-9552-36dc02fe66f4.png) |
| In config.ini define: General Settings<br/>Enable Status Screen<br/># Select the Main Screen flavour<br/># Options: [Enable: 1, Disable: 0]<br/>**status_screen: 0** | In config.ini define: General Settings<br/>Enable Status Screen<br/># Select the Main Screen flavour<br/># Options: [Enable: 1, Disable: 0]<br/>**status_screen: 1** |



## Customization

### Bootscreen and Icons

See [Customization guides](https://github.com/bigtreetech/BIGTREETECH-TouchScreenFirmware/tree/master/readme/) for detailed  information.



## Troubleshooting

**In case the upload of a new firmware failed**

First, verify that you have been using the correct version for your TFT. After that, try to upload the new firmware again (like described above) using a **new** SD card - 8GB or smaller, FAT32 formatted. Some uploads worked fine after executing a low level format of the SD card and not a quick format.

**Simple Reset**

To reset the TFT's touch screen calibration, create a blank file named  "reset" with the file-extension "txt", and place it in the root folder of an SD card (the SD card capacity must be less than or equal 8GB and formatted as FAT32). Insert the SD card into the TFT's SD card reader and power cycle your printer or restet your TFT to start the reset process.

**Worst Case Scenario**

In case the screen remains black or the brightness is not stable, the screen does not react after pressing a button or executes clicks by itself or does something similar - and the reset described above did not help - do the following. Remove the TFT from the enclosure and disconnect everything from the TFT, including the cable to the mainboard. Cut a USB cable you do not need anymore and connect the red and black wire to 5V and GND of the TFT. Do not use the unshielded wires directly but use a 2 pin connector instead. Power up the TFT and try to reset the TFT or to instal a new firmware like described in this document. With only power supplied, you should be able to navigate through the menus using the touchscreen and even to switch to Marlin Emulation (if available), even the Marlin Emulation screen will not show the interface with a proper EXP based connection.



### Show more statistics at the end of the print

Statistics as filament length, filament weight and filament cost can be embedded into the gCode. After the print is finished there will be an infobox that you can click and a popup will present you the printed filename (limited to the first 25 characters), the time needed for the print, the filament length used, the filament weight and its cost. In the case of multi-filament usage the statistics will show the sum of all individual data (sum of length, sum of weight, sum of cost).
The statistic data in the gCode must have the following format (a good practice would be to include this at the beginning of the gCode):
* `M118 P0 filament_data L:{12.3456}m`  L: represents the length in meters
* `M118 P0 filemant_data W:{1.23456}g`  W: represents the weight in grams
* `M118 P0 filament_data C:{0.1234}`    C: represents the cost without a unit

The values of every filament data can be in a brackets, parentheses, apostrophes, etc. or without them, measurement units can be there or not.
So `M118 P0 filament_data L:(12.3456)m`, `M118 P0 filament_data L:12.3456meters`, `M118 P0 filament_data L:[12.3456]` and so on are all valid formats.
For multi-filament print statistics the data for each used filament should be written, they can be separated by comma, space, asterix, whatever, except ";" and ".".
Examples for multi-filament:
* `M118 P0 filament_data L:(12.3456, 8.2520974)m`
* `M118 P0 filament_data W: 24.87652 15.568264 gramm`
* `M118 P0 filament_data C:[1.3456], [0.56024]`

The inclusion of the filament data into the gCode can be automated. In Cura all you have to do is to insert the following into the Start G-Code:
* `M118 P0 filament_data L:{filament_amount}m`
* `M118 P0 filament_data W:{filament_weight}g`
* `M118 P0 filament_data C:{filament_cost}`

In case the gCode file has been generated using the  [BTT 3D Plug-In Suit](https://github.com/bigtreetech/Bigtree3DPluginSuit), the data is automatically added.

In case filament data is not present in the gCode, the filament length data is calculated during print. Length is calculated regardless of using the TFT USB, TFT SD or the onboard SD. Calculations are done in both absolute or relative extrusion mode. Filament data takes into account the flow rate also but with a caveat. It has to be the same flow rate during the entire time of the printing, because the end result is calculated based on the flow rate at the time the print has finished. If flow rate changes during the print the results will not be accurate anymore.
