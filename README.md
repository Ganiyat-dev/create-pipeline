# setting up a circleCI pipeline process
## create a simple workflow
- config0.yml consist of simple workflow with a set of job that prints Hello and World

## adding environment variables
- config01.yml adds a job to the project's pipeline that prints a name to the console using the environment variable. 

## Create and share files between jobs in a workflow.
- config.yml consists of a simple workflow that output "hello world" to a file called output.txt
- Add a persist_to_workspace block to that job and reference output.txt so that it gets saved to the "workspace" (making it available to other jobs).
- Add another job named print_output_file.
- In this job, add a attach_workspace block (much like attaching a hard drive).
- In this job, also run a bash command that prints the contents of output.txt. For example: cat output.txt.

## Create a job that uses a reusable "command" that prints the pipelineId to the console.
- config02.yml contained a simple workflow that uses a pipeline variable instead of environment variabes

## Create a job that has an intentional failure in it with a step that runs on fail that prints "Hello Error!" to the console.
- config03.yml contains a job with step that fails on purpose by exiting with a non-zero code, and also a step that handles the error i.e when: on_fail

