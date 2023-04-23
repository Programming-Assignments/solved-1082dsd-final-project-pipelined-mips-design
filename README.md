Download Link: https://assignmentchef.com/product/solved-1082dsd-final-project-pipelined-mips-design
<br>
In final project, you are asked to design a <strong>pipelined MIPS processor (synchronous active low reset) with instruction cache and data cache</strong>. This processor should at least support the instruction set defined in Table 1. The instruction set is referenced from Appendix A of [1], and we encourage you read it in detail.




The whole module hierarchy is shown in Figure 1. And the processor architecture is shown in Figure 2 referenced from Chapter 4 of [1]. As you see, the processor architecture is modified from single-cycle architecture of our HW3. Your design should follow this <strong>5-stage pipelined architecture</strong>. You need to modify several parts to fit our specifications. For example, you need to add the path for <strong>J-type instructions</strong>.




Also, you should <strong>solve the hazards</strong> by adding some circuits. There are 3 hazard categories should be properly handled in your pipelined processor:

<ul>

 <li>Structure hazard</li>

 <li>Data hazard</li>

 <li>Branch hazard</li>

</ul>

Although all of these hazards can be solved by insert NOP manually or automatically in your test program, we ask you to implement <strong>data forwarding unit</strong> and <strong>pipeline stall unit</strong> to solve these hazards.







<strong>Figure 1.</strong> Module Hierarchy




<strong>Figure 2.</strong> Simplified Pipeline Architecture of MIPS.




<h1>2.    Cache and Memory Interface</h1>

The instruction memory and data memory will not be contained in your design. The memory interface is left as module I/O. You have to use the provided slow memory model. <strong>Do not</strong> <strong>synthesize the slow memory. </strong>




The cache units are suggested to have the same block number (8) and block size (4) as those in HW4. Besides, we do not restrict the replacement policy and writing policy of the cache design. You are encouraged to optimize the cache units to fit your MIPS design.




<h1>3.    Synthesis Notes</h1>

You should synthesize your design using TSMC 0.13 cell library, and the relevant files, e.g. <em>.synopsys_dc.setup</em>, can be copied from previous HW or use the attached file. The design constraints are specified in “<em>CHIP_syn.sdc</em>”. Note that the pipelined MIPS, instruction cache, and data cache are included in the <em>CHIP.v</em>. They should be synthesized together.




The post-synthesis simulation is required and all involved Verilog files should be all modeled by gate-level. Note that the maximum clock frequency must be verified by post-synthesis gate-level simulation. And you are recommended to buffer the input signal to avoid timing violation.