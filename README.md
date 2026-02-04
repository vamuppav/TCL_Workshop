# _TCL_Workshop_
_Author: Venkata Akhil Muppavarapu_

_Acknowledgements: TCL Workshop by Mr. Kunal Ghosh , VLSI System Design_

## Introduction
TCL (Tool Command Language) is a scripting language widely used in VLSI and EDA workflows for tool control and automation. It enables engineers to automate design flows, process input files, configure constraints, and generate outputs such as timing constraints and reports. Due to its simplicity and flexibility, TCL is the standard interface language for most industry EDA tools.

## DAY 1

__Create Command (tclbox) and pass csv file from UNIC shell to Tcl script__

* We let the system know its a UNIX script by ```  #!/bin/tcsh -f ```
* we can create our own logo for letteing the user know more about the provider.

* Then we verify three general scenarios for a user point of view
   1. When user doesnt enter the csv file
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/015e44b0b8feb3879014eb96dabbabc772d1315d/1..png)
  
   2. When user enters the wrong csv file/ file doesnt exist
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/015e44b0b8feb3879014eb96dabbabc772d1315d/2..png)
 
   3. when user enters __-help__
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/015e44b0b8feb3879014eb96dabbabc772d1315d/3%2C..png)
* Then we source the Unix shell to the Tcl script by passing the required csv file

  ```
  tclsh tclbox.tcl $argv[1] 
  ```
  Ensure the file has execution permissions by running: ``` chmod -R 777 panda ```

  ## DAY 2 & 3 
  
  CSV Processing and SDC Constraint Generation
     - Validated all files and directories referenced in CSV inputs  
     - Converted `constraints.csv` into a matrix for structured processing  
     - Computed row and column indices using matrix-based algorithms  
     - Identified and generated complete clock constraints (period, latency, slew) in SDC format  
     - Classified input ports as single-bit or bussed using pattern matching  
     - Parsed Verilog netlists to extract and normalize input port definitions  
     - Removed duplicate ports through sorting and uniquifying logic  
     - Generated input and output port constraints in SDC format, completing the end-to-end flow
       
Note: Identifing bussed and non-bussed input and output ports before formatting them for further processing is necessery.
  
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/f58bca9c97642d0abe3c08e6db5c2da9b0f6710e/4..png)
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/f58bca9c97642d0abe3c08e6db5c2da9b0f6710e/54..png)
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/f58bca9c97642d0abe3c08e6db5c2da9b0f6710e/6..png)
   ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/f58bca9c97642d0abe3c08e6db5c2da9b0f6710e/7..png)


SDC file
    ![image _alt](https://github.com/vamuppav/TCL_Workshop-/blob/62c813c6e4f7fb6e5cd5ea6973b55b4a5f0c6d8f/8..png)


## DAY 4






       

  
