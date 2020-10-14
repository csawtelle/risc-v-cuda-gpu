Legend: 
  - D<num>: Defintion 
  - T<num>: Task
  - E<num>: Experiment 
  - S<num>: Study
  - C<num>: Comment
Tasks take highest precedence, then experiments or studies. 
Definitions are used for consice speech. 


((D1)): Development-Deployment Process: 
1. Synthesis: translates RTL to logic gates.
2. Implementation: converts logic gates to layout for target FPGA
3. Generate Bitstream: generate FPGA bit file from implementation. 
4. Program Device: load bitstream onto the FPGA.


((T1)): Getting Freedom RTL onto Arty: 

https://github.com/sifive/freedom 

Interested in the verification and data-out. 


((E2)): Direct placement of logic on FPGA: 

An FPGA is comprised of many logic cells. It is assumed, during the compilation process 
(synthesis and implementation) of RTL and constraint files, that the various CLBs are picked 
and routed. It is wondered if this can be controlled via user. Can you place logic in specific 
CLBS->SLICES->LUTS? If this is not possible, at which point does this control stop? Any why so? 

NOTE: An interesting approach would be to analyze report logs produced during Vivado compilation. 


((Q1)) Timing considerations for FPGA implementations: 

Preliminary questions: (these should be understood prior to answering main question)
  - what is the consideration for timing within combinational circuits? 
  - what is the consideration for timing within sequential circuits? 

Assumptions: 
  - Clocking is properly defined within RTL implementation. 
  - Standard constrainst files used for device mapping between RTL and FPGA pins. 
  
At what point duing the development-deployment process is the timing *thought of* or *handled*? 

Is the timing just handled by: (1) writing proper RTL and (2) the compiler, during implementation, 
*considers and possibly adjusts* for timing based on the *type of logic* and or placement of logic 
(which CLB, Slice, and LUT are to be used). 

((S1)): Report logs from Vivado during dev-deploy process: 

The dev-deploy process consists of four key stages. It would be good to study the process by analyzing the 
the various output log files at each stage. Moreover, a study of the various options available to tune the 
compilations, and the subsequent analysis of its effects, would be seemingly useful. 


Other material: 

https://www.reddit.com/r/FPGA/comments/ce1ecv/project_ideas_for_artya7_to_develop_skills/




  

