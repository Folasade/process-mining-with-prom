Process Mining With Prom Tool

In this project, the process in a road traffic fine management was mined with the Prom Tool

Event Log: Data was gotten from the future learn process mining with Prom course.

Algorithm Used:
Inductive miner was used to mine the process as it guarantees sound process models. A process model was discovered. 

The conformance check was done by replaying the event log
the event log on the process model discovered.

Result
1. Algorithm used: 
The inductive miner was applied because it guarantees sound process models.

2. Settings used: 
Defualt setting was used. First it was represented with preocess tree, ten converted to petrinet notations.

3. Result of the discovery algorithm: 
A model is discovered that describes the data. A petrinet notation is used to display the model. The transitions are shown in squares. It has a start place and final markings. 
It has silent transitions. Link to the process model here: 
    
4. Conformance checking is applied on the discovered process model and the input event log, result is as follows:

* The resulting model showed the transitions colored according to the freqency of the activities
* The "Create fine" transition has the highest activity of 16031010
* Only one place was no move log occurred
* The "insert date appeal to prefecture" transition showed the trace not conforming totally with the process model. 4001 times, the activity executed synchronously/correctly and 25 times there was a model move, these activities where not observed in the traces.
* The global statistic shows the trace fitness, how well the data aligns with the model,   the data complies 99% with the model. It has a fitness of 0.99168 

