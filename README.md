# **Project Charter**

### Project Overview

  Deep learning has recently contributed to learning state-of-the-art representations in service of various image recognition
tasks. Deep learning uses cascades of many layers of nonlinear processing units for feature extraction and transformation. Recently, researchers have shown that deep learning architectures are particularly vulnerable to adversarial examples, inputs to machine learning models intentionally designed to cause the model to make a mistake (Goodfellow et al 2014). In this paper, we propose three methods for increasing the robustness of deep learning architectures against adversarial examples. Specifically, we propose a biologically inspired multi-task learning (MTL) model, a downsampling model, and a model trained on images created by the generator from a generative adversarial network. Our results show that using these models improve adversarial robustness against universal adversarial perturbations (Moosavi-Dezfooli et al 2016). Additionally, we present a metric for adversarial robustness and provide extensive analysis on how adversarial images are represented in image vector space. 

### Project Approach

  Adversarial images and adversarial inputs in general have been the subject of a number of papers. What causes adversarial images? How are they generated? Are certain networks more resilient to adversarial images than others and if so what does it mean to be resilient and how can we measure a networks resilience? The project aims to answer the questions what does it mean to be an adversarial input, how can we make a network more resilient to adversarial images, and how do we measure resilience. Measuring resilience in a closed form would involve mapping the classification spaces of a network, which may be possible but is out of the scope of our project. Instead we intend to develop a method for comparing the resilience of two networks. This would give us the ability to measure the effectiveness of our techniques for improving the resilience of a network. We intend to run experiments where we train two networks, one network that uses one of our proposed methods for increasing resilience and one standard network as a control. We can then compare the resilience of the two networks and if our modified networks is more resilient than the control we can backup or claim that this method improves resilience. 

### Project Goals (High Level)

* To develop a method for measuring the robustness of a neural network against adversarial images.

* To determine if the discriminator of a GAN can detect adversarial inputs.

* To determine if downsampling improves the robustness of a network

* To determine if multi-task learning increases the robustness of a network


### Risks and How to Avoid Them

    1. Risk - Our metric for adversarial robustness only measures robustness against a certain type of adversarial image. 

    2. Mitigation - Define what we mean by robustness and prove that our metric actually measure that quality either absolutely or relative to other networks.    

    3. Risk - Writing code will take longer than expected.

    4. Mitigation - have modular goals that can be accomplished one by one. If we don’t try out all of our methods for improving robustness we will still have meaningful results.

    5. Risk - The more experienced member of the team may start to resent the less experienced member of the team because they are contributing less to project. 

    6. Mitigation - Talk about realistic expectations for each team member

    7. Risk - The more experienced member of the team may not trust the less experienced member of the team and thus avoid delegating responsibilities to them. This could waste a valuable human resource and make the less experience team member feel under appreciated.

    8. Mitigation - The more experienced team member should trust the less experienced team member initial until they have a working track record. 

    9. Risk - Our method for comparing the robustness of two networks involves finding adversarial images that are adversarial to one network but not adversarial to the other. This may prove difficult than we anticipate. 

    10. Mitigation - If cannot adversarial images prove more universal than we expect that is worthy talking about in and of itself.

# Group Management

  The team works together after class and has weekly meetings with the project advisor Alric Althoff. Because of exploratory nature of the project the development roles will continue to change throughout the quarter. We continue to come up with different ideas for how improve the robustness of a neural network. Individual team members will work on specific ideas. Each team will have autonomy when working on their own idea, but before an idea is pursued it will be questioned by the rest of the group. 

# Project Development

  The project uses python and TensorFlow along with a variety of small open source software packages that be found on our requirements.txt file. We also make use of an AWS GPU for additional computational resources. None of the code requires the use of a GPU, but it does speed up the experiments. All of the code can be found on the project GitHub repository along with instructions on how to run it and how to replicate our experiments. 

# Project Schedule

### Milestones

<table>
  <tr>
    <td>Description / How will you demonstrate completion</td>
    <td>Due</td>
    <td>Person Responsible</td>
    <td>Priority</td>
  </tr>
  <tr>
    <td>Write Inception Net. Report network accuracy on test set with visualizations of network predictions. Post the code.</td>
    <td>Week 4</td>
    <td>Patrick</td>
    <td>Low</td>
  </tr>
  <tr>
    <td>Build pipeline for adding universal perturbations to a dataset. Show visualizations of the process.
</td>
    <td>Week 4</td>
    <td>Davis</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Find a dataset to use for our experiments. Provide reasons for choosing the dataset. </td>
    <td>Week 5</td>
    <td>Patrick</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Preprocess the dataset to fit properly within Inception Net framework. Post code.</td>
    <td>Week 5</td>
    <td>Davis</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Generate Universal Adversarial Images using preprocessed dataset. Write code for getting accuracy of a pre-trained model given some input and labels. </td>
    <td>Week 6</td>
    <td>Patrick</td>
    <td>High</td>
  </tr>
  <tr>
    <td>Write the autoencoder, convolutional autoencoder, and PCA models. Create three datasets by running the adversarial images through the models to use as input for experiments. </td>
    <td>Week 6</td>
    <td>Davis</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Run experiments on auto-encoder, convolutional auto-encoder, and pca models and report accuracy using Patrick's tester code. Write the MTL model. </td>
    <td>Week 7</td>
    <td>Davis</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Formalize method for measuring adversarial robustness. Work on digesting mathematical formalization of our methods of increasing adversarial robustness.</td>
    <td>Week 8</td>
    <td>Patrick</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td>Run experiments to see if multi-task learning improves a networks robustness. Report accuracy. </td>
    <td>Week 8</td>
    <td>Davis</td>
    <td>Medium</td>
  </tr>
  <tr>
    <td> REPORT WORK: See how well these techniques generalize across datasets and across network architectures. Report the results of the experiments done on other networks and other datasets.</td>
    <td>Week 9</td>
    <td>Patrick and Davis</td>
    <td>Medium</td>
  </tr>

  <tr>
    <td>Finalize Video Presentation Stuff.</td>
    <td>Week 10</td>
    <td>Patrick and Davis</td>
    <td>High</td>
  </tr>

</table>
