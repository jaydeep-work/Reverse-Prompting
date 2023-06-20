# Reverse-Prompting
Generating prompts from images. It can help in labeling dataset for Generative models like stable diffusion. It can also be used to help creators find and mimic inspirations from the creation of other artists.


# img_2_txt Models
LLaVA
GPT-4
BLIP-2
OpenFlamingo


# MiniGPT4
[![demo](MiniGPT4.png)](https://minigpt-4.github.io)


# How usually the finetuning of LLaVA happens?
1. Pretraining (2 hours)
2. Extract projector features
3. Visual instruction tuning (1 hour)

*authors have directly provided projector features. So we can directly jump to Visual instruction tuning…

# Data Source
[https://www.kaggle.com/datasets/ldmtwo/midjourney-250k-csv](https://www.kaggle.com/datasets/ldmtwo/midjourney-250k-csv)

# Data Formats

[detail_23k.json](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K/raw/main/detail_23k.json)

```json
{
    "id": "000000442786",
    "image": "000000442786.jpg",
    "conversations": [
      {
        "from": "human",
        "value": "What do you see happening in this image?\n<image>"
      },
      {
        "from": "gpt",
        "value": "The scene depicts a lively plaza area with several people walking and enjoying their time. A man is standing in the plaza with his legs crossed, holding a kite in his hand. The kite has multiple sections attached to it, spread out in various directions as if ready for flight.\n\nNumerous people are scattered throughout the plaza, walking and interacting with others. Some of these individuals are carrying handbags, and others have backpacks. The image captures the casual, social atmosphere of a bustling plaza on a nice day."
      }
    ]
}
```

[conversation_58k.json](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K/raw/main/conversation_58k.json)
```json
{
    "id": "000000033471",
    "image": "000000033471.jpg",
    "conversations": [
      {
        "from": "human",
        "value": "What are the colors of the bus in the image?\n<image>"
      },
      {
        "from": "gpt",
        "value": "The bus in the image is white and red."
      },
      {
        "from": "human",
        "value": "What feature can be seen on the back of the bus?"
      },
      {
        "from": "gpt",
        "value": "The back of the bus features an advertisement."
      },
      {
        "from": "human",
        "value": "Is the bus driving down the street or pulled off to the side?"
      },
      {
        "from": "gpt",
        "value": "The bus is driving down the street, which is crowded with people and other vehicles."
      }
    ]
  }
```

[complex_reasoning_77k.json](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K/raw/main/complex_reasoning_77k.json)
```json
{
    "id": "000000215677",
    "image": "000000215677.jpg",
    "conversations": [
      {
        "from": "human",
        "value": "<image>\nWhat skill set might someone need to perform such a frisbee trick?"
      },
      {
        "from": "gpt",
        "value": "To perform the frisbee trick shown in the image, where the man is passing a frisbee between or underneath his legs, a person would need a combination of skills. These skills include good hand-eye coordination, agility, balance, flexibility, and dexterity. Additionally, the ability to throw and catch the frisbee accurately while maintaining control of bodily movements would also be essential. To perfect the trick, practicing these skills and building up muscle memory through repetition would be beneficial."
      }
    ]
  }
```
