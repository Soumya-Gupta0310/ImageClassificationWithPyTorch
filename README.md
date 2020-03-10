# ImageClassificationWithPyTorch
### Required Installation:-
1. Download and Install the Anaconda3 Distribution
2. Open the Anaconda Prompt
3. Type the following command to install cuda:-
```bash
conda install -c anaconda cudatoolkit
``` 
### Files to run:-
1. train.py (This file is used to train the classifier with images)
2. predict.py (This file is used to load the already trained classifier to predict new image content)

### Arguments to be passed while running the files:-
  #### Arguments for train.py:-
      a. data_directory i.e. the directory in which the training and validation images are present (This argument is mandatory)
      b. save_directory i.e. the directory in which the information about the trained model  will be saved as checkpoint (optional argument)
      c. model architecture(optional argument)
      d. learning rate (optional argument)
      e. hidden_units i.e. the number of nodes in each of the three hidden layers (optional argument)
      f. epochs (optional argument)
      g. gpu - If this argument is passed, the model will be trained on gpu (optional argument) 
      
   #### Example command for running train.py:-
```bash
python train.py "DirectoryPathContainingTrainingandValidationImages"
``` 
Or,

```bash
python train.py "DirectoryPathContainingTrainingandValidationImages" --save_dir "save_directory" --arch "vgg13" --learning_rate 0.001 --hidden_units "[1536,1024,512]" --epochs 5 --gpu
``` 
      
  #### Arguments for predict.py:-
      a. input i.e. the complete path of the image to be predicted (This argument is mandatory)
      b. checkpoint i.e. the complete path of the file containing the model checkpoint (This argument is mandatory)
      c. top_k i.e. the top k number of categories having highest probabilities (optional argument)
      d. cat_to_name i.e. the complete path of the file containing category to name mapping (optional argument)
      e. gpu - If this argument is passed, the model will make the prediction with gpu enabled (optional argument) 
      
  #### Example command for running train.py:-
```bash
python predict.py "CompletePathOfTheTestImage" "CompletePathForModelCheckPoint"
``` 
Or,

```bash
python predict.py "CompletePathOfTheTestImage" "CompletePathForModelCheckPoint" --top_k 5 --cat_to_name "CompletePathOfTheJsonFileContainingCategoryToNameMapping" --gpu
``` 

### Steps to Run the train.py file:- 
1. Clone the repository in your local machine. The url is:- https://github.com/Soumya-Gupta0310/ImageClassificationWithPyTorch.git
2. Open the Anaconda prompt
3. Run the train.py or the predict.py file as required. 

