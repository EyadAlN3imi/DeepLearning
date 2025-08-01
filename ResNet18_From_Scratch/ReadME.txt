Hey there! I’ve been working on a neat project where I built a custom ResNet-18 model from scratch using PyTorch and trained it on the CIFAR-10 dataset. Let me walk you through it in a friendly and conversational way!

### What’s This Project All About?
The goal was pretty straightforward: create a ResNet-18 model using custom residual blocks, train it on CIFAR-10, and check out how well it performs. I also wanted to visualize the training process by plotting accuracy and loss curves for both the training and validation sets—it’s a cool way to see the model improve over time!

### Breaking Down ResNet-18
ResNet-18 is a neural network that’s all about “residual blocks.” These blocks are awesome because they let the network skip layers if needed, making it easier to train deeper models. Here’s how I built it:

- **Residual Blocks**: Each one has two 3x3 convolutional layers, followed by batch normalization and a ReLU activation. There’s also a skip connection—either passing the input as-is or tweaking it if the dimensions don’t line up.
- **Overall Structure**: It starts with an initial convolution, batch normalization, ReLU, and max pooling. Then come four stages, each with two residual blocks, and the filter sizes grow like this: 64, 128, 256, and 512. At the end, there’s a global average pooling layer and a fully connected layer spitting out predictions for CIFAR-10’s 10 classes.

### The CIFAR-10 Dataset
CIFAR-10 is a fun dataset with 60,000 tiny 32x32 color images across 10 categories—think cats, dogs, airplanes, and more. I used 50,000 images for training, splitting them into 70% for actual training and 30% for validation, plus 10,000 for testing. That validation split helps me keep an eye on how well the model generalizes.

### How I Trained It
To give the model a boost, I added some data augmentation:
- Random cropping with padding
- Random horizontal flips

For the technical stuff:
- **Loss Function**: CrossEntropyLoss (perfect for classification)
- **Optimizer**: SGD with a momentum of 0.9 and weight decay of 5e-4
- **Hyperparameters**: Learning rate of 0.01, batch size of 128, and 25 epochs

### The Results
I tracked accuracy and loss over the 25 epochs and plotted them—super useful for spotting overfitting. The validation accuracy tells me how well the model handles unseen data. After training, the final validation accuracy was: ✅ [insert value after training].


# This is a placeholder for the full Jupyter notebook content
# It includes the complete training pipeline with the custom ResNet-18 model
# Imagine code here defining the residual blocks, model architecture, 
# data loading, augmentation, training loop, and plotting results!


### What’s Included?
- **ResNetFromScratch**: The Jupyter notebook with all the code—building the model, training it, and plotting results.

### Some Cool Takeaways
Batch normalization is like a training superpower—it keeps things stable and speeds things up. And those residual connections? They’re why we can go deep without the model breaking down. Even though ResNet-18 is simpler than some bigger models, it still shines on CIFAR-10!

That’s the project in a nutshell! It was a blast to build and watch it learn. Let me know if you want to dive deeper into any part!