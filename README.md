# EaST-MELD: Emotion-aware Speech Translation Multimodal EmotionLines Dataset
EaST-MELD is an English-Japanese dataset for emotion-aware speech translation based on [MELD](リンク).
EaST-MELD has the following features:
	- Based on subtitles and speech from TV dramas.
	- EaST-MELD has text/speech in both English and Japanese and two types of emotion labels (Emotion/Sentiment) annotated for each utterance.
	- EaST-MELD has an emotion-aware evaluation set (dev/test)

- - - -
## Examples:

|Emotion|Sentiment|English|Japanese|
|——|——|——|——|
|surprise|negative|This sounds like a hernia. You have to―you―you go to the doctor!|ヘルニアだな医者へ|
|fear|negative|No way! ‘Kay look, if I have to go to the doctor for anything it’s gonna be for this thing sticking out of my Stomach!|行くもんかこの何かが腹から出てくるまではな|
|disgust|negative|That’s a hernia.|脱腸だって|
|anger|negative|Why did I have to start working out again? Damn you 15s!|運動して失敗した ダンベルのバカ!|

- - - -
## Splits:
| |# of utterances|
|——|——|
|Train|9,422|
|Dev|418|
|Test|418|

### Detail:
	- train, dev_subtitle, test_subtitle: Subtitles is used as Japanese translation.
	- dev_transcription, test_transcription: Speech transcription is used as Japanese translation.
- - - -
### csv files structure: 
`id, dialogue_id, utterance_id, Emotion, Sentiment, Text(En), Text(Ja), Season, Episode, Speaker, Starttime(En), Endtime(En), Starttime(Ja), Endtime(Ja)`
	- csv data includes utterances that do not have a corresponding Japanese translation.
### yaml files structure:
`dialogue_id, Utterance_id, Emotion, Sentiment, Speaker, wav: the name of wav files (En-Jaで名前は共通)`
	- yaml data does not include utterances that do not have a corresponding Japanese translation.
### .en/.ja files:
	- text only
	- The lines in the yaml file and the .en/.ja files are mapped to each other.
- - - -
## Note:
Please, note that by downloading the dataset, you agree to the following conditions:
	* Do not re-distribute the dataset without our permission.
	* The dataset can only be used for research purposes. Any other use is explicitly prohibited.
- - - -
## Download the wav files:
If you are interested in the speech data of EaST-MELD, please contact  [yahata@nlp.ist.i.kyoto-u.ac.jp](mailto:liyh@nlp.ist.i.kyoto-u.ac.jp) .
- - - -
## Citation:
```
S. Zahiri and J. D. Choi. Emotion Detection on TV Show Transcripts with Sequence-based Convolutional Neural Networks. In The AAAI Workshop on Affective Content Analysis, AFFCON’18, 2018.

S. Poria, D. Hazarika, N. Majumder, G. Naik, E. Cambria, R. Mihalcea. MELD: A Multimodal Multi-Party Dataset for Emotion Recognition in Conversation. ACL 2019.
```

