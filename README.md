Inference:

To run inference you can get the model, config and vocab file here kaggle.com/models/suhaibrashid2003/xtts-v2-urdu-ft
You need to follow the following steps once you have downloaded the files
1) pip install coqui-tts
2) Locate TTS/tts/layers/xtts/tokenizers.py in site-packages
3) Replace the tokenizers.py with the tokenizers.py in the repo
4) Andddd you should be good to go i guess
5) One more thing, it doesnt perform well on very long inputs. You can write your own text splitter according to your needs to split longer inputs to shorter sentences.


Fine-tuning:

The current version is only fine-tuned for 17 epochs and the losses were still going down. Further fine-tuning can improve results.
In order to Fine-Tune, please follow this repo https://github.com/anhnh2002/XTTSv2-Finetuning-for-New-Languages
Just change the code in train_gpt_xtts.py, so that fine-tuning starts from current checkpoint rather than the base one
