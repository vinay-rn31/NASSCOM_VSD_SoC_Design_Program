
# DIGITALL VLSI SOC DESIGN AND PLANNING
## Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK
### SKY130_D1_SK1 - How to talk to computers
### SKY130_D1_SK2 - SoC design and OpenLANE
### SKY130_D1_SK3 - Get familiar to open-source EDA tools
![Screenshot (191)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/6c8f9aa1-fea7-45c9-8244-11ec9802f311)

![Screenshot (193)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/cdb2bd40-fd01-486a-8bbe-70322f807435)

![Screenshot (197)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/b5fc033b-fe85-4004-8aec-5a7aa1365192)

![Screenshot (198)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/3c926ab9-093a-44a1-a03d-1fc53512bc77)

![Screenshot (200)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/a3570639-3c7a-41b1-bf73-c16fa5bbfacc)

![Screenshot (202)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/fb39545d-c367-4845-a5e7-7361903e719b)

![Screenshot (203)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/265734f2-e83e-4e93-9d47-534d06b3d0de)

![Screenshot (204)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/340c01ab-82e6-4b75-94e7-c203147ca9a5)

![Screenshot (209)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/fb10af71-0ec7-4048-9f63-7c3175eabc48)

![Screenshot (205)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/9f3aa94a-444f-470e-90c5-a43046c6fb53)

![Screenshot (210)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/be7b7381-6daa-4ad8-b13c-d065f43087ff)

![Screenshot (212)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/6b1241dd-54be-4901-82c1-01c7437dc4b3)


![Screenshot (213)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/fcd60f60-80ed-4873-ae6a-c09ad5a5902e)

![Screenshot (214)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/db0ad75e-a17f-4476-88a0-8db93b0a8cd0)

![VirtualBox_vdsworkshop_05_05_2024_21_28_57](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/481f1b3e-8d78-402d-a908-ff20ddf1587c)

![VirtualBox_vdsworkshop_06_05_2024_03_18_02](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/87728bcb-9f91-4fe6-9399-15364d613d1e)

to invoke openlane:
docker ./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a

Assignment:
![VirtualBox_vdsworkshop_05_05_2024_21_27_39](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5122f61d-bd32-4a62-8eea-3e2e617c70e5)
Flop Ratio = No. of D FlipfLops / Total No. of cells
           =1613/14876
           =0.1084
Percentage of D FF's = 10.84%

## Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells
### SKY130_D2_SK1 - Chip Floor planning considerations
#### Utilization factor and aspect ratio 
![Screenshot (222)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/06fc3113-9625-4a18-b0d1-993339781c79)
* CORE- The logical cells occupies the complete area of the core
* DIE-A die which consists of core, is small semiconductor material specimen on which the fundamental circuit is fabricated.
* Utilization factor = Area Occupied by Netlist/Total Area of the core
* Aspect Ratio= Height/Width

#### Pre-placed cells
![Screenshot (223)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/7d9fbd35-c323-4e7f-9f60-c14793f86c8a)
The arrangement of these IP's in a chip is referred as Floorplanning,These IP's/blocks have user-defined locations, and hence are placed in chip before automated placement-and-routing and are called as pre-placed cells.

#### De-coupling Capacitors
![Screenshot (224)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f56e8124-5851-4c81-bc87-c8ac8c10d7a6)

#### Power Planning 
![Screenshot (226)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/2ac6c3df-3dda-44a1-bddc-2ada19b46f16)
![Screenshot (225)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/701a5f8e-69c6-475e-bb5a-76646ebea114)
#### Pin placement and logical cell placement blockage
![Screenshot (227)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/22bc2651-71ad-4eed-ae13-be4040a54939)
![Screenshot (228)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f7ad3e6e-3f31-498f-a6e1-08da5457b29e)
//#### Steps to run floorplan using OpenLANE
#### Review floorplan files and steps to view floorplan
![ut_sys](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/ebc18523-b44f-4594-8044-df9701105385)
SYSTEM DEFAULTS
![ut_2](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/ece79124-e770-4955-b1e0-0ed75d2a6955)
PDK DEFAULTS

![utilization](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/bbff7a66-6266-4d1a-b383-82d9a8855b7e)
TEST DEFAULTS
pdk configured tcl file overwrites design configuration that overwrites the system defaults

