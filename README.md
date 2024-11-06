# kai-chatbot-microsoft-copilot-studio

## Introduction
This is a chatbot project created using Microsoft Copilot Studio. There are two chatbot demo files included in this project. 

kai-chatbot-need-identify-document.yaml is a chatbot that have 2 steps to answer the question. The first step is to identify the correct question, and once the correct question is identified, the chatbot will send the correct question to kai studio to get the answer.

kai-chatbot-search.yaml is a chatbot that has 1 step to answer the question. The chatbot will send the question to kai studio to get the answer.

## How to use
1. Clone the repository to your local machine.
2. Open the bot file you want, in this case, kai-chatbot-need-identify-document.yaml or kai-chatbot-search.yaml.
3. Add your trigger word list.
```yaml
    triggerQueries:
      - your trigger word list 
      - your trigger word list
```
if you want to trigger the chatbot with any word, just write
```yaml
    triggerQueries:
      - *
```
4. Add your api key, instance id, and two search parameters to the bot file.
```yaml
    - kind: SetVariable
      id: setVariable_iNJfrn
      variable: Topic.apiKey
      value: your api key like 9087VBNBFIOIIUIY3Eftj+IFEBZUIVIE987=

    - kind: SetVariable
      id: setVariable_DoE36i
      variable: Topic.instanceId
      value: your instance id like vov987-p909-nvje98-vfqv-908bn987kjhg
      
    - kind: SetVariable
      id: setVariable_ATGC3W
      variable: Topic.multiDocuments
      value: true

    - kind: SetVariable
      id: setVariable_gOtsgD
      variable: Topic.needFollowingQuestions
      value: true
```

5. Open your Microsoft Copilot Studio.
6. Create new agent. Need to pay attention, you need to pick your language when creating new agent, after creating, you can't change it.
7. Create new theme
8. Click More, then click Code editor, then copy the code in kai-chatbot-need-identify-document.yaml or kai-chatbot-search.yaml to the code editor.
9. Click Save

Then you can try your chatbot or publish your chatbot.