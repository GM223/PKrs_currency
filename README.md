# PKrs_currency
Pakistan currency classification using deep learning, **The model achieved a classification accuracy of 98.5%**.

### Python Notebook for training on this dataset
The link to gist of the [PKRS_Classifier.ipynb](https://colab.research.google.com/gist/GM223/c9673150974efd4e25fbc3bebded4351/pkrs_classifier.ipynb)

The link to github [PKRS_Classifier.ipynb](https://github.com/GM223/PKrs_currency/blob/master/PKRS_Classifier.ipynb)

This code is based on code from a [fast.ai](https://github.com/fastai/fastai) MOOC that will be publicly available in Jan 2019.

### Dataset
I wanted to see how accurate a Neural Network would be at categorising images of currency. Being a resident of Pakistan i wanted to train it on the [Pakistnai Rupee](https://en.wikipedia.org/wiki/Pakistani_rupee) but a quick google search discovered that there were very little camera images of the different Pakistani notes on the internet so i created the dataset myself.

The different bank notes in the dataset are as following : 

I took the 6 images below from [this](http://www.mkhalid.com/2008/04/27/pakistani-rupee-currency-note/) blog post, images in the dataset are my own.
<p float="left">
  <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/10rupees2005jinnahpesha.jpg" width="300" />
  <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/20rupees2008muhammad_ali_jinnahmohen-jo-daro_larkana.jpg" width="300" /> 
  <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/PKR-50-note-300x300-july-9-2008.jpg" width="300" />
   <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/100rupees2005muhammad_al.jpg" width="300" />
   <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/500rupee2007muhammad_alibashahi_masjid_lahore.jpg" width="300" />
   <img src="http://www.mkhalid.com/wp-content/uploads/2008/04/1000rupeesjinnahislamia_college_peshawar.jpg" width="300" />
</p>

### Creation of Dataset
The first step was to find as many currency notes as i could, everyone in the family lent me their riches for science!
   
![img_stack](https://github.com/GM223/PKrs_currency/blob/master/others/InkedIMG_20181023_161942_LI_pile.jpg?raw=true)

I then took pictures of all the notes and divided them in train and validation set, the distribution of the dataset is as following :

| Category | Train | Valid | Total |
|:------------:|:-----:|:-----:|-------|
| ten | 101 | 44 | 145 |
| twenty | 12 | 6 | 20 |
| fifty | 15 | 7 | 22 |
| hundred | 14 | 6 | 20 |
| five_hundred | 2 | 2 | 4 |
| Thousand | 5 | 3 | 8 |
| **TOTAL** | **149** | **68** | **217** |
| **Percentage** | *68.7%* | *31.3%* | *100%* |

The data was distributed into a dataset directory structure as shown below:

![alt text](https://github.com/GM223/PKrs_currency/blob/master/others/direct_struct.PNG?raw=true)
