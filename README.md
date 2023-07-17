Some nice examples of Whisper prompts:

## Diarization

Whisper can do a crude form of speaker turn tracking (e.g. " - Hey how are you doing? - I'm doing good. How are you?", note that the token for " -" is suppressed by default and will need to be enabled manually.)

<https://github.com/openai/whisper/discussions/117#discussioncomment-3727051>

## Utterance verification

"Repeat after me: text to verify"
  
## Force UK spelling
  
"As British would say:" 
 
## Prompt vs prefix

<https://github.com/openai/whisper/discussions/117>

## Prompting the Hidden Talent of Web-Scale Speech Models for Zero-Shot Task Generalization

<https://arxiv.org/abs/2305.11095>

<https://github.com/jasonppy/PromptingWhisper>

## ASR results combination

<https://arxiv.org/abs/2306.17103>


> Task: As a GPT-4 based lyrics transcription post-processor, your task is to analyze multiple ASR model-generated versions of a song’s lyrics and determine the most accurate version closest to the true lyrics. Also filter out invalid lyrics when all predictions are nonsense.
> Input: The input is in JSON format: 
> {“prediction_1”: “line1;line2;...”, ...}
> Output: Your output must be strictly in readable JSON format without any extra text:
> {
> “reasons”: “reason1;reason2;...”,
> “closest_prediction”: <key_of_prediction>
> “output”: “line1;line2...”
> }
> Requirements: For the "reasons" field, you have to provide a reason for the choice of the "closest_prediction" field. For the "closest_prediction" field, choose the prediction key that is closest to the true lyrics. Only when all predictions greatly differ from each other or are completely nonsense or meaningless, which means that none of the predictions is valid, fill in "None" in this field. For the "output" field, you need to output the final lyrics of closest_prediction. If the "closest_prediction" field is "None", you should also output "None" in this field. The language of the input lyrics is English.

## Surveys the paper focusing on Adapters and Prompting methods for Speech Processing.

<https://github.com/ga642381/Speech-Prompts-Adapters>
