Design specifications & understanding: 

Given specification :
 ▪ Vmin (read port) = 0.81V
 ▪ Vmin (write port) = 1.08V when mux 16
 ▪ Vmin (write port) = 0.81V when mux 1 with WL Boost
 Icell = 100uA at wc, 1.08V
 
Understanding:

▪ Sizing of write port is determined on the basis of SNM and write functionality.
▪ Icell needs to be 100uA at worst PVT condition, i.e. SS, Low voltage 1.08V, 125C.
▪ Icell determines the sizing of NMOS stack at the read ports, Icell ↑, Read speed ↑. 

For MUX_1:
 
▪ VDD applied to bitcell is 0.81 V, precharge should charge BL, BLB & RBL up to 0.81 V.
▪ Vmin applied to read and write port is 0.81 V. 

▪ WL boost (Vmin + δ) is employed, Ids of PG ↑, Time to discharge ‘1’ ↓, Write speed ↑.            
  Since SNM constraints, WL boost is used only for MUX_1.
  
▪ Icell needs to be 100uA at worst PVT condition, i.e. SS, Low voltage (1.08V), High Temp.          
  Icell is the discharge current of RBL that flows into the cell when RBL discharges during read.
  
 
 For MUX_16:
 ▪ VDD for write port is given at 1.08 V, whereas for read port it is kept at 0.81 V.
