# Deepfake-Detection-for-Chest-CT-Images

Abstract - Medical imaging is the non-invasive process of producing internal visuals of a body for the purpose of medical examination, analysis, and treatment. Numerous attacks on clinics and hospitals occurred in 2018, resulting in serious data breaches and delays in medical services. When an attacker has access to medical records, they are able to do far more than just demand a ransom or sell the information. One method of creating deepfakes is to inject and remove tumours from medical imaging. Failure to recognise medical deepfakes might result in significant losses of hospital resources or even death. Hence, we attempted to build a machine learning model and train it to carry out detection between original images and deepfakes created and analyse them. 

# Dataset - https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).
Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

# Methodology -

We illustrate the difference between deepfake images and original ones by training a CNN model on both - the original and the deepfake datasets. Hence, the initial part of our project would include the training of an appropriate CNN model on the original dataset. For the initial training, we trained a variant ResNet model on the Chest X-Ray dataset. In ResNets, the technique of skip connections is used. The skip connection connects activations functions of a layer to further layers by skipping some layers in between, and this structure forms a residual block. ResNets are made by stacking these blocks together. For the creation of deepfakes, we to used DCGAN. Overall for creation of deepfake images we used DCGAN, we trained the original dataset with CNN, RenNet18, ResNet50, MobileNetV2 and for testing again CNN.

# Conclusion - 

Among the 4 models we trained on the original dataset, our custom-made CNN model gave the highest accuracy of around 99.6%. The same model, when trained on a dataset of 500 deepfakes generated by our DCGAN model from the original dataset, gives an accuracy of 50%. Thus, our hypothesis that the accuracy of the model drops steeply when the learning from a set of original models is transferred to a deepfake image was found to be true for the given use case. Future work in the project can be the extension and verification of this methodology for other images in the medical field and the generalization of the idea for various other sectors where deepfakes are an issue. 





