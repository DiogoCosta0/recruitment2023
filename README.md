# Recruitment Task 2023

## Module 1 - Implementing and training a neural network

### Procedure

To solve this task, do the following:
- Fork this repository on you personal GitHub account;
- Open a draft pull request to this repository's "main" branch;
  - Run the code snippets in `mod1/notebook.ipynb` and answer the questions made there.
- When you're done, mark the pull request as ready for review and notify the department leader (until 15 october);
- Your work will be reviewed directly on the pull request until 18 october.

### Requirements

- Python
    - PyTorch
    - TorchVision
    - TensorBoard

Use the Jupyter Notebook to explore and solve this task. You can use Jupyter Notebooks using Jupyter, PyCharm or a VS Code plugin.

## Module 2 - Integration with C

The software of an autonomous car is composed of many components, which require integration. 

The goal of this second task is to integrate the work you developed previously with a C program. 

### Functional requirements

- First, change the script notebook code to save the trained model after training.
  - https://pytorch.org/tutorials/beginner/basics/saveloadrun_tutorial.html
- Create a new Python script which:
  - Loads the saved model;
  - Connect to the named pipe created by the C program;
  - Run inference on a random dataset image;
  - Send the inference result to the C process.
- Create a C program which:
  - Creates a named pipe;
  - Accepts the Python pipe connection;
  - Waits for data (the class prediction);
  - Prints the results on the console.

### Recommended environment
- To solve this task, you should use some Linux distribution. Feel free to install a virtual machine. This is for the 
following reasons:
  - Programming involving inter-process communication is simpler on UNIX, is properly implemented and has proper documentation;
  - All the car software runs on Linux. Considering this, we usually work on Linux to work in an environment closer to
  deployment to avoid integration issues.

### Reading list

- Relevant Linux manual pages (e.g.: "`man pipe`, `man read`, `man write`)
- Python Documentation: https://docs.python.org/3/library/multiprocessing.html#pipes-and-queues