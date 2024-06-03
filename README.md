Leveraging Electric Guitar Tones and Effects to Improve Robustness in Guitar Tablature Transcription Modeling

This repository is structured into three main folders:

- **AMT-Tools**: A customized version of the Cwitkowitz AMT-Tools code ([Cwitkowitz AMT-Tools](https://github.com/cwitkowitz/amt-tools/)), including our dataset loader, for training models and saving datasets.
- **Guitar Pro Conversor**: Code to convert any pre-GP5 guitar pro files to a valid format.
- **Performance Generator**: Code to create token, MIDI, and HAM files from Guitar Pro tabs and audio from the generated JAMS files.

### Getting Started

Clone our repository and install AMT-Tools:

```bash
git clone https://github.com/robust-guitar-tabs/code
pip install -e amt-tools
```

This repository includes 16 Guitar Pro examples. For a full dataset, request access from DadaGP: [DadaGP](https://github.com/dada-bots/dadaGP).

### Models Training and Testing

The python files needed for training are in `AMT-Tools/amt-tools/amt_tools/examples/papers/` folder.

-`guitarProFx` for GuitarProFx training and GuitarSet validation

-`guitarSetFx` for GuitarSetFx training and GuitarSet validation

-`tabcnn` for original GuitarSet Training and GuitarSet validation

To run EG12SET inference with any model you must run `AMT-Tools\amt-tools\examples\inference\EgSet12_inference.py` file, updating the desired model filepath as indicated in line 83.

### Dataset Directory Structure

Each code notebook contains instructions for use. Ensure datasets are located in the `datasets` directory for AMT-Tools to run properly. By default, this directory is:

```python
DEFAULT_DATASETS_DIR = os.path.join(HOME, 'Desktop', 'Datasets')
```

You can change this in `AMT-Tools/amt-tools/amt_tools/tools/constants.py`.

### Folder Structure

Except for GuitarSet, which downloads by default and has a different structure, all datasets must have two folders:

- `audios`
- `jams`

### Performance Generation

Inside the Performance Generation folder, there's a Python notebook with code to vary the GuitarSet JAMS BPM. Point it to the correct folder for use. This was utilized before audio generation for the GuitarSetFx dataset.

### EGFXSET Notes

EGFXSET contains some errors. Edit the `egfxset_index_1.json` file and some filenames after downloading to use all 9 effects in our code.

### Issues

If issues arise, feel free to reach out to the first author.