floorplan results to  know diearea:
![diearea](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/a6cb6797-4d1a-4480-85d4-0420171cb078)

#### Review floorplan layout in Magic
![floorplan](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5bfa2f91-8c52-49fe-a411-25d746de05e8)
To open Magic give command
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read .. / .. /tmp/merged.lef def read picorv32a.floorplan.def &

### SKY130_D2_SK2 - Library Binding and Placement
####  Netlist binding and initial place design
![Screenshot (231)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/067aeb3c-8582-48e2-a940-671bc59d9af8)

#### Optimize placement using estimated wire-length and capacitance
![Screenshot (232)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/00e33d1d-5eb7-4d25-9844-052c03736919)

#### Final placement optimization
![Screenshot (233)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/c1f2c6ed-ee2d-4aa3-a0eb-d397e24c4823)

#### Need for libraries and characterization
![Screenshot (234)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f0d23982-b7fa-4f62-99d9-6b3ead638d59)

#### Congestion aware placement using RePlAce
![placement_2](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/d1d6fede-87fc-43f9-9cb3-19dc267d9998)
![placement](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/2f7a7904-9bd8-4335-bf67-f83f7b9cfaa4)
To open Magic give command and to see placement
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read .. / .. /tmp/merged.lef def read picorv32a.placement.def &

### SKY130_D2_SK3 - Cell design and characterization flows
![Screenshot (237)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5fb4beaa-5994-4455-a8c2-9fbb4ce8eec0)
#### Inputs for cell design flow
![Screenshot (238)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/8eabd77a-6d08-4a42-a415-25353ffc9494)

#### Circuit design step
![Screenshot (239)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/d790cd36-dce4-4731-82a0-d0b138356f7c)

#### Layout design step
![Screenshot (240)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/20d46897-1286-4fcb-9c80-0a186914887c)

#### Typical characterization flow
![Screenshot (241)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/e6fb9910-eae6-4938-98cd-97b6595f0057)

### SKY130_D2_SK4 - General timing characterization parameters
#### Timing threshold definitions
![Screenshot (242)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/7b20f20c-a0b5-49f4-ba0b-52dc4d09c967)

#### Propagation delay and transition time
![Screenshot (243)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/b18f6b7a-f091-49b4-bb77-51039fd6df33)

## Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization
### SKY130_D3_SK1 - Labs for CMOS inverter ngspice simulations
#### IO placer revision
0 = unequidistant ports
1 = equidistant ports
2 = compressed ports 
To set this mode give command as shown in the below figure
![equidis](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5f4947a1-6f1f-4562-bbf8-f88e0e37301a)
set ::env(FP_IO_MODE) 1

![dis](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5258d1e8-d569-4328-9fbc-948f0fa4ff50)
set ::env(FP_IO_MODE) 2

#### SPICE deck creation for CMOS inverter
![Screenshot (244)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/2fc6255a-61a6-4947-84c2-8397305c39ed)

#### SPICE simulation lab for CMOS inverter
![Screenshot (246)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/af416398-af5e-4d56-a92a-17d7809705f6)

#### Switching Threshold Vm
![Screenshot (247)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/d200c925-3305-4b6e-b12b-caa33c36cae0)

#### Static and dynamic simulation of CMOS inverter
![Screenshot (248)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/3ae9f69f-5d68-40ae-bc42-e4f627e63979)

#### Lab steps to git clone vsdstdcelldesign
![GIT_CLONE](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/5b40af7e-09ac-44e2-9152-fda38d7fd15a)

![git_clone1](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f49f6b69-9908-4a3e-bb9d-454e2fc9b8e5)

### SKY130_D3_SK2 - Inception of Layout ÃÂ CMOS fabrication process
![Screenshot (249)](https://github.com/vinay-rn31/NA![Screenshot (250)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/91499159-170b-498a-af73-120bd09243ec)
SSCOM_VSD_SoC_Design_Program/assets/168123355/a798e542-70a0-4b4a-92c1-723e567a8ac5)
![Uploading Screenshot (250).png…]()
![Screenshot (251)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/7edf0199-a64d-40c8-890e-a420ab526ce4)

![Screenshot (253)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/77118ba4-fe01-49bb-b69c-17786001cda3)

![Screenshot (254)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/d3346365-b470-4f15-a921-fd8f076f9890)

