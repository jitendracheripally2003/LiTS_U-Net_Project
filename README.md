# Liver Tumour Segmentation using U-Net
LiTS_project notebook file contains the implementation of the already converted images of the CT scans. It has been finetuned and exhibited for this project, it has hiigher accuracy and evaluation metrics like IoU, Dice Coefficient and loss.
The total explanation of the above mentioned implementation is given in the project report PDF file. It has the detailed information about the project from data preprocessing to model evaluation. Refer both the notebook and also PDF file for better understanding.
Data used for this project is image dataset extracted from the CT scans, which have gone through so much of conversions. Images are extracted using FastAI code for medical imagaing, but it has a small issue which turned into a very effective factor. The dataset contains images and masks, which are categorized into 3: Empty without liver and tumour, contains only liver and with liver and tumour. We care about only data with liver and tumour for the model training, but for that seperation which we cant do maunally had to be automated and reliable. The empty masks are easily identifed and deleted but the main issue is that masks containing only liver, has liver in dark blue* color and in masks with liver and tumour liver is light blue* and tumour dark blue* which will be not helpful for segmentation because for adding some noise in training we considering all the masks with liver and tumour, but also some empty and only liver masks. So it has to be reversed to make the process possible, using some opencv techniques it has been done.
Here is the [link](https://www.kaggle.com/datasets/jitendracheripally/liver-tumour-dataset-with-model) for the dataset, it also contians the model hdf5 file, which can be used to used to get the nearly same results we got.
  *color can change according to the package we use

liver-tumour-segmentation-on-lits17 notebook contains the implementaion of the CT scans. Though the whole methodology of the both implementaion is same but the models have to be finetuned differently. This shows us the supremacy of the data we use for the model building, which effects all the other factors.
The data used for this implementaion is the direct dataset from Kaggle, the links for those can be find in the dataset section of the notebook file.
The problem we have faced with the previous implementation is not encountered here, because we are using the images converted on the fly.

I hope this project has many suboptimal or non optimal things, please suggest them in the issues section. Thank you for reading and considering our project.

This project is made in collaboration of [Meghana Arisela](https://github.com/MeghanaArisela) and [Jitendra Cheripally](https://github.com/jitendracheripally2003).
