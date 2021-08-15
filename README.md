# speech-training-recorder

> A simple GUI application to help record audio dictated from given text
prompts, for use with training speech recognition or speech synthesis.

Given a text file containing prompts, this app will choose a random selection
and ordering of them, display them to be dictated by the user, and record the
dictation audio and metadata to a `.wav` file and `recorder.tsv` file
respectively. You can select a previous recording to play it back, delete it,
and/or re-record it.

![Screenshot](.github/screenshot.png)

**Requirements:**

* Python 3
* See [`requirements.txt`](requirements.txt) for required packages
* Cross platform: Windows, Linux, MacOS

## Getting Started

```
git clone https://github.com/daanzu/speech-training-recorder.git
cd speech-training-recorder
mkdir ../audio_data
pip install -r requirements.txt
python3 recorder.py -p prompts/timit.txt
```

```
usage: recorder.py [-h] [-p PROMPTS_FILENAME] [-d SAVE_DIR] [-c PROMPTS_COUNT]
                   [-l PROMPT_LEN_SOFT_MAX] [-o]

Given a text file containing prompts, this app will choose a random selection
and ordering of them, display them to be dictated by the user, and record the
dictation audio and metadata to a `.wav` file and `recorder.tsv` file
respectively.

optional arguments:
  -h, --help            show this help message and exit
  -p PROMPTS_FILENAME, --prompts_filename PROMPTS_FILENAME
                        file containing prompts to choose from
  -d SAVE_DIR, --save_dir SAVE_DIR
                        where to save .wav & recorder.tsv files (default:
                        ../audio_data)
  -c PROMPTS_COUNT, --prompts_count PROMPTS_COUNT
                        number of prompts to select and display (default: 100)
  -l PROMPT_LEN_SOFT_MAX, --prompt_len_soft_max PROMPT_LEN_SOFT_MAX
  -o, --ordered         present prompts in order, as opposed to random
                        (default: False)
```

## Customization

See `prompts/` directory for acceptable formats for prompt files: the simplest is `rainbow_passage.txt`.