![Screenshot (255)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/ff10239d-64eb-452e-82c2-ed30ffbb5b4d)

### SKY130_D3_SK3 - Sky130 Tech File Labs
![Screenshot (256)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/7a0d6d66-8cba-4ccc-9100-18be7509b1f5)

![nmos](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/674cfeb1-a287-456f-bd88-96cf8289faee)
NMOS

![pmos](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/13ab7a56-52b6-4016-a746-7c8b5a1b4f95)
PMOS

![n-well](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/d8b498a2-bb44-47e4-9de4-c556f9ff67ae)
N-WELL

![extract](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/88c4c96c-7b54-4941-937e-b5a32a65c126)
RC EXTRACTION

![spice](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/36baaeae-c6a1-4cfa-a7f6-a545fe09bf83)

![spice file](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/983f74ec-422d-41f6-815b-c39878f0fd3a)

![spice file2](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/36dd5d38-705a-4332-80bf-e216f09d2465)

![3](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/0733625a-0ab9-48d4-bee9-162db7fbfeb0)
SPICE FILE

![delays](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/604bebdd-e42b-4a2e-9593-acdc15de6931)

![image](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/243a6219-77bb-4a1b-aede-b87eb028719d)
Rise Transition = x1(80%) – x1(20%) = 2.1823-2.1423 = 0.04ns


![image](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/a2adba5d-da47-4c5e-93fa-335a1f3718fe)
Fall transition = 4.0866-4.04613 = 0.04047nsec

![image](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/30c4700f-2fae-45b7-824a-e5428b51c047)
RISE PROPAGATION DELAY= 4.065-4.05 = 0.015nsec


![graph](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/56b3b155-dd88-447d-a097-ba89d9e5a51c)
TRANSIENT ANAYLISIS OF INVERTER

![GRID](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/6e9c7e92-06da-4718-8b4b-4ea2a0990ac9)
GRID CHANGING TO REQUIRED GRID


## Sky130 Day 4 - Pre-layout timing analysis and importance of good clock tree
### SKY130_D4_SK1 - Timing modelling using delay tables
![Screenshot (257)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/58631a15-f06d-4c4a-8c09-60baf30279d4)

![Screenshot (258)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/77c774b5-088d-49f3-a40d-1ba241b9ad4c)

![Screenshot (259)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/da28297c-bbd1-4f1a-8af7-a2417c6fc6a4)

![TRACKS](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/8ae11c78-e11b-45b8-a7e2-614e79c6528c)
TRACK FILE INFO
tracks.info which is used in the routing

### SKY130_D4_SK2 - Timing analysis with ideal clocks using openSTA
![Screenshot (260)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/72a6d0c5-261c-401f-9b20-1cfd58368eaf)

![Screenshot (261)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/cb567673-05f9-498f-8ddb-2f507bfe763c)

### SKY130_D4_SK3 - Clock tree synthesis TritonCTS and signal integrity
![Screenshot (262)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/4b219c6a-cb6d-4380-a0a8-7d3fbbfcc93a)

![Screenshot (263)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/75b23b60-09e5-48b2-ae93-10e2644d3715)

![Screenshot (264)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/58c7b51b-7f0f-4c27-87c3-3c3047a65423)

### SKY130_D4_SK4 - Timing analysis with real clocks using openSTA
![Screenshot (265)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/90737fb8-5d62-4a8e-9e26-7e4293baa569)

## Sky130 Day 5 - Final steps for RTL2GDS using tritonRoute and openSTA
### SKY130_D5_SK1 - Routing and design rule check (DRC)
![Screenshot (266)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/e82fbfc4-df67-4cf8-b459-a13fd9fd28c5)

![Screenshot (267)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/1393c5f2-a48f-440b-9eda-23a78e6203a2)

![Screenshot (268)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f2f11359-77a8-4892-bbbf-641d7ab12155)

### SKY130_D5_SK2 - Power Distribution Network and routing
![Screenshot (269)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/568e2923-d679-4c36-b1c9-5d685a2146c5)

### SKY130_D5_SK3 - TritonRoute Features
![Screenshot (270)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/f6530066-71f9-4df3-8705-08acd82b3229)

![Screenshot (272)](https://github.com/vinay-rn31/NASSCOM_VSD_SoC_Design_Program/assets/168123355/3645953b-59d2-4a91-beb1-d90d86a4fefd)
