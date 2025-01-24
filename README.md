# BTech-Project

In final_to_be_uploaded file:
   the original dataset of 1400 env activists was preprocessed and cleaned.
   Bart algorithm(fine tuned) was used on the about section of each person to extract a corpus for every individual in a given standardized     format. (stored in summarized corpus)
   Adjacency lists were created for every person to show the connections.
   the adjacency lists are stored in the module 1 branch of this project.
   Sbert was used for embedding the texts.
   When the user enters a prompt like "i want to build an aeroplane" , the gemini or chatgpt(fine tuned curie model) is used to extract the     necessary skills required to do that job or task.
   After this the novel algorithm is used to calculate who is the best fit for helping in doing the given job(matching between corpus of 
   each person and skills extracted for doing the job.
   Novel algorithm developed by us: The matching is not only done mathematically using cosine(equally imp) but semantic simalirity is also      taken into consideration by using t5 semantic matching . Both are given 60% and 40% weightage to consider the overall mathching of the       person ,including the skill in which he can help the best.
   How he can help is found out by LLM by giving llm the above findings.

  In the bart_fintune file:
    To generate the corpus for each individual in our given format we fine tuned the bart algorithm for abstractive summary generation using     manually created summaries as per our need which are present in train_data.xlsx

  In the skills_finetuning file:
    To extract necessary skills required to do the job Curie model was trained on the Environmental_Problem_Statements.jsonl data       
    which(purposely used some repeated values) which has the data of environmental problem statements and skills req to solve them. The data 
    was made by filling a public form in and env department of a public college.For better results we can use da-vinci model for base 
    instead of curie , but it is very costly
   
