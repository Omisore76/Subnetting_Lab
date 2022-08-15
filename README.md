# Subnetting_Lab

Subnetting is a way of dividing up a network into smaller sections. It's often used in larger networks to help improve efficiency and performance.
I used a real-life example to help me understand it better. I pretended that I was a network administrator for a small company. The company had been given a subnet of 194.150.0.0/24. I was required to create two subnets from this address.

My approach:
First, I identified the network and the host portion of the given subnet. From the given subnet mask, I knew 24 out of the 32 bits was being used for the network portion. That left me with 8 bits for the host portion. So, the network portion was 194.150.0, and the host portion was 0.

Next, I figured out the number of bits that needed to be borrowed from the host portion of the original subnet to create new ones. In this case, it was 1 bit, resulting in 2 subnets (2^1).

Then, I calculated the new subnet masks for each subnet. To achieve this, I added the borrowed bit to the default 24-bit subnet mask. Hence, the new subnet mask was 25, which could also be written as 255.255.255. 128.
I set the bit borrowed to 0 and 1. This gave me the two required subnets:
               194.150.0.0/25
               194.150.0.128/25

I configured my computers and the routers. I assigned the subnet 194.150.0.0/25 to site one and 194.150.0.128/25 to site2. The router in each site was configured as the default gateway, which allowed devices on one site to communicate with devices on the other site. Finally, I tested the network by pinging both sides and verifying that the connection was working properly.
