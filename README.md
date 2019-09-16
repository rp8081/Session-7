# Session-7

#### In this assignment , We have to design the network (CIFAR10) generated from ENA's macro space search for image classification

#### I have tried to include each and every skip connection (to the best of my visibility).							
#### But because of large number of parameters(470,429)  and skip connection , model training is very slow . 
####  It takes 45 minutes for 1 epoch to run	. I have run it for 15 epoch.

###### The challenge with this assignmnet is , while using skip connection we have to make sure size of channels are same .								
###### How do we make same size ??								
###### For example , let us consider layer 14 which has skip connections from 12,8,6,4,3 and 1.						
###### Obviously there is direct connection from layer 13 as well .			

Layers	Size (height,weidth)
Layer 13	(8,8)
Layer 12	(8,8)
Layer 8	(16,16)
Layer 6	(16,16)
Layer 4	(32,32)
Layer 3	(32,32)
Layer 1	(32,32)


