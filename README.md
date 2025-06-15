# Assignment3

**2. Short Answer Questions:**
**What is the difference between stemming and lemmatization? Provide examples with the word “running.”**
 
    Stemming: Heuristically removes word endings to reduce to a base/root form. Less accurate; may produce non-words.
  	example : running" → "run", "flies" → "fli"

    Lemmatization: Uses vocabulary and morphological analysis to return the base or dictionary form (lemma). More accurate; produces valid words.
    example : "running" → "run", "flies" → "fly"

  	
**Why might removing stop words be useful in some NLP tasks, and when might it actually be harmful?**

    Removing stop words is beneficial in tasks where common words do not add meaningful information and could introduce noise.
  	Examples:
    Text Classification / Topic Modeling:
    Words like “the”, “is”, “and” appear in all documents → don’t help differentiate topics.

    Search Engines:
    Improves performance by indexing only informative keywords.
    Example: In a dataset about sports, “game”, “team”, “score” are more important than “the” or “was”.

    
**3. Short Answer Questions:**
**How does NER differ from POS tagging in NLP?**

    Named Entity Recognition (NER) and Part-of-Speech (POS) tagging are both important tasks in Natural Language Processing, 
    but they serve different purposes. NER focuses on identifying and classifying real-world entities in text—such as people, 
    organizations, locations, dates, and monetary values. For example, in the sentence "Barack Obama was born in Hawaii in 1961",
    NER would label "Barack Obama" as a PERSON, "Hawaii" as a GPE (Geo-Political Entity), and "1961" as a DATE. In contrast, 
    POS tagging labels each word based on its grammatical role in the sentence. In the same sentence, POS tagging would mark "Barack"
    as a proper noun (NNP), "was" as a past tense verb (VBD), and "born" as a past participle verb (VBN). While NER is about recognizing 
    meaningful real-world entities, POS tagging is about understanding sentence structure and syntax.

 **Describe two applications that use NER in the real world (e.g., financial news, search engines).**

    One major real-world application of NER is in financial news analysis, where it is used to extract names of companies, stock symbols, 
    economic indicators, and dates from news articles to assist in automated trading or market trend analysis. For instance, if an article 
    mentions "Apple Inc. reported a 10% rise in Q1 revenue", NER helps detect "Apple Inc." as an ORGANIZATION and "Q1" as a DATE. Another 
    application is in search engines, where NER helps interpret user queries more accurately. For example, in the query "weather in Paris next 
    Monday", NER identifies "Paris" as a LOCATION and "next Monday" as a DATE, enabling the system to retrieve more relevant and contextual results.

    
 **4. Short Answer Questions:**
 **Why do we divide the attention score by √d in the scaled dot-product attention formula?**
  
    In scaled dot-product attention, the dot product of the query and key vectors can become very large when the dimensionality 
    d is high. These large values can push the softmax function into regions where it has extremely small gradients, making learning unstable. 
    Dividing by 𝑑 (the square root of the key dimension) scales down the dot products to prevent this. This keeps the softmax output more balanced, 
    ensuring better gradient flow during training and more stable attention distributions.

**How does self-attention help the model understand relationships between words in a sentence?**
    
    Self-attention allows a model to compare each word in a sentence with every other word and assign different levels of importance to them. 
    This helps the model capture context and dependencies, regardless of the distance between words. For example, in the sentence "The cat that 
    chased the mouse was fast," self-attention helps link the word "was" to "cat" (not "mouse") by assigning higher attention weights to related 
    words. This enables the model to understand the true meaning of sentences, manage long-range dependencies, and disambiguate word roles in context.


    
 **Short Answer Questions:**
 ** What is the main architectural difference between BERT and GPT? Which uses an encoder and which uses a decoder?**
      
       The main architectural difference between BERT and GPT lies in their Transformer components. BERT uses only the Transformer encoder, 
       which processes the entire input bidirectionally — meaning it looks at both the left and right context of each word. This makes BERT 
       ideal for tasks like classification, question answering, and token-level predictions. On the other hand, GPT uses only the Transformer 
       decoder, which is autoregressive and processes text left-to-right — generating one token at a time based on previous tokens. This make
       GPT more suitable for text generation tasks like summarization, translation, and chatbot responses.
  **Explain why using pre-trained models (like BERT or GPT) is beneficial for NLP applications instead of training from scratch.**

      Using pre-trained models like BERT or GPT is highly beneficial because they are already trained on massive text corpora and have learned 
      a deep understanding of language patterns, grammar, and semantics. This allows developers to fine-tune these models on specific tasks 
      (like sentiment analysis, named entity recognition, or summarization) with relatively little data and computing power. Training from scratch 
      would require huge datasets, enormous computational resources, and time — which is often impractical. Pre-trained models enable faster development, 
      better accuracy, and more efficient use of resources in real-world NLP applications.
