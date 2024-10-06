Counterfeit IC Detection

These are steps to be followed to run the executable file:

1. Firstly load the executable.ipynb onto Google Colab's environment.
2. Run the first cell to import all necessary libraries.
3. Run the second cell to connect your drive to the Colab Notebook.
4. Now if your dataset which are images of IC, if they are in folder on the drive that are NOT zipped then give the source and destination path to copy the contents on to the Google Colab's local environment because it is easier to fetch from local rather than on drive. Use the first commented part to copy contents by uncommenting only the first part and changing the source and destination path.
5. If the contents are in a zipped folder just change the path to the zip folder in second part of the code and run the cell to unzip on to Google Colab's local environment.
6. Based on the destination path make changes in the next cell where we load images into Numpy arrays to feed it to the model.
7. In the next cell do not forget to change the location of the saved model while loading.
8. After this you can run the subsequent cells to get various outputs such as the accuracy, classification outcomes(FP, FN, TP and TN) and the confusion matrix.