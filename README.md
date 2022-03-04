# BirdClef-2022-Kaggle-comp

https://www.kaggle.com/c/birdclef-2022/overview

The challenge in this competition is to identify which birds are calling in long recordings given quite limited training data. This is the exact challenge faced by scientists trying to monitor rare birds in Hawaii. For example, there are only a few thousand individual Nene geese left in the world, which makes it difficult to acquire recordings of their calls.

This competition uses a hidden test. When your submitted notebook is scored, the actual test data (including a sample submission) will be availabe to your notebook.

Files
- train_metadata.csv - A wide range of metadata is provided for the training data. The most directly relevant fields are:

  - primary_label - a code for the bird species. You can review detailed information about the bird codes by appending the code to https://ebird.org/species/, such as https://ebird.org/species/amecro for the American Crow.
  - secondary_labels: Background species as annotated by the recordist. An empty list does not mean that no background birds are audible.
  - author - the eBird user who provided the recording.
  - filename: the associated audio file.
  - rating: Float value between 0.0 and 5.0 as an indicator of the quality rating on Xeno-canto and the number of background species, where 5.0 is the highest and 1.0 is the lowest. 0.0 means that this recording has no user rating yet.
- train_audio/ - The bulk of the training data consists of short recordings of individual bird calls generously uploaded by users of xenocanto.org. These files have been downsampled to 32 kHz where applicable to match the test set audio and converted to the ogg format.

- test_soundscapes/ - When you submit a notebook, the test_soundscapes directory will be populated with approximately 5,500 recordings to be used for scoring. These are each within a few milliseconds of 1 minute long and in the ogg audio format. Only one soundscape is available for download.

- test.csv - Metadata for the test set. Only the first three rows are available for download; the full test.csv is provided in the hidden test set.

  -row_id - A unique identifier for the row.
  -file_id - A unique identifier for the audio file.
  -bird - The ebird code for the row. There is one row for each of the scored species per 5 second window per audio file.
  -end_time - The last second of the 5 second time window (5, 10, 15, etc).
- sample_submission.csv - A valid sample submission. Only the first three rows are available for download; the full submission.csv is provided in the hidden test set.

row_id - A unique identifier for the row.
target - True/False for whether or not the bird in question called during the 5 second window.
scored_birds.json - The subset of the species in the dataset that are scored.

eBird_Taxonomy_v2021.csv - Data on the relationships between different species.

![alt text](/newplot.png)
