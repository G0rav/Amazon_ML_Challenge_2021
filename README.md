# Note
All the Notebooks are messy right now. I'll organise them as soon as I got some time.

I've used simple bag of words model here to classify the node ids.
As of now I've only trained it for 1 epoch and it is performing really good.
Unfortunately, I was not able to participate and submit it to the actual challenge, so not able to test it on the test dataset.
But train data is infact really big around 3 Million data points. So, I splits the train data itself in 70-30 ratio in order to validate the performance of the model.

Training results are:
12755/12755 [==============================] - 5117s 401ms/step - loss: 1.8350 - accuracy: 0.6135 - val_loss: 1.3929 - val_accuracy: 0.6825

Time take to train 1 epochs is: 1:25:22.537572 hour

----
# Amazon_ML_Challenge_2021

Dataset: https://s3-ap-southeast-1.amazonaws.com/he-public-data/dataset52a7b21.zip

## Product Browse Node Classification

Amazon catalog consists of billions of products that belong to thousands of browse nodes (each browse node represents a collection of items for sale). Browse nodes are used to help customer navigate through our website and classify products to product type groups. Hence, it is important to predict the node assignment at the time of listing of the product or when the browse node information is absent.

As part of this hackathon, you will use product metadata to classify products into browse nodes. You will have access to product title, description, bullet points etc. and labels for ~3MM products to train and test your submissions. Note that there is some noise in the data - real world data looks like this!!

## Data Description

### Full Train/Test dataset details:

- Key column – PRODUCT_ID
- Input features – TITLE, DESCRIPTION, BULLET_POINTS, BRAND
- Target column – BROWSE_NODE_ID
- Train dataset size – 2,903,024
- Number of classes in Train – 9,919
- Overall Test dataset size – 110,775

### Important Note:

In case you are using pandas to read the csv train and test datasets, use escapechar = "\\" and quoting = csv.QUOTE_NONE options with read_csv to avoid errors during import.

### Evaluation Criteria

This contest uses Accuracy as the evaluation metric to measure submissions quality. Since this is a multiclass classification problem, we are interested in subset accuracy: the set of labels predicted for a sample must exactly match the corresponding set of ground truth labels.

### Submission File

For each PRODUCT_ID in the test data set, you are required to provide a browse node id prediction. The submission file should be a csv and contain a header followed by pairs of PRODUCT_ID, BROWSE_NODE_ID.
