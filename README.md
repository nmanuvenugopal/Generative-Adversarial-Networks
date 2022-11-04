# Generative-Adversarial-Networks

This type of network consist of two layers: 
1. Generator layer 
2. Discriminator layer.

Layer construction is almost similar to the autoencoder model. we will be creating the Generator layer and Discriminator layer and combine both of them to form a GAN model.
![image](https://user-images.githubusercontent.com/99719105/199973620-aa58d8fd-7994-4a14-8d69-11451db6e016.png)


Generator layer mainly received the noise in the form of Gaussian distribution. It will create a fake images based on the noise.

However the Discriminator layer takes the inputs which will be combination of real images from original datatset and fake images from the generator. Then it will try to classify the real and fake images. Important point to be noted here is that classification will be always binary classification as it classifying the real (1) and fake (0) images.

Things to note while training the Discriminator
1. We need to create the noises
2. Pass the image through the generator to create noisy or fake images.
3. Combine both fake and real images.
4. Create the corresponsing target labels such that original images maps to 1 and fake images maps to 0.
5. Feed it to Discriminator to train
6. We need to make the traininable parameter of discriminator to True while training phase 1
![image](https://user-images.githubusercontent.com/99719105/199976238-9a8f6258-adff-4ffd-b595-c12431e3086a.png)


Thinngs to note while training the Generator.
1. Create some noise.
2. Create a targetv labels y2 such that it maps fake images to 1.
3. Feed the noise and target labels to GAN network.
4. Since this is pahse 2 we need to make the traininable parameter of discriminator to False.
![image](https://user-images.githubusercontent.com/99719105/199976413-eba747aa-c950-49c5-b840-1db2b708ee82.png)


If we want to see the GAN generted images then 
![image](https://user-images.githubusercontent.com/99719105/199976701-99da098f-d3e4-449e-ba95-c59a9d6b65b1.png)

![image](https://user-images.githubusercontent.com/99719105/199976797-0be8955f-5c4c-4346-8358-7184a68f6e4d.png)


Reference : Udemy tutorial on Deep learning by Jose Potilla
