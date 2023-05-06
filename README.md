Download Link: https://assignmentchef.com/product/solved-ee526-homework-2
<br>
<strong>Problem 1. </strong>Prove that the softplus function

<em>f</em>(<em>z</em>) = log(1 + <em>e<sup>z</sup></em>)                                                           (1)

is convex in <em>z </em>by showing that its second derivative is positive for all <em>z</em>.

<strong>Problem 2. </strong>Let <strong>z </strong>denote a vector <strong>z </strong>= [<em>z</em><sub>1</sub><em>,z</em><sub>2</sub><em>,…,z<sub>n</sub></em>]<em><sup>T </sup></em>. Let <strong>p </strong>= [<em>p</em><sub>1</sub><em>,p</em><sub>2</sub><em>,…,p<sub>n</sub></em>]<em><sup>T </sup></em>, such that

<em>.                                                              </em>(2)

That is <strong>p </strong>is the output when the softmax function is applied to <strong>z</strong>. Derive the Jacobian matrix

<em>.                                                         </em>(3)

<strong>Problem 3. </strong>Let <strong>z </strong>denote a “logit” vector <strong>z </strong>= [<em>z</em><sub>1</sub><em>,z</em><sub>2</sub><em>,…,z<sub>n</sub></em>]<em><sup>T </sup></em>. Let <strong>p </strong>= [<em>p</em><sub>1</sub><em>,p</em><sub>2</sub><em>,…,p<sub>n</sub></em>]<em><sup>T </sup></em>, such that

(4)

Let <strong>y </strong>denote a probability vector <strong>y </strong>= [<em>y</em><sub>1</sub><em>,y</em><sub>2</sub><em>,…,y<sub>n</sub></em>]<em><sup>T </sup></em>such that <em>y<sub>i </sub></em>≥ 0<em>,</em>∀<em>i </em>∈ [1<em>,n</em>], and = 1. Let <em>J </em>denote the cross entropy between <strong>p </strong>and <strong>y</strong>:

<em>,                                                       </em>(5)

where log is natural logarithm.

Derive the gradient vector

(6)

Hint: You can either use the Jacobian, or directly take the gradient. If you take the derivative directly, without using the Jacobian matrix, then it is helpful to write log(<em>p<sub>i</sub></em>) =

<strong>Problem 4. </strong>Let a neural network be such that it has two neurons in one single layer. The neurons has two common inputs. The model can be described as

<strong>z </strong>= <strong>Wx </strong>+ <strong>b                                                               </strong>(7)

We are given two training points:

(a) When <strong>x </strong>= [1<em>,</em>0]<em><sup>T </sup></em>, <strong>y </strong>= [1<em>,</em>0]<em><sup>T </sup></em>. (b) When <strong>x </strong>= [0<em>,</em>1]<em><sup>T </sup></em>, <strong>y </strong>= [0<em>,</em>1]<em><sup>T </sup></em>.

Page 1 of 2

Note that <strong>y</strong>, the output has been one-hot encoded. Let <strong>X </strong>and <strong>Y </strong>both be the 2×2 identity matrix, denoting the input and output for the training data. Use softmax on <strong>z </strong>and use crossentropy as the cost function, run the forward and backward propagation <em>by hand calculation </em>to update <strong>W </strong>and <strong>b </strong>for two iterations, with the following conditions:

<ul>

 <li>Both initialized to all zeros.</li>

 <li>Learning rate is <em>η </em>= 1.</li>

 <li>Use gradient descent.</li>

</ul>

That is, make two updates of <strong>W </strong>and <strong>b </strong>by hand calculation. You need to show the intermediate steps (values of <strong>z</strong>, <em>d</em><strong>z</strong>, <strong>p</strong>, <em>d</em><strong>W</strong>, <em>d</em><strong>b</strong>, etc).

<strong>Problem 5. </strong>Design a three layer neural network that has the following specifications:

<ul>

 <li>Input dimensions: 57 (all real numbers);</li>

 <li>Output dimension: 1 (binary);</li>

 <li>Layer 1: <em>d</em><sub>1 </sub>neurons, with ReLU (rectified Linear Unit) nonlinearity;</li>

 <li>Layer 2: <em>d</em><sub>2 </sub>neurons, with ReLU nonlinearity;</li>

 <li>Output Layer: 1 neuron, with logistic nonlinearity;</li>

 <li>The objective function is cross-entropy (logistic regression).</li>

</ul>

Use the same training and test data from the Spambase Data Set. Train the neural network using forward and backward propagation and gradient descent.

You can use the DNN.py program available on Canvas. You need to submit the source program, in Python. Also the results on the learning rate(s) used, and training and test errors, and running time should be reported.

<strong>Problem 6.</strong>

Using the code available on canvas DNN.py, experiment with doing classification with the MNIST data set, using the following settings:

<ul>

 <li>Single layer, 10 neurons, softmax + cross entropy objective function.</li>

 <li>Three layers, [(50, ReLU), (50, ReLU), (10, Linear)], softmax + cross entropy objectivefunction.</li>

 <li>Experiment with other neuron settings, with no more than 3 layers, and no more than 150 neurons in total.</li>

</ul>





