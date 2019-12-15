# UDLND---Project-5---Generate-Faces

This project involved building a CNN GAN to generate faces using the CelebA data set.  GANs have gotten a lot of attention in the press for producing realistic faces, and it was a lot of fun learning what they are all about and how to train them.  

## Learning Process

I kept running into a problem where my model produced identical images that were static or random, brightly-colored noise, but I believe this was because I forgot to run zero_grad on the generator.  Before I realized this I assumed that the problem came from the detector being too good early on, and I tried to bound the training of the detector to the loss score of the generator.  This was the first time that I tried to get creative with the network and normal coding (if/then).  It didn't work very well because I hadn't found the zero_grad mistake, but it did work somewhat.  It led me to question why that is not seen more often in neural networks.

## Conclusion

Of all the projects I did for these courses, this is the one that I really wanted to revisit to see if I could make the generated faces in higher definition.  The low resolution kind of detracts from the enormity of the accomplishment, but even this small result took a lot of training and wasn't completely finished when the project was good enough to pass.  It was neat to see how fragile the relationship is between the generator and detector.  They have to find a Nash Equilibrium in the Game-Theory sense in order to compete against each other affectively and produce realistic images from random noise.  I learned a lot.
