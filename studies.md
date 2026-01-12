# Self-Study Preparation

**⏳ Estimated Prep Time:** 45–60 minutes

Welcome to our flipped-classroom session, where you'll review foundational concepts beforehand to maximize our time for hands-on coding and debugging. This pre-study transitions us from traditional text processing to **Deep Learning**, the engine behind modern breakthroughs like ChatGPT, automated translation, and advanced sentiment analysis. Understanding these architectures is essential for building scalable, context-aware applications in professional environments.

## ⚡ Your Self-Study Tasks

Please complete the following activities before our session. These tasks are designed to provide the conceptual framework we will implement during the live workshop.

### 📝 Task 1: The Shift to Deep Learning

**Activity:** Read the sections **"Deep Learning for NLP"** and **"Recurrent Neural Networks (RNNs)"** in the Colab notebook ([`3.10 NLP Advanced.ipynb`](https://colab.research.google.com/drive/1io-CwOqM7Aw90_VEkvshIaP2DUx_7IpX?usp=sharing)). Focus on the limitations of traditional machine learning (like the manual feature engineering we discussed previously) and how Recurrent Neural Networks (RNNs) attempt to solve sequence problems.

**Guiding Questions:**

* **Automation:** The text notes that deep learning allows for "Automatic Feature Extraction." How does this differ from the manual feature engineering (like TF-IDF) required in traditional models?
* **The Memory Problem:** RNNs suffer from the "Vanishing Gradient Problem," making it hard to learn long-range dependencies. In a business context (e.g., analyzing long legal contracts), why would a model that "forgets" the beginning of a document be problematic?

### 📝 Task 2: Solving the Bottleneck (Attention & Transformers)

**Activity:** Review the sections on **"Attention Mechanisms"** and **"Transformer Architecture"**. Pay close attention to how the "Attention" mechanism allows a model to focus on specific parts of a sentence rather than processing everything sequentially.

**Guiding Questions:**

* **Dynamic Context:** Traditional models use a fixed-size context vector. How does the Attention mechanism alleviate this bottleneck to improve performance on tasks like machine translation?
* **Parallelization:** The Transformer architecture removes recurrence entirely. How might this impact training speed compared to processing words one by one in an RNN?

### 📝 Task 3: The Giants of NLP (BERT vs. GPT)

**Activity:** Skim the **"Understanding BERT and GPT"** section. Distinguish between these two industry-standard models based on their architecture and best-use cases.

**Guiding Questions:**

* **Context Direction:** BERT is "bidirectional" while GPT is "unidirectional." Why is BERT better suited for *understanding* a sentence (e.g., classification), while GPT is better suited for *creating* one (e.g., text generation)?
* **Application:** If you were building a customer support chatbot that needs to *answer* questions based on a manual, which model architecture (BERT-like or GPT-like) seems more relevant?

## 🙌🏻 Active Engagement Strategies

To ensure you are ready for the live coding session, try one of the following strategies:

* **The "Attention" Analogy:** Write down a long sentence. Underline a specific word at the end (e.g., "bank"). Now, circle the words earlier in the sentence that clarify if you mean a *river* bank or a *financial* bank. This is essentially how the Attention mechanism works!
* **Concept Comparison Table:** Create a quick 3-column table comparing **RNNs**, **LSTMs**, and **Transformers**. Note one "Pro" and one "Con" for each based on the reading.
* **Code Scouting:** Briefly look at the `RNNModel` class in the code cells. You do not need to run it, but identify where the `nn.RNN` layer is defined vs. where the `nn.Linear` (fully connected) layer is defined.

## 📖 Additional Reading Material

* [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) – A highly recommended visual guide to understanding the architecture we will use in class.
* [BERT vs. GPT](https://www.google.com/search?q=https://medium.com/walmartglobaltech/bert-vs-gpt-a-comparison-of-two-powerful-nlp-models-4d693526027e) – A deeper dive into when to choose which model for your workplace projects.
- [Deep Learning for NLP: History and Achievements)](https://www.exxactcorp.com/blog/Deep-Learning/deep-learning-in-natural-language-processing-history-and-achievements) - Article traces the evolution of natural language processing (NLP), highlighting its shift from rule-based systems to deep learning breakthroughs like word embeddings, attention mechanisms, and Transformer architectures

### 🙋🏻‍♂️ See you in the session!

