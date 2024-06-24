# Hindi Accent English Speech Conversion Using Seq2Seq-VC

This repository contains the code and experimental results for converting the English accent of Hindi native speakers using Seq2Seq voice conversion (VC) methods. The project is built upon the original [seq2seq-vc](https://github.com/unilight/seq2seq-vc/tree/main/egs/l2-arctic/cascade) repository, with adaptations and additional experiments to address the accent conversion task.

## Experiments Overview

A total of four experiments are conducted to investigate different aspects of the accent conversion process. Below are the details of each experiment:

### Experiment 1: Reproduction of Original Results

- **Objective:** Reproduce the results of the original repository using English speech with an Indian accent.(SVBI from L2-Arctic dataset)
- **Dataset:** Used the source speaker SVBI in L2-ARCTIC dataset and target speaker BDL in ARCTIC dataset.

### Experiment 2: Speaker-Independent Training from Scratch

- **Objective:** Extend the method to be speaker-independent by training from scratch.
- **Dataset:** 
  - Source Data: Hindi-accented English speech from the [NISP-Dataset](https://github.com/iiscleap/NISP-Dataset/tree/master).
  - Target Data: North American English speech generated using Google TTS for the same content.
- **Method:** Trained the Seq2Seq model from scratch using the new dataset.


### Experiment 3: Speaker-Independent Training from Checkpoint

- **Objective:** Enhance performance by training from the checkpoint of Experiment 1.
- **Dataset:** Same as Experiment 2.
- **Method:** Continued training from the checkpoint obtained in Experiment 1.


### Experiment 4: Incorporating Speaker Embedding

- **Objective:** Introduce speaker embedding to further improve the model's performance.
- **Dataset:** Same as Experiment 2.
- **Method:**
  - Extracted 64-dimensional speaker embeddings using the [dvector](https://github.com/yistLin/dvector) repository.
  - Incorporated speaker embeddings into the Seq2Seq training process.


## Repository Contents

- **Code Modifications:** All modifications to the original [seq2seq-vc](https://github.com/unilight/seq2seq-vc/tree/main/egs/l2-arctic/cascade) codebase are included in this repository.
- **Checkpoints:** The checkpoints from the experiments are available for further use and research.
- **Audio Results:** Audio samples demonstrating the performance of each experiment are provided.


