# PHP-AutoGpt

PHP-AutoGpt is a simple class implementation designed to showcase capabilities of LLMs in tasks creation and automation. The class generates initial tasks based on the objective, executes those tasks, generates new tasks based on the results, and reprioritizes tasks based on the most recent task completed.

## Usage

First, you will need an API key. You can obtain one from your OpenAI. Once you have your key, include it when constructing the class.

```php
$agent = new Pport\AutoGpt();
$agent->setApiKey('OPENAI_KEY');
$agent->setObjective("Create A Blog Post bout Artificial Intelligence");
$agent->setInitialTask("Research the best ideas");
$agent->run();
```

The run() method will loop through each task until the objective is reached. It will automatically generate new tasks based on the results of the previous task and prioritize the tasks accordingly.

## Methods

### \_\_construct($objective,$initialTask, $apiKey)

Constructs the AutoGpt class with the given $objective and $apiKey.

### run()

Generates first task if none exists and then recursively executes the list of tasks until the objective is reached.

### generateObjectiveTasks()

Generates the initial list of tasks based on the given objective.

### executeTask()

Executes the given task.

### createNewTasks()

Generates new tasks based on the result of the previous task.

### prioritizeTasks()

Prioritizes the list of tasks based on the given current task.

### sendRequest($prompt)

Sends a request to the GPT-3 API with the given prompt.|
