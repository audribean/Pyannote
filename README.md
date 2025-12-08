# Workflow for predicting annotation vs model errors

Hello! For this project (located in workflow.ipynb) I have set up a workflow for analysing speaker diarisation errors. This workflow isolates segments where annotations and model predictions disagree. The interface below then displays disagreements with the highest and lowest model confidence, alongside the flagged error type and segment duration. The user is presented with an option to select whether the model or annotation are correct, or if this is ambiguous.

As of 8 Dec, I've just now reached an interesting point that I want to continue working into! Since I'm able to get an iterable list of errors that can be sorted by model confidence, we can now collect additional features about these segments that could be useful for setting up supervised classification! I've listed these features as a checklist in workflow.ipynb, but they include overlap detection, embedding similarity, and possibly signal to noise ratio.

My goal is to build up a small sample of data with error source selections from the interface and these features to see if they could predict whether an error is from annotations or the model. Isolating annotation errors will be helpful for understanding where they come from, establishing better benchmarks, and possibly automating corrections.

### User interface prototype demo as part of workflow.ipynb:
I realise that the widget does not appear when viewing the notebook in Github, so here is a short video demo:

https://github.com/user-attachments/assets/8d81dcfe-b07a-46d8-9442-8fe0e6119e11

