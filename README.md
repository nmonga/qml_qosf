# A Simple Solution for Task 2 of the QOSF Mentorship Program Evaluation

This repository provides a simple solution to task 2 as part of the evaluation for the QOSF mentorship program. To re-iterate, task 2 requires a mapping of 4 random 4 quibit states onto specific target states. We utilize a cost function, which when minimized maximizes the fidelity between the input states and the required target states. 

Note that for noisier or real world data, more elegant solutions may instead maximize the cumulative fidelities between the set of input states and the set of output states (i.e. equivalently minimzing the associated cost), or for instance if such states were to be identified via features from a noiser dataset, say for a classification task one could use a softmax function with the Forest-SDK. 

Here instead we use argmax instead to identify which of the set of parameters will correctly map our random input states to the target staes, noting that for each random state, the best fidelity is likely to be produced only by one of the 4 sets of parameters (since the parameters were obtained by training the same circuit for each mapping separately, we store only the parameter values for each transformation and use these as part of a classifier/transformer).

I have not used many packages for this besides Pennylane, PyTorch and Pandas, so the notebook should work "out of the box". Nevertheless I have included a virtual environment containing the python version that I used along with a requirements.txt file where the environments can be loaded in the usual way. If any difficulty presents the following steps can be repeated, 

```python3 -m venv qml-venv```

```source qml-venv/bin/activate``` 

And finally we can install the requirements by running the shell script (nothing special here - just an old habit :) )

```sh install_requirements.sh```

Thanks Much. 

Nikhil
