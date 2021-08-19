# kzg
VIA for Split75 / Wheatfield75
1. Install QMK Toolbox : https://github.com/qmk/qmk_toolbox

Install Text editor : https://www.sublimetext.com/

Install QMK Msys: https://github.com/qmk/qmk_distro_msys/releases/tag/1.4.2

Install VIA: https://caniusevia.com/



2. Open QMK Msys > qmk setup (setup qmk enviroment)

Start building > qmk compile -kb wheatfield/split75 -km default 

After that, go keyboards/wheatfield/split75/config.h change #define DYNAMIC_KEYMAP_LAYER_COUNT 4 --> #define DYNAMIC_KEYMAP_LAYER_COUNT 2



3. In QMK folder > keyboards/wheatfield/split75/keymaps/ , duplicate 'default' folder , change this folder name to 'via' (without ')


4. In this via folder, creat file is rules.mk > in this file type :

VIA_ENABLE = yes

LTO_ENABLE = yes


5. In QMK Msys, we build : qmk compile -kb wheatfield/split75 -km via

After that, we will have this hex file for via "wheatfield_split75_via.hex" in qmk_firmware folder
Flash this file to board  thru QMK Toolbox


6. Open VIA, in VIA setting, enable Show Design Tab

In Design Tab, press LOAD and locate this split75_via.json


7. Go Key Tester > Test Matrix than test all of button

PS: If layer 1, layer 2 is wrong mapping in default, just clear it, dont worry :D 

