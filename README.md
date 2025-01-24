# BTech-Project


### Final_to_be_uploaded File:
- The original dataset of 1400 environmental activists was preprocessed and cleaned.
- **Bart Algorithm (fine-tuned)** was used on the about section of each person to extract a corpus for every individual in a given standardized format. *(Stored in summarized corpus)*.
- Adjacency lists were created for every person to show the connections.
  - The adjacency lists are stored in the **module 1** branch of this project.
- **Sbert** was used for embedding the texts.
-  When the user enters a prompt like "i want to build an aeroplane" , the gemini or chatgpt(fine tuned curie model) is used to extract the     necessary skills required to do that job or task.
- After this, the novel algorithm is used to calculate who is the best fit for helping in doing the given job. *(Matching between the corpus of each person and the skills extracted for doing the job)*.
- **Novel Algorithm Developed by Us**:
  - The matching is not only done mathematically using cosine similarity (equally important) but also semantic similarity is taken into consideration by using **T5 semantic matching**.
  - Both are given **60% and 40% weightage** to consider the overall matching of the person, including the skill in which they can help the best.
  - How the person can help is found out by the LLM by providing the above findings to the model.

---

### Bart_Finetune File:
- To generate the corpus for each individual in our given format, we fine-tuned the **Bart algorithm** for abstractive summary generation using manually created summaries as per our need. *(These are present in train_data.xlsx)*.

---

### Skills_Finetuning File:
- To extract necessary skills required to do the job, the **Curie model** was trained on the `Environmental_Problem_Statements.jsonl` data.
  - *(Purposely used some repeated values)*.
  - This dataset contains environmental problem statements and the skills required to solve them.
  - The data was created by filling a public form in the environmental department of a public college.
- For better results, we can use the **DaVinci model** as the base instead of Curie, but it is very costly.

   
