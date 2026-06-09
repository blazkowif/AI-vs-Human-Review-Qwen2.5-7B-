# Human vs. AI Reviews Dataset

## Description
This dataset contains a collection of human-written and AI-generated product reviews, specifically designed to facilitate research into the linguistic and structural differences between human and machine-generated text.

The human-written reviews are sourced from the "Digital Music" subset of the [Amazon Reviews dataset](https://nijianmo.github.io/amazon/index.html) (Jianmo Ni, UCSD). This source material is highly valuable for this research as it contains historical reviews spanning from **May 1996 to October 2018**, guaranteeing absolute pre-LLM authenticity for the human baseline.

To create the artificial AI counterparts, the original human reviews were paraphrased using two modern Large Language Models: **Qwen 2.5-7B** and **Gemini 2.5**. This paraphrasing approach, inspired by Salminen et al. (2022), ensures that both the human and AI subsets discuss the exact same subject matter. This methodology allows for a highly controlled comparison across AI generations and provides a direct way to study the differences between human and AI writing styles.

## Data Structure
The dataset is organized into three primary columns:

| Column Name | Description |
| :--- | :--- |
| **`text_df2`** | The actual text content of the review (either the original human text or the AI-paraphrased version). |
| **`label_df2`** | A binary classification label indicating the origin of the review. <br> **`1`** = Yes, AI-generated (Qwen or Gemini). <br> **`0`** = No, human-written. |
| **`rating_df2`** | The original star rating given by the user for the music item. |

## Methodology
1. **Human Baseline:** Original reviews extracted from the historical Amazon Digital Music dataset.
2. **AI Generation:** The original human text was fed into Qwen 2.5-7B and Gemini 2.5 with instructions to paraphrase the content while maintaining the original sentiment and topic.
3. **Compilation:** The datasets were merged and labeled accordingly to allow for seamless binary classification and linguistic analysis.

## References
* Ni, J., Li, J., & McAuley, J. (2019). *Justifying Recommendations using Distantly-Labeled Reviews and Fine-Grained Aspects*. Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP).
* Salminen, J., et al. (2022). 
