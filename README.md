# virality_indexing

Scope: To index the virality of a video from YouTube.

Business Problem: To understand virality grade of a youtube video

Usability: In order to achieve the above business problem, a video will be passed through the model and value of virality grade will be predicted. Model will be said to have achieved acceptance criteria if it has less error value.

Strategy: The model is trained and tested on a mixture of Indian trending and non-trending videos of  approximately  9800 and oversampled using data synthesis (SMOTE algorithm) to maintain the weightage of each label.  
The model can be further improved by adding more country data. Each video is assigned virality grading based on its statistics by manually studying each video. Hence, there might be a chance to incorrect assumptions about the labeling and also thorough testing is mandatory. 
There will be a latency of 3-4 seconds per video.

Solution: model’s output will be the predicted value of virality grade which can be used to estimate the popularity of a video. 

Versions: version 1: Testing gave accuracy of 0.976 on test videos. It is tested by third party which gave about 80% of accuracy.

Data Quantity Required: 9800 videos data containing public stats collected for analysis

Sources: various youtube apis (video stats, comments extraction) 

List Of Algorithms used: random forest classifier 

API Endpoints: predicted value of virality grade and rank along with video id (version 1) 

QA Strategy: Testing needs to be done on known unused videos of youtube and the model is accepted if model gives at least 80% of accuracy on test data

Delivery Mechanism: (Data processing\Batch\Lambda): model will be delivered in the form of api

Phase of Development: (Completion state\iteration): Version 1: Passed in QA testing
