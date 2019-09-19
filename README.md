# Session-7

#### In this assignment , We have to design the network (CIFAR10) generated from ENA's macro space search for image classification

![alt text](https://github.com/rp8081/Session-7/blob/master/enasdiscoverednetwork.png)

<p>
I have tried to include each and every skip connection (to the best of my visibility). But because of large number of parameters(470,429)  and skip connection , model training is very slow .  						
It takes 45 minutes for 1 epoch to run	. I have run it for 15 epoch.
<p>

#### The challenge with this assignmnet is , while using skip connection we have to make sure size of channels are same .		
#### How do we make same size ??

<p>
For example , let us consider layer 14 which has skip connections from 12,8,6,4,3 and 1.						
Obviously there is direct connection from layer 13 as well .
<p>

<b> Original layers size <b>:- 
![alt text](https://github.com/rp8081/Session-7/blob/master/table1.png)
Before concatenating  these layers ,  we have to make sure they all have same size. 	
Since the minimum size(layer13 and layer 12) is 8. So we will make the size of all layer as 8.	
For this we use tensorflow's space_to_depth (which reduces the size and correspondingly increases the depth) and Lambda from keras.

<b> Changed layers size (space to depth) <b> :- 
![alt text](https://github.com/rp8081/Session-7/blob/master/table2.png)

<p>
The output of this  layer  is (8,8,1856) 				
The depth has increased drrastically because of space to depth transformation.							
I have used 1*1 convolution to reduce number of channels.				
<p>		
				





