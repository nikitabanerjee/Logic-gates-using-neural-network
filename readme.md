**Artificial Neural Network**<br/>

Artificial neural network (ANN) is the concept that was taken from a biological neural network; ANN is composed of several artificial neurons which are connected by a link. Each neuron takes the input data and performs some function, and the output generated by the node is sent to another node called an activation value.ANN consists of three-layer that are input layer, the hidden layer, and the output layer.<br/>

 **Objective:**<br/>
The main objective of this experiment is to implement logic gates using artificial neural network.<br/>


**Libraries Imported For Execution:**<br/>
Numpy:  Numpy has been used to work with array.<br/>
Matplotlib: Matplotlib has been used for ploting the graph.<br/>
Random: For using random number.<br/>

**Data for Logic gates:**<br/>
X is training set and Y is testing set.For X shape was taken as (4,2).For Y shape was taken as (4,1). Shape are same for all the logic gates<br/>
**And Gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]])<br/>
Y = np.array([[0], [0], [0], [1]])<br/>
**Or Gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]])<br/>
Y = np.array([[0], [1], [1], [1]])<br/>
**Nand gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]]) <br/>
Y = np.array([[1], [1], [1], [0]])<br/>
**Nor Gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]]) <br/>
Y = np.array([[1], [0], [0], [0]])<br/>
**XOR Gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]]) <br/>
Y = np.array([[0], [1], [1], [0]])<br/>
**XNOR Gate:**<br/>
X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]]) <br/>
Y = np.array([[1], [0], [0], [1]])<br/>

**Implementation of AND, OR, NAND, NOR Gates**<br/>
As AND, OR, NAND, and NOR gates are linearly separately, the hidden layer was not used. For implementation, weight and bias were taken randomly, and the was taken for weight is (2,1) and bias (1,1),The activation function used here is a sigmoid function that is 1/(1+np.exp(-h)), and for backpropagation sigmoid derivative has been used. Initially, the epoch value was taken as 0 and was executed up to 500, which was assigned in a variable loop. After finding the error, delta_output and output_update were calculated based on that weight, and bias was also updated. The output shows that the prediction was made correctly, and then the graph has 
been plotted between epoch and error. From the graph, it could be seen that after a certain iteration, the error approaches 0.<br/>

**Implementation of XOR and XNOR Gates**<br/>
The hidden layer was used because XOR and XNOR gates are not linearly separate. For implementation, weight and bias were taken randomly weight is (2,1) and bias (1,1) for the output layer and hidden layer shape was taken for weight is (2,2), and bias(1,2) Activation function used here is a sigmoid function that is 1/(1+np.exp(-h)) and for backpropagation sigmoid derivative has been used. Initially, the epoch value was 0 and would execute up to 500, which was assigned in a variable loop. After finding the error, weight and bias were updated. The error was calculated for the hidden layer, then corrected the output layer's weight and bias and updated the hidden layer's weight and bias. The output shows that the prediction was made correctly, and the graph has been plotted between epoch and error. From the graph, it could be seen that after a certain iteration, the error approaches 0.
