# diarization_khoekhoe

Repository for a course project on the topic: **"Speaker Diarization on the data of Low-Resource Languages"**

## Notebooks Overview

- `creatingprotocol.ipynb`:  
  Takes as input ELAN-annotated files with the `.eaf` extension (the files themselves and a list of their names in a CSV) and creates a database `database.yml`.  
  The database contains links to three types of files:  
  - `.rttm` — files with annotated segments of each audio  
  - `.uem` — annotation boundaries  
  - `.lst` — list of audio filenames

- `finetuningandoptimizing.ipynb`:  
  Takes `database.yml` as input and fine-tunes the model and optimizes parameters based on the available data.  
  The code in this notebook is adapted from the tutorial:  
  https://github.com/pyannote/pyannote-audio/blob/develop/tutorials/adapting_pretrained_pipeline.ipynb

- `correlations.ipynb`:  
  Calculates correlations between DER (Diarization Error Rate) and parameters that may be significant, such as:  
  - Total speech duration in the file  
  - Spoken language  
  - Number of speakers

