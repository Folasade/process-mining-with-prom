# Process-mining-with-ProM

## Overview

In this project, the process of a road traffic fine management was mined with the Prom Tool

## Environment Setup
Event Log: Public data from the future learn process mining with Prom course.

Tool: Prom Lite 1.2

## Method
### Algorithm:
Inductive miner chosen to mine the process as it guarantees sound process models. 

### Conformance Check:
Method: Conformance checked by replaying the event log on the process model discovered.

### Settings: 

a. Setting for the process discovery, 

   * Variant - Inductive Miner-infrequent(iMf)
    
   * Noise Threshold - 0.02 chosen at first, 0.00 chosen second time.
    
   * Event Classifier: Concept:name
    
   * First, the model was represented with [process tree](https://github.com/Folasade/process-mining-with-prom/blob/master/images/process-tree.jpg), later converted to petrinet notations.

b. Setting for Replay,

   * Transitions were mapped to event classes
    
   * Classifier - MXML Legacy Classifier
    
   * The purpose of the replay - To measure fitness
    
   * Improper Completion - penalized
    
   * Move on node and move on log cost set to 1

## Result of the discovery algorithm: 
    
   * A model is discovered that describes the data. A petrinet notation is used to display the model. 
    
   * The transitions are shown in squares, representing activities taking place in the road traffice fine management. 
    
   * It has a start place and final marking. 
    
   * It has silent transitions.
    
   * A different model is discovered when Noise threshold is set to 0.00

   [Process model with noise threshold set to 0.02](https://github.com/Folasade/process-mining-with-prom/blob/master/images/pmodel-noisethreshold0.02.jpg)
    
   [Process model with noise threshold set to 0.00](https://github.com/Folasade/process-mining-with-prom/blob/master/images/pmodel-noisethreshold0.00.jpg)
    
## Result of conformance checking
 
 Conformance checking is applied on the discovered process model and the input event log, result is as follows:

   * The resulting model showed the transitions colored according to the frequency of the activities. 

   * The "Create fine" transition has the highest activity of 16031010

   * Only in one place was no move log occurred
 
   * The "insert date appeal to prefecture" transition showed the trace not conforming totally with the process model. 4001 times, the activity executed       synchronously/correctly and 25 times there was a model move, these activities where not observed in the traces. This means the "insert date appeal to prefecture" activity needs to be checked and recommendation made to address the discrepancy.
   
   * The global statistic shows the trace fitness, how well the data aligns with the model, the data complies 99% with the model. It has a fitness of 0.99168 

   [Replay with noise threshold 0.02](https://github.com/Folasade/process-mining-with-prom/blob/master/images/replay-with-nt0.02.jpg)
   
   [Trace fitness with noise threshold 0.02](https://github.com/Folasade/process-mining-with-prom/blob/master/images/tracefitness-with-nt0.02.jpg)
  
  
  ## Conformance with Noise Threshold set to 0.00
   
   Result with Noise threshold set to 0.00 shows perfect log fitness. Global statistics showed that the data complies 100% with the model, it has a fitness of 1

   [Replay with noise threshold 0.00](https://github.com/Folasade/process-mining-with-prom/blob/master/images/replay-with-nt0.00.jpg)
   
   [Trace fitness with noise threshold 0.00](https://github.com/Folasade/process-mining-with-prom/blob/master/images/tracefitness-with-nt0.00.jpg)
   
   
   
   
