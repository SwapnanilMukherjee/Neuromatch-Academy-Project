# Comparison of the Human Brain and Deep Convolutional Neural Network Responses to Natural Images

In this mini-project that was conducted as a part of [Neuromatch Academy: Deep Learning 2022](https://deeplearning.neuromatch.io/tutorials/Schedule/daily_schedules.html), we were interested in comparing the response profiles of the human brain (via fMRI activity) with a neurally-inspired deep convolutional neural network model (via CORnet-Z layer activations) through the implementation of *representational similarity analysis* [(RSA: Kriegeskorte et al., 2008)](https://www.frontiersin.org/articles/10.3389/neuro.06.004.2008/full). 

## Project Description
The human brain interprets the visual world in a stream of hierarchy which involves the collaboration of multiple brain regions in the occipital cortex. The visual information is passed by the lower regions (i.e., V1, V2) by taking into account basic features such as lines and angles to the higher ones (i.e., V4, lateral occipital cortex (LatOcc), IT) which process more complex features such as shapes and the identity of an object. In this project, we focused on the dataset by [Kay et al. (2008)](https://www.nature.com/articles/nature06713) which consists of greyscale natural photographs presented to humans and their corresponding fMRI responses during an object recognition task. Using representational similarity analysis (RSA) [(Kriegeskorte et al., 2008)](https://www.frontiersin.org/articles/10.3389/neuro.06.004.2008/full), we compared the responses to these photos obtained from the human brain and the deep convolutional neural network (DCNN). Here, we examined the role of intermediate regions, which was unaddressed in the original study. We compared the response profiles of four region-of-interests (ROIs) (V1, V2, V4, LatOcc) from the experiment with the convolutional layers of the CORnet-Z model [(Kubilius et al., 2018)](https://www.biorxiv.org/content/10.1101/408385v1). We divided the stimuli into four hierarchical classes, one for each level of hierarchy (from general to more specific), and as a result, four distinct CORnet-z model instances were produced. We first used a model that had been pre-trained on ImageNet (Deng et al., 2009), then we fine-tuned this model using the training data, hence creating representational dissimilarity matrices (RDMs) corresponding to each of the four ROIs. We then compared these to the RDMs generated directly from the response profile of the brain. In the case of the aforementioned intermediate regions playing a significant role during the task, we anticipated that the DCNN model would also behave in a similar fashion.

![An example set of natural images used in the project](https://github.com/batiyilmaz/NMA-DeepLearning-Natural-Photographs-DCNNvsHumanBrain/blob/main/example_set_images.png)

**An example set of natural images used in the project**

### Code Organization
The code for the fMRI and CORnet-Z model responses is stored in the same subdirectory called *Code*. The code was written in Python.
