# Build a Language Translation Bot using Amazon Lex
In this project, we'll be building a language translation bot using Amazon Lex.
If you want to translate a word or sentence into another language, all you have to do is type it into the chatbot - and it will output the translation.

1. Creating an empty chatbot
2. Specifying intents and slots
3. Specify Fulfilment
4. Create an IAM role
5. Create a Lambda function
6. Test the Lambda function
7. Test the chatbot

### Services Used 🛠
* Amazon Lex: Build the chatbot and define conversation flow.
* AWS Lambda: For translation.
* AWS IAM: Ensures secure access by managing user permissions.
* Amazon Translate: Used for translation of the sentence according to the input language specified.

### Estimated Time & Cost ⚙️
* This project is estimated to take about 1-2 Hours
* Cost: Free (When using the AWS Free Tier)

### Project Architecture:
<img width="1630" height="711" alt="translator_bot_arch" src="https://github.com/user-attachments/assets/af219e6b-0850-4582-b8d1-f4228d608be9" />

### Final Result:
<img width="439" height="690" alt="image" src="https://github.com/user-attachments/assets/9fae4f47-5024-45e3-9225-6198024ee1b4" />

```sh
Sample Utterances:

I want to translate
Can you help me translate
Translate for me
I want to translate in {language}
Translate in {language}
Can you translate in {language} for me

Language Slot Type:
French
Japanese
Chinese
Spanish
German
Norwegian

Lambda Role:
TranslateFullAccess
AWSLambdaBasicExecutionRole
```

### Lambda Test Event:

```JSON
{
  "sessionState": {
    "intent": {
      "name": "TranslateIntent",
      "slots": {
        "text": {
          "value": {
            "interpretedValue": "Hello",
            "originalValue": "Hello"
          }
        },
        "language": {
          "value": {
            "interpretedValue": "French",
            "originalValue": "French"
          }
        }
      }
    }
  }
}
```
