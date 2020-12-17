# Concrete Cracks Classification
Model training guide for detecting cracks on concrete surfaces.

Step 1: In terminal, traverse into the Pipeline folder.

            terminal command : cd pipeline/Concrete_Crack_classification/

Step 2: Activate the tensorflow environment.
    
            terminal command : source activate tensorflow_p36

Step 3: In Pipeline, there are two text files "pospath.txt" and "negpath.txt".
        Each of them containing corresponding paths for folders containing Positive and Negative Images.

Step 4: Splitting data into train and test
        Currently splitting into 80% train data and 20% test data ,it could be changed accordingly.

            terminal command : python train_test_split.py --pos=pospath.txt --neg=negpath.txt
        
Step 5: Data Preprocessing-

            terminal command : python Data_prepration.py

Step 6: Initiate Training

            terminal command : python train.py

Currently Epochs are set to 10 and validation split to 20 percent, it could be changed accordingly.
It will start training our model, and generate an ‘.jpg’ image file displaying accuracy graph.
-Accuracy.jpg

Step 7: Testing on sample

**For single image testing
    It will tell if the image with given path have crack or not in it.

            terminal command : python test.py --path=/home/ubuntu/..image_path../../image_name.jpg
              
    Note: Path for image will starts from home directory. for ex."/home/ubuntu/..folder../ImageName.jpg" 
    
**For multi image testing
    It will show the Results in terms of Accuracy.

            terminal command : python test.py
