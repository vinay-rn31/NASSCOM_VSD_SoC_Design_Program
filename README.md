
# DIGITALL VLSI SOC DESIGN AND PLANNING
## Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK
### SKY130_D1_SK1 - How to talk to computers
### SKY130_D1_SK2 - SoC design and OpenLANE
### SKY130_D1_SK3 - Get familiar to open-source EDA tools

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
### SKY130_D3_SK2 - Inception of Layout ÃÂ CMOS fabrication process
### SKY130_D3_SK3 - Sky130 Tech File Labs


## Sky130 Day 4 - Pre-layout timing analysis and importance of good clock tree
### SKY130_D4_SK1 - Timing modelling using delay tables
### SKY130_D4_SK2 - Timing analysis with ideal clocks using openSTA
### SKY130_D4_SK3 - Clock tree synthesis TritonCTS and signal integrity
### SKY130_D4_SK4 - Timing analysis with real clocks using openSTA

### Sky130 Day 5 - Final steps for RTL2GDS using tritonRoute and openSTA
### SKY130_D5_SK1 - Routing and design rule check (DRC)
### SKY130_D5_SK2 - Power Distribution Network and routing
### SKY130_D5_SK3 - TritonRoute Features
