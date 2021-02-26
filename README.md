# CMPE-258-HW2

Homework 2 - Deep Learning Class

AI Platform Unified Demo Part1_Part2 

Demonstrate simple hello world examples end-2-end with automl tools on google cloud AI Platform. 

Part1

[AI Platform](https://cloud.google.com/ai-platform-unified/docs/tutorials/) with your optional but important creative modifications.
Like either use different data sets or building your own data set by labelling and collecting from images.google.com or 
something else that you think you can do (or may be even taking pictures using ur mobile phone cameras), 
different target labels, different tuning configurations s to automl etc., 
I challenge the students to take on interesting twists to these hello world examples and produce results.

Five examples - one in each of below categories. 

Hello AI Platform (Unified)

•	Hello image data
  Use an image dataset to train an AutoML model.
  
  Result: 
  -Successfully Trained the AutoML Image Classification Model using different dataset (smaller dataset - Citrus Plants)
  -The dataset was created using import image and same as the labeling of images.
  -The training took only 27mins and have low accuracy of Black Spot labeled data based on the Confusion Matrix.
  -The main issue is the deployment of a model to send a prediction failed to create an endpont to send a prediction.
  
  (Refer page 9~16 for the detailed demo screenshot of this report)
 
•	Hello text data
  Use a text dataset to train an AutoML model.
  
  Result: 
  -Successfully trained the AutoML Text Classification model using smaller dataset from the sample data happiness.csv.
  -Copy the sample dataset happiness.csv to storage bucket for training sample but it took too long to train the sample.
  -Cancelled the training set instead use smaller dataset from the happiness.csv with 91samples only.
  -The training took 4Hrs and 54mins to train the smaller dataset. Predicted correctly the achievement and affection labels based on
  confusion matrix.
  -The main issue is the deployment of a model to send a prediction failed to create an endpont to send a prediction.
  
  (Refer page 17~32 for the detailed demo screenshot of this report)
  
•	Hello video data
  Use a video dataset to train an AutoML model.
  
  Result:
  -Successfully trained the AutoML Video Classification model using sample video.
  -Created the sample dataset from AutoML and import the sample video data from Cloud Storage gs://automl-video-demo-data/hmdb_split1_5classes_all.csv
  -Trained the sample for 2Hrs and 4mins. Predicted correctly all the true video label 100% ( pullup, kickball, cartwheel, ride_horse, golf) based on
  confusion matrix.
  -Successfully created a batch prediction of video model.
  -AI provides three types of information for labels
    Labels for the video - Segment tab below the video on the results page.
    Labels for shots within the video - Shot tab below the video on the results page.
    Labels for each 1-second interval within the video - 1 Second Interval tab below the video on the results page.
    If you want to see more labels, you can change the threshold score when you request a prediction. 
    AutoML video only displays the labels that are above the specified threshold.
    
   (Refer page 33~45 for the detailed demo screenshot of this report)
  
•	Hello custom training
  Learn how to bring your own code to AI Platform, by using a sample app to train an image recognition model.
  
  Result:
  -Successfully trained the AutoML Custom Image Classificaion model.
  -Trained the sample for 14mins and 36secs using the custom training pipeline and pre-built container.
  -Deployment to Endpoint failed because the GPU accelerators are not supported in the container image.
  -Enabled the Cloud Build API to deploy the function deploy classify_flowers.
   (This step is not added in tutorial documentation, instead this was caught as an error in cloud shell after running the command provided)
  -Successfully run the cloud function after enabling the Cloud Build API.
  -Successfully use a web app to send prediction requests but the predictions request predictions were mostly "error getting prediction"
   (Reason: The endpoint deployment creation failed)
   
   (Refer page 46~71 for the detailed demo screenshot of this report)
  
•	Hello structured data
  Use a structured dataset to train an AutoML model.
  
  Result:
  -Successfully trained the AutoML Tabular model.
  -Created the sample dataset from AutoML Cloud Storage gs://cloud-ml-tables-data/bank-marketing.csv.
  -Trained the sample for an hour using the target column Deposit.
  -Predicted the True label vs Predicted label (True Positive - 96%, True Negative - 48%) based from Confusion Matrix.
  -The top three Feature Importance is (1-Duration, 2-Month, 3-Contact)
  -The endpoint deployment to send a prediction was successful.
  -Send a prediction request to determine if the deposit was made or not.
   ( Prediction Result is 99%, with a result of 1 that represents a negative outcome — a deposit is not made at the bank)
   
   (Refer page 72~89 for the detailed demo screenshot of this report)
  
  Summary:
  1.Only Structured data was successful in deployment to endpoint for prediction. The rest have some issues.
  2.Video data was successful for batch prediction of video model.
  3.Custom Training successfully deploy a web app to send prediction requests but the predictions request predictions were mostly "error getting prediction".
  4.Text data use small dataset from 11K samples to 91samples still the training took almost 5HRs.
  
  



