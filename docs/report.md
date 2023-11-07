# Table of Contents
* Abstract
* [Introduction](#1-introduction)
* [Related Work](#2-related-work)
* [Technical Approach](#3-technical-approach)
* [Evaluation and Results](#4-evaluation-and-results)
* [Discussion and Conclusions](#5-discussion-and-conclusions)
* [References](#6-references)

# Abstract

Provide a brief overview of the project objhectives, approach, and results.

# 1. Introduction



### Motivation & Objective:
In an era where information is abundant, the ability to understand, process, and communicate in natural language is a valuable asset. Large Language Models (LLMs) are designed to bridge the gap between human communication and machine understanding. The primary goal is to create a tool that can interpret and generate human-like text, providing assistance, simplification, and augmentation of our daily informational and communicational tasks. Essentially, we are trying to teach machines the art of human conversation and written communication.

### State of the Art & Its Limitations:
Currently, Large Language Models are at the forefront of artificial intelligence research. Models like GPT (Generative Pre-trained Transformer) have shown capabilities in generating coherent and contextually relevant text based on the input they are given. However, they are not without their limitations. These models often require vast amounts of data to train, can sometimes generate biased or incorrect information, and lack a deep understanding of the nuances and complexities inherent in human languages.

### Novelty & Rationale:
Our approach involves in deploying existing LLMs on different devices to look at the bottleneck and perforamce on various platforms and systems. We selected several state-of-the-art LLM models which are extremely popular these days, both in research and industry. For example, Llamma-2 from Meta AI, LoRA/QLoRA. Additionally, we plan to choose various deployment platforms ranging from cloud, personal edge devices, computing server, etc. This could help us to understand the capacity of LLMs in current computing platforms and areas.

### Potential Impact:
The successful development of an improved LLM has the potential to revolutionize numerous fields. From automating customer service to aiding in creative writing, the applications are vast. Technically, it would signify a leap towards more nuanced AI communication. Broadly, it could enhance education, accessibility, and information dissemination, breaking down language barriers and making knowledge more readily available.

### Challenges:
One of the greatest challenges is ensuring that the model can discern context and handle the subtleties of human language without perpetuating biases or misinformation. The complexity of language means that even small errors can significantly alter the meaning of the generated text. Additionally, the ethical use and potential misuse of LLMs pose a risk that must be carefully managed.

### Requirements for Success:
To undertake this project, a team with expertise in machine learning, natural language processing, and ethics in AI is essential. Access to large datasets, powerful computational resources, and a framework for ongoing evaluation against ethical standards are also necessary components for success.

### Metrics of Success:
Success will be measured by the model's ability to generate accurate, relevant, and unbiased text across a range of topics and styles. Performance metrics will include the quality and coherence of text, the ability to understand and generate responses to nuanced queries, and feedback from users on its reliability and usefulness. Additionally, adherence to ethical guidelines and the responsible use of the technology will be a crucial metric.

* Motivation & Objective: What are you trying to do and why? (plain English without jargon)
* State of the Art & Its Limitations: How is it done today, and what are the limits of current practice?
* Novelty & Rationale: What is new in your approach and why do you think it will be successful?
* Potential Impact: If the project is successful, what difference will it make, both technically and broadly?
* Challenges: What are the challenges and risks?
* Requirements for Success: What skills and resources are necessary to perform the project?
* Metrics of Success: What are metrics by which you would check for success?

# 2. Related Work

We did a survey and literrature review about the current and past LLMs.

## GPT-3 Family Associated with GPT-4
Generative Pre-trained Transformers, or GPTs, represent a series of evolutionary steps in the domain of natural language processing and machine learning. Developed by OpenAI, these models have set new benchmarks in the field of AI with their ability to understand and generate human-like text.

GPT-3:
Introduced in June 2020, GPT-3 (the third generation of the GPT series) astounded the tech world with its 175 billion machine learning parameters. This vast network of parameters allows GPT-3 to engage in tasks such as translation, question-answering, and content creation with remarkable fluency and minimal task-specific training. Its critical technique lies in unsupervised learning from a diverse and extensive corpus of text which enables it to generate contextually rich and varied responses. Evaluation of GPT-3's capabilities has been predominantly qualitative, focusing on its linguistic versatility and the breadth of applications it can adapt to, though quantitative measures such as perplexity scores also showcase its efficiency.

GPT-3.5:
GPT-3.5 serves as an intermediary iteration, an update to GPT-3, fine-tuned and optimized based on user feedback and ongoing research. It is not a full-fledged successor to GPT-3 but rather an enhancement that addresses some of the limitations found in GPT-3, particularly in consistency and factual accuracy. The critical technique employed remains largely the same, with improvements in fine-tuning processes and possibly the inclusion of more data to address gaps identified in GPT-3. Evaluations continue to focus on both qualitative and quantitative aspects, with increased attention to the model's ability to remain coherent over longer conversations and to better handle nuanced instructions.

GPT-4:
GPT-4, as the successor to GPT-3, is anticipated to be a more advanced version that not only increases the parameter count but also introduces new techniques for training efficiency and output quality. While details are speculative until its release, it is expected that GPT-4 will make strides in addressing issues of bias, ethical use, and misinformation. The critical techniques might involve more sophisticated training algorithms, better contextual understanding, and refined interaction patterns. Evaluation will likely encompass a wide array of benchmarks including ethical alignment, multi-modal abilities (should it support more than text), and the efficiency of learning from fewer examples (few-shot learning).

Each of these models represents a leap forward in the capacity of machines to interact with human language, both in understanding and generation. The evolution from GPT-3 to GPT-4 illustrates a trajectory of AI becoming more integrated into daily tasks, emphasizing the need for rigorous evaluation and responsible deployment. The overarching aim of these models is to serve as a versatile and reliable interface between humans and computers, enhancing our ability to communicate with and through technology.

## Llamma-2 Family
Llama-2, standing as a speculative successor to a hypothetical Llama-1 language model, would embody the next step in natural language processing and AI-driven linguistic tasks. This model, in the realm of machine learning, would likely aim to eclipse its predecessor in understanding and generating human-like text with higher precision and broader contextual awareness.

Critical Technique:
Assuming advancements along the lines of its contemporaries, Llama-2's critical technique would probably involve a combination of unsupervised and supervised learning, likely harnessing a transformer-based architecture renowned for its effectiveness in handling sequential data. The model would plausibly incorporate larger datasets, more refined parameter tuning, and potentially innovative approaches to reduce bias and improve the model's ability to grasp nuanced text. Advances in few-shot learning, where the model generates accurate responses with minimal input, could also be a focus, alongside multi-modal capabilities that integrate text with other data types like images or sounds.

## Fine-tuning LLMs Family
LoRA, which stands for Low-Rank Adaptation, is an innovative technique designed to enhance the capabilities of large pre-trained language models such as GPT-3. Developed with the intent to fine-tune these vast models more efficiently, LoRA focuses on the adaptability of neural networks without the need for significant architectural changes or the extensive computational cost typically associated with training large-scale AI models.

Critical Technique:

The critical technique behind LoRA lies in its novel approach to model tuning. Instead of updating the entire weight matrix within the transformer layers of a model, LoRA strategically targets specific parts of the weights for low-rank updates. By doing this, it can maintain the original model's performance while enabling new capabilities or knowledge to be added with minimal updates. This approach reduces the number of trainable parameters significantly, which in turn lowers the computational cost and resources required for fine-tuning.

LoRA's method allows the model to retain its original "knowledge" learned during pre-training while also acquiring new information during the fine-tuning process. This is particularly useful when adapting a model to a specialized domain or function without retraining it from scratch on large datasets.

Evaluation:

Evaluating the effectiveness of LoRA involves assessing both the performance of the adapted model on targeted tasks and the efficiency gains it provides. Performance metrics would typically include standard benchmarks relevant to the specific tasks for which the model has been fine-tuned, such as accuracy, F1 score, or BLEU score for language translation tasks. Efficiency metrics would compare the computational resources and time required for fine-tuning with LoRA against traditional full-model fine-tuning techniques.

Furthermore, evaluation of LoRA also includes how well the adapted model can transfer its learning to other related tasks without additional training—this assesses the model's generalization capabilities. The ability to maintain baseline performance on tasks for which the model was not specifically fine-tuned is also a critical part of LoRA's evaluation.

In summary, LoRA represents a significant advancement in the fine-tuning of large-scale language models, providing a pathway to model customization that balances performance with resource efficiency.

# 3. Technical Approach

## Deployment Environment

## Model Selection

## Task Definition

# 4. Evaluation and Results

# 5. Discussion and Conclusions

# 6. References