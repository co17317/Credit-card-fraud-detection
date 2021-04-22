## Credit Card Fraud Detection 

**1.Overview**  - In this project, we try to identify the fradulent applications for credit card using hybrid model consisting of 
self orgainizing maps and neural network.This project was done as a part of Deep Learning A-Z course on Udemy.

The Jupyter notebook with the hybrid model (SOM + NN) can be found [here](https://nbviewer.jupyter.org/github/abishekarun/Credit-Card-Fraud-Detection/blob/master/hybrid_som.ipynb).

**2.Introduction** - 
A self-organizing map (SOM) is a type of artificial neural network that uses unsupervised
learning to build a two-dimensional map of a problem space. The key difference between a
self-organizing map and other approaches to problem solving is that a self-organizing map
uses competitive learning rather than error-correction learning such as backpropagation with
gradient descent. A self-organizing map can generate a visual representation of data on a
hexagonal or rectangular grid. Applications include meteorology, oceanography, project
prioritization, and oil and gas exploration. A self-organizing map is also known as a selforganizing
feature map (SOFM) or a Kohonen map.

The aim is to make all the nodes in the
network respond differently to different inputs. A self-organizing map makes use of
competitive learning where the nodes eventually specialize. When fed input data, the
Euclidean distance, or the straight-line distance between the nodes, which are given a weight,
is computed. The node in the network that is most similar to the input data is called the best
matching unit (BMU). As the neural network moves through the problem set, the weights
start to look more like the actual data. The neural network has thus trained itself to see
patterns in the data much the way a human see. The approach differs from other AI
techniques such as supervised learning or error-correction learning, but without using error or
reward signals to train an algorithm. Thus, a self-organizing map is a kind of unsupervised
learning.

**3. Basic structure** - 
The self-organization process involves four major components:
Initialization: All the connection weights are initialized with small random values.
Competition: For each input pattern, the neurons compute their respective values of a
discriminant function which provides the basis for competition. The particular neuron with
the smallest value of the discriminant function is declared the winner.Cooperation: The winning neuron determines the spatial location of a topological
neighbourhood of excited neurons, thereby providing the basis for cooperation among
neighbouring neurons.

**4. **Working**** - 
Each data point in the data set recognizes themselves by competing for representation. SOM
mapping steps starts from initializing the weight vectors. From there a sample vector is
selected randomly and the map of weight vectors is searched to find which weight best
represents that sample. Each weight vector has neighbouring weights that are close to it. The
weight that is chosen is rewarded by being able to become more like that randomly selected
sample vector. The neighbours of that weight are also rewarded by being able to become
more like the chosen sample vector. This allows the map to grow and form different shapes.
Most generally, they form square/rectangular/hexagonal/L shapes in 2D feature space.
Each node’s weights are initialized. A vector is chosen at random from the set of training
data. Every node is examined to calculate which one’s weights are most like the input vector.
The winning node is commonly known as the Best Matching Unit (BMU). Then the
neighbourhood of the BMU is calculated. The amount of neighbors decreases over time. The
winning weight is rewarded with becoming more like the sample vector. The nighbors also
become more like the sample vector. The closer a node is to the BMU, the more its weights
get altered and the farther away the neighbor is from the BMU, the less it learns.
Best Matching Unit is a technique which calculates the distance from each weight to the
sample vector, by running through all weight vectors. The weight with the shortest
distance is the winner. There are numerous ways to determine the distance, however, the
most commonly used method is the Euclidean Distance.

**5. Dataset** - ![image](https://user-images.githubusercontent.com/46992415/115770907-e8d61e80-a3ca-11eb-9cb0-abc622a8c724.png)

**6. Imported dataset** - ![image](https://user-images.githubusercontent.com/46992415/115771023-10c58200-a3cb-11eb-864a-de696bdec8fb.png)

**7. Result** - ![image](https://user-images.githubusercontent.com/46992415/115771098-289d0600-a3cb-11eb-89fe-02a269643a49.png)




The resources that helped me are:

+ [The Self-Organizing Map](https://pdfs.semanticscholar.org/45e6/c7492d01228a33c295557a0b491ec2b4e20e.pdf)
+ [ Kohonen's Self Organizing Feature Maps](http://www.ai-junkie.com/ann/som/som1.html)
+ [ SOM – Creating hexagonal heatmaps with D3.js](https://www.visualcinnamon.com/2013/07/self-organizing-maps-creating-hexagonal.html)
+ [SOM tutorial](https://algobeans.com/2017/11/02/self-organizing-map/)
