DataSet Source:
https://data.mendeley.com/datasets/8h65ywd2jr/3

Preprocessing steps:
1) conversion to grayscale
2) resizing image to 256*256
3) image Normalization (divinded each pixel by 255 to bring them in range 0 -1)

Data Repartition:
Training set -> 80%
Validation set -> 20%


1)  The first problem was that we were unable to load the entire data into memory at 
    once so we had to write a custom data loader that loads only one batch of images from the hard drive

2)  After that we Split the data into training and validation set (80% training & 20% Validation)

3)  Initialize our CNN model which takes grayscale images of size 256*256 (In our data, color was not important that's why we use grayscale. 
    Benefit of using grayscale image will be that our input size will be reduced three times )

4)  Now we train our model on batches of size 64.
    While loading each batch we apply preprocessing 
    (conversion of image to grayscale, resizing images to have same size for all of them, normalization )
