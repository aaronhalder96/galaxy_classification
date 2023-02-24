# Galaxy Classification
Program to identify type of galaxy when given an image

System Requirements: Python Version >= 3.9.0

To clone the repository with HTTPS, use the following command in your desired directory: <br />
git clone https://github.com/aaronhalder96/galaxy_classification.git

Before running the app, please install the packages mentioned in the requirements.txt file by using the following command: <br />
pip install -r requirements.txt

## Objective
The aim of the project is to develop a program that takes an image as the input and determines if the provided image is that of a galaxy or not. If it determines that it is a galaxy, it proceeds to classify which kind of galaxy it is - spiral, elliptical, or irregular.

## Uses
This project can be used to classify a singular image. For example, if someone wants to see whether a particular image is that of a galaxy or not, this program could be used to identify which galaxy it most closely resembles to and the probability of likeness of the picture to that galaxy. A second usage would be to classify a huge dataset of images. For example, let us consider that a person has 100,000 images of different galaxies on his hard drive and he/she wants to sort these images into respective folders depending on the category of the galaxy. It would be a very time-consuming process for that person to identify each image individually and then sort them. This program could be used to look through each image, calculate its probability of resemblance to a galaxy, and sort it into the correct folder. This could save researchers, scientists, astronomers, etc. hundreds of hours of perusal and classification.

## To train a model
1. Open the terminal and navigate to the repository. <br />
2. Run the following command in the terminal. <br />
python train_network.py -d train_images -m galaxy_new.model <br />
The ‘train_images’ folder has already been provided with some images to allow a new network to be trained. <br />
3. The program should start execution and a model will be trained based on the data inside the “train_images” folder.
4. After execution is over, a new file called “galaxy_new.model” will be created in the main directory.

## To test a single image with the model <br />
1. Open the terminal and navigate to the repository. <br />
2. Run the following command in the terminal. <br />
python classify_single_image.py -m galaxy.model -i 1.jpg <br />
The “galaxy.model” and “1.jpg” files have already been provided. If another model file exists which is to be used for testing purposes (or another image which needs to be tested), the following command format should be sufficient. <br />
python classify_single_image.py -m path_to_model -i path_to_image <br />
3. The program should execute and a new terminal containing a smaller version of the input picture with a classification category and a probability of likeness should be displayed as the output.

## To classify and sort multiple images with the model <br />
1. Open the terminal and navigate to the repository. <br />
2. Run the following command in the terminal. <br />
python classify_multiple_images.py -d test_images/all_images -m galaxy.model <br />
The “galaxy.model” file has already been provided. The “test_images” folder containing 100 images has also been provided. If another model file exists which is to be used for testing purposes (or another folder which is to be chosen to be classified), the following
command format should be sufficient. <br />
python classify_multiple_images.py -d path_to_folder -m path_to_model <br />
3. The program should execute and begin sorting the images into created folders. This might take some time, depending on how many images the folders contain. After the execution is over, the folders should contain the images classified according to category.