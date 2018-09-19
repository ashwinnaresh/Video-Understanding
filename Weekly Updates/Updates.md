# Video Understanding - Weekly Updates

This document contains the weekly updates on the video understanding project for the MIIS Capstone requirement.

## Work done since the final presentation in May

An initial topic analysis of the videos in the How-To dataset was done using the video transcriptions. The dominant topics of the videos were Health, Yoga, Cooking, Stitching to name a few. 

## 09/05 - 09/12

Member | Upcoming Tasks 
------ | ---------------
Arvind | Get similar dissimilar videos clustered:<ul><li>Analyze topic distribution</li><li>Get similar videos based on empirical threshold</li><li>Reduce the empirical threshold to get dissimilar videos</li></ul>
Ashwin | Get summarization baselines up and running:<ul><li>Setup environment</li><li>OpenNMT baseline for summarizing videos based on transcription</li><li>Stretch goal: Experiment with action features along with text for summarization</li></ul>
Madhura | Time alignment of transcriptions of video pairs:<ul><li>Literature survey</li><li>Implementation of simple techniques like n-gram overlap, LCS</li><li>Stretch goal : DTW</li></ul>

## 09/12 - 09/19

Member | Status | Upcoming Tasks
------ | ------- | ----------------
Arvind | Get similar dissimilar videos clustered:<ul><li>Analyze topic distribution - Checked a 50 topic LDA distribution. The topics seem to be well formed but the choice of the number of latent topics is yet to be confirmed.</li><li>Get similar videos based on empirical threshold - Identified yoga as one of the "hot topics". Evaluated DBSCAN, HDBSCAN, K-means and KNN based on intrinsic measures.</li><li>Reduce the empirical threshold to get dissimilar videos - Basic tests based on KNNs. Threshold setting still an open question</li></ul> | <ul><li>Setup extrinsic evaluation of LDA topics</li><li>Setup extrinsic evaluation of the similar and dissimilar clusters</li><li>Tune the clustering, choice of k in kNN and number of topics based ib the extrinsic evaluation</li></ul>
Ashwin | Get summarization baselines up and running:<ul><li>Setup environment - Environment setup on Rocks cluster</li><li>OpenNMT baseline for summarizing a video based on transcription - Model has been trained. It needs to be evaluated with ROUGE.</li><li>Stretch goal: Experiment with action features along with text for summarization - Not started</li></ul> | <ul><li>Evaluate the trained model on ROUGE and content F1 score metrics</li><li>Experiment with action features along with text for summarization</li></ul>
Madhura | Time alignment of transcriptions of video pairs:<ul><li>Literature survey - Surveyed multiple methods for aligning text in documents</li><li>Implementation of simple techniques like n-gram overlap, LCS - Used other techniques like Rogue and Edit Distance from Survey</li><li>Stretch goal : DTW - Might not be relevant for our use case</li></ul> | <ul><li>Currently experimenting with multiple similiarity scores</li><li>Will have to evaluated the techniques on multiple pairs of videos from different domains to choose the most robust method on identifiying differences</li></ul>

## 09/19 - 09/26

Member | Status | Upcoming Tasks
------ | ------- | ----------------
Arvind | <ul><li>Setup extrinsic evaluation of LDA topics - Primary evaluation based on the kNN for videos (subjective)</li><li>Setup extrinsic evaluation of the similar and dissimilar clusters - Subjective evaluation completed. Extrinsic evaluation will be possible after a few downstream tasks are defined</li><li>Tune the clustering, choice of k in kNN and number of topics based on the extrinsic evaluation - Implemented a re-ranking metric for kNN based on content similarity in the retrieved neighbours</li></ul> | <ul><li>Try content F1 score and other content similarity measures (METEOR/ ROUGE) to get better distinction between similar and dissimilar videos</li><li>Identify main sets of topics to focus on for initial evaluation</li><li>Improve the interpretibility of the different techniques by juxtaposing the results appropriately.</li><li>Stretch goals: <ul><li>Design model for difference generation</li></li></ul>
Ashwin | <li>Evaluate the trained model on ROUGE and content F1 score metrics - Model evaluated on BLEU-4 (30.797), ROUGE-L (50.3) and METEOR (25.21) scores</li><li>Summarization model trained with video action features and text which gave scores of </li></ul> | <ul><li>Figure out how to compute content F1 score</li><li>Visualize the attention of the summarization model</li><li>Design model architecture for difference generation</li><li>Stretch goals: <ul><li>Implement model and train for difference generation (on dummy data atleast)</li><li>Experiment with object and scene features for summarization</li></ul></li></ul>
Madhura | Time alignment of transcriptions of video pairs:<ul><li> Implemented a time alignment methodology to align transcriptions with respect to a similarity score</li><li>Evaluated techniques on multiple similarity scores</li></ul> | <ul><li>Implement the Viterbi algortihm to align sentences and use a similairy metric in between to decide insertions and deletions</li><li>Create a grah based to structure to better visualize the sentences which are similar for the videos</li></ul>
