# Using a Pre-trained Image Classifier

## Running a Program using command line arguments

To run a program like check_images.py, first, open a terminal window within the Project

    python check_images.py

To run a program like check_images.py using the command line argument --dir specifying the images directory

    python check_images.py --dir pet_images/

### Choosing another architecture

    python check_images.py --dir pet_images/ --arch resnet

### Choosing a labels file to the different classes

    python check_images.py --dir pet_images/ --dogfile dognames.txt

## Batch Processing

    ##  Code from run_models_batch.sh 
    python check_images.py --dir pet_images/ --arch resnet  --dogfile dognames.txt
        > resnet_pet-images.txt
    python check_images.py --dir pet_images/ --arch alexnet  --dogfile dognames.txt  
        > alexnet_pet-images.txt
    python check_images.py --dir pet_images/ --arch vgg  --dogfile dognames.txt 
        > vgg_pet-images.txt


 Each file ends with `> filename.txt`. The `>` is a pipe and it pipes the output from the console into a file. The file contains the filename of the model being used. This way after each run, the results are automatically stored in your workspace.

 ### To run file run_models_batch.sh

    sh run_models_batch.sh

#### NOTE: The Batch processing used here can't be used on windows
