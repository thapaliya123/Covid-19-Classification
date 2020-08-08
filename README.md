# Covid-19-Classification
Capable of  classifying whether a patient is suffering from Covid-19 or not using X-ray images. 

# Description of files
1. covid_19_dataset_preparation.ipynb
- capable of creating pickle files of datasets for training the network
- Download Covid-19 and normal X-ray images and pass the path of datasets stored in google drive in __DATADIR__ variable
- Optionally, can use two pickle files, for description of pickle file keep reading

2. train_covid19.ipynb
- This is the notebook where whole training process takes place
- Loads the pickle files
- splits the data into training and testing purpose
- Initilize the sequential network using keras
- train the network
- save and load model
- plots confusion matric and classification reports using loaded model

# Description of pickle files
1. features_datasets.pickle
- contains training 50 training data of normal and covid-19 patients x-ray images 
- Each image is resized to (224, 224, 1)
- Final shape: (50, 224, 224, 1)

2. labels_datasets.pickle
- A pickle file containing labels of respective image stored in features_datasets.pickle
- 0 indicates Covid, 1 indicates normal

# Running in Colab
- Open files in colab
- Copy all the files in google drive in a single directory including pickle files
- Copy the pickle files path from google drive directory and paste in train_covid19.ipynb files in variable named i)FEATURES_PICKLE_FILE;ii)LABELS_PICKLE_FILE
- Run the train_covid19.ipynb files
