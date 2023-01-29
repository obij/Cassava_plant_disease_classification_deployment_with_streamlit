# Cassava_plant_disease_classification_deployment_with_streamlit
Using deep learning to classify and identify diseases present on a cassava leaf image

<h2><b>Abstract</b></h2>
Cassava is fourth on the list of important food crops in developing nations, after rice, wheat and maize, based on FAO statistics from 1987. It is estimated around 500 million people depend on it, as a source of food and in some nations, cassava accounts for more than 50% of the food they consume on a day to day basis.<br>
<br>
For a group project, for our internship in our Applied Artificial Intelligence course, at Teesside University UK, our group had to train a deep learning model to accurately classify and identify cassava plant diseases. The final model was also deployed to a web app using streamlit.<br>
<br>
We were able to achieve accuracies of 100% on the training data, 95.12% on the validation data and 95.34% on the test data for our best performing transfer learning model, the ResNet50. Callbacks and early stopping were applied to the training, as well as weight regularization to counter overfitting.<br>
<br>
For future work, we could also try to deploy the model to a mobile app, as well as extend the project ot other crops.<br>
<br>
<h2><b>Overview and Background</b></h2>
It is estimated around 500 million people depend on cassava as a source of food and in some nations, cassava accounts for more than 50% of the food they consume on a day to day basis.<br>
<br>
Four common diseases that plague cassava are: Cassava Brown Streak Disease(CBSD), Cassava Green Mite(CGM), Cassava Bacterial Blight (CBB) and Cassava Mosaic Disease (CMD). We got a dataset from kaggle that had images of cassava leaves that were afflicted with these four diseases as well as images of healthy leaves. So we had to train a deep learning mdoel that could accurately classify an image of a cassava leaf plant into one of these classes.<br>
<br>
We actually trained various deep learning models, compared them and chose the best performing one. As an added innovation, we also deployed the best model to a web app.<br>
<br>
<h2>Goals</h2>
This project is the internship project, my group undertook for our internship at Teesside University, in our Applied Artificial Intelligence masters programme
.<br>
<br>
For this project, our goals were the following:
<ol>
<li><b>Investigation and exploration of cassava disease images: </b></li> We explored some of the images in the various cassava disease classes
<li><b>Data visualization and Data augmentation of the data set: </b></li> We visualized the dataset in multiple ways, detected class imbalance and did data augmentation to help correct the imbalance
<li><b>Training the various deep learning models and selecting the best performing model: </b></li> We trained various models, compared their performances and selected the best performing model.
<li><b>Loss and Accuracy  analysises of the various models:</b></li>We also analysed and compared the loss and accuracy curves of the models from the training.
<li><b>Deployed the best performing model to a web app using streamlit: </b></li> Using streamlit, we deployed the best performing model to a web app, so the model can be conveniently accessed from the web app.
<li><b>Conclusions:</b></li>We drew conclusions and made suggestions and recommendations for future work.
</ol><br>
<br>
<h2>Data Details</h2>
Data credits: https://www.kaggle.com/competitions/cassava-leaf-disease-classification/overview<br>
<br>
The dataset came from a Kaggle competition that had a dataset of about 21,000 labelled images collated at Uganda. The images were gotten from farmers taking pictures of their cassava crops and were labelled by the scientists at the National Crops Resources Research Institute (NaCRRI)in conjunction with the Makere University AI lab. it is in a format that captures a good essence of the type of diseased cassava plants farmers would tend to encounter.<br>
<br>
The cassava leaves were classified into 5 classes:
<ul>
<li>CBB</li>
<li>CBSD</li>
<li>CGM</li>
<li>CMD</li>
<li>Healthy</li>
</ul><br>
<br>
Below are examples of each image class:
![train-cbb-464](https://user-images.githubusercontent.com/53709283/215355221-2980ce69-fb43-48d6-825a-0aa44141dba7.jpg)<br>
<br>
![train-cbsd-1441](https://user-images.githubusercontent.com/53709283/215355261-2ff5e8ae-1595-477b-b121-21e5d8db41fb.jpg)<br>
<br>
![train-cgm-748](https://user-images.githubusercontent.com/53709283/215355291-dd5f7be4-28b9-44f1-8170-fcf74f2ab324.jpg)<br>
<br>
![train-cmd-2629](https://user-images.githubusercontent.com/53709283/215355317-cf976300-2da3-478d-9e3d-703dc6773ef9.jpg)<br>
<br>
![train-healthy-309](https://user-images.githubusercontent.com/53709283/215355329-558cf3e2-2831-46cc-8564-613de52e1bed.jpg)<br>
<br>
Some of the important folders in the dataset directory are:
<ul>
<li>train_images:</li> The approximately 21,000 training images to be used to train the models <br>
<br>
<li>train_csv: </li> table file linking the image ids of the training images to their class labels or DiseaseNames<br>
<br>
</ul>
<h2>Outcomes of the Project</h3>
We trained about five different models namely: a basic CNN, the EfficientNetB4, the VGG16, the inception V3 and the Resnet50. The last four are all transfer learning models. Also, all these five models initially appeared to be overfitting, as they all had poor accuracies on the test dataset. However, by using weight regularization on the ResNet5o, to counter overfitting, we were able to improve its accuracy to 95.34% on the test data, while it had an accuracy of 100% on the training data and 95.12% on the validation data. it was thus the best performing model. It was also saved and was the model deployed to the web app<br>
<br>
Below are the accuracy and loss curves for the ResNet50 (with weight regularization):
![image](https://user-images.githubusercontent.com/53709283/215356074-af4f6f22-c6a5-40fe-b028-6b9754d3a66e.png) <br>
</br>
![image](https://user-images.githubusercontent.com/53709283/215356145-29f2218c-7615-4d49-875d-965438558306.png)<br>
</br>
<h2>Deploying the model to a web app using streamlit</h2>
To deploy the model to web app,  using streamlit, follow the following steps:
<ol>
<li>Clone this repo to your local machine</li>
<li>Open Anaconda command prompt on your desktop and navigate to the folder, where the repo is</li>
<li>iF this is your first time deploying the model to the web app, you first need to install the dependencies listed in the requirement.txt file before you can run the app. To do so, in the command prompt, type: pip install -r requirement.txt</li>
<li>In the command prompt, run the file by typing: streamlit run streamlit_host.py</li>
</ol><br>
<br>
<h2>Conclusions, Future Work</h2>
The ResNet50 model that was trained with weight regularization gave the best performance and was the model deployed to the web app.<br>
<br>
So for future study, it would be interesting to:
<ol>
<li><b>Compare more transfer learning models :</b></li> Compare more transfer learning models with our best performing model.
<li><b>Deploy the model to a mobile app: </b></li>It would even be more convenient to deploy the model to a mobile app.
<li><b>Extend the project idea to other crops:</b></li>Extend the project idea to other crops like tomatoes, that are also seriously affected by diseases.
</ol>
<br>
<br>
<b>Note:</b> The trainings were done on Google collab in order to utilize the GPU on the platform.<br>
<br>
<b>Contributors/Group Members:</b> Obinna .J. Okafor, Okala Nwoke, Theophilus Otajonor, Ozoene Ikenna, Martin Toxifarian, Ohanme Bartholomew, Ogunleye Adebayo<br>
<br>
<b>Languages:</b> Python<br>
<br>
<b>Tools/IDE:</b> Google colab, Visual Studio Code<br>
<br>
<b>Libraries:</b> numpy, matplotlib, streamlit, datetime, tensorflow, keras, os, opencv













