# Challenge: Generate img2vid using GenAI only!

To generate a video from images using GenAI, we must first set up and Devika IDE for the TAMI server and then fix it to generate the code for the img2vid task.

Tech specs:

Find the Tesla-P40 spec on the TAMI server using the following command:

```bash
nvidia-smi
```

Steps:

1. Install and set up Devika on TAMI computer with llama

2. How does Devika work under the hood? 
 - Is it using the same LLM thread or is it different for each iteration? 
 - How does it generate the plan?

- Fix : the bug that saves the file names wraped with `` !!!
- Add logs to all files 