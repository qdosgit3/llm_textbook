
## LLM overview

LLM stands for Large Language Model. An LLM is made up of a set of functions and parameters connected together, such that outputs of functions are then used as inputs to others, that can give coherent, natural language output, after being prompted by an initial input, such as a question or instruction.

LLMs are generally developed by well-funded companies, who are able to spend large quantities of money on data and computational power to develop competitive models. Examples of LLMs include Llama-4 from Meta, ChatGPT-4 from OpenAI, or Gemini 3 from Google.

There are a few major stages within the lifetime of an LLM:
1. Development \- large quantities of data are run through the functions that make up the LLM, and the parameters are optimised so that inputs give expected output  
2. Adaptation \- deploying more specific methods to fine-tune a model for specific use-cases  
3. Utilisation \- invoking output from the trained model, for practical uses, by crafting prompts

Generally, development of a competitive LLM is outside of the budget of most companies \- DeepSeek, a Chinese competitor to OpenAI, is said to have built the LLM DeepSeek-R1 for $6M USD. However, businesses across a large variety of industries increasingly benefit from the automation abilities of the utilisation stage that LLMs offer, such as for customer service, content creation, or information retrieval purposes.

Note that LLMs are prone to acting on predictions, even if reasoning is not substantive for them, and so LLMs are regarded as experimental.

Take the following murder mystery I invented, for example:
*8 guests resided in a rented house on the night 12th July 2015 \- Margaret, Joe, James, Kyle, Carter, Judith, Janice, and Jillary. Margaret and Joe went out to dinner at 7pm, their attendance at a local restaurant confirmed by restaurant staff and a local couple, and left at 10pm. James and Kyle state that they watched an action movie in the attic of the house at 8pm, which was confirmed via their streaming account. Carter and Judith retired to their en-suite room at 9pm for the rest of the night. Janice went out for a moonlit walk along the riverside, and is confirmed to have spoken with some locals walking their dog. Jillary was found dead on the morning of 13th July 2015, killed at gunpoint. An unsilenced weapon was found by her bedside, with no fingerprints on it. No guests state that they heard a gunshot. Who was the murderer?*  

The responses from various LLMs are as follows:
* Llama-4 ruminated through a logical 12-step process then quickly blamed James, without explanation  
* ChatGPT-4 blamed Janice due an ambiguous alibi  
* ChatGPT-5 blamed Carter or Judith, but specifically Carter (allegedly due to the subtlety)  
* Gemini 2.5 Flash suspected suicide, an unexpected plot twist  
* Gemini 2.5 Pro suspected Carter and Judith due to the decibels of an unsilenced gunshot which was claimed unheard

Note that I did not have any clear perpetrator in mind at the time of writing this murder mystery, though I do have awareness of statistical differences between crime rates of different demographics (e.g. male and female).

Furthermore, once trained, LLMs are only able to retrieve data available during the training stage reliably; newer data is unreachable. For example, ask an LLM what the current UK inflation rate is:  
*The current inflation rate in the UK for August 2025 is projected to be around 4%. This figure is based on trends observed in previous months, where inflation rose to 3.6% in June 2025, up from 3.4% in May.*  
\- ChatGPT-4

This is verifiably inaccurate; as of August 2025, the Bank of England official website states the UK inflation rate to be 3.6%, \~10% less than the number provided.

However, ask Llama-4 something more general, e.g. "What are common problems among Computer Science departments (within universities)?" and we get a list of very coherent and topical responses:

* Keeping the curriculum up-to-date with rapidly evolving industry trends and technologies  
* Meeting accreditation standards and requirements  
* High student-to-faculty ratios, leading to limited individual attention and support  
* Creating a welcoming and inclusive environment for underrepresented groups  
* Encouraging collaboration between CS departments and other disciplines

This text attempts to give an overview of the theory behind how the major pieces of an LLM works, without getting too caught up in the current most popular implementation details (tensors, Python, etc.).

