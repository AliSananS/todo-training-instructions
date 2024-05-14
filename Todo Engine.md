# Todo Engine

## How it works?

The todo engine manages a database of todo lists and updates it based on the data provided by the AI model in a json format.

## How does the database look like

The database is an array of todos that look like the code below.

```json
{
"todo": [
   {"id": 88277,
    "title": Title of the Todo,
    "description": "Description of the task.",
    "time": "16:00/01/01/2024",
    "priority": "important",
    "urgent": "false",
    "notificationType": "alarm",
    "isCompleted": false,
    "expires": "22:00/01/01/2024"
   }
],
"message": "The message from AI assistant."
}
```

# Todo Data Documentation

## Data Structure

Each to-do item is represented as a JSON object with the following fields:

- **id (Integer)**: A unique identifier for each to-do item.
- **title (String)**: The title of the to-do.
- **description (String)**: A brief description of the task.
- **time (String)**: Time at which the task is scheduled. It is represented in the format "HH:MM/DD/MM/YYYY".
- **priority (String)**: The importance level of the task. Possible options are "low", "high" and "critical".
- **urgent (Boolean)**: A boolean value ("true" or "false") indicating whether the task is urgent.
- **notificationType (String)**: The type of notification set for the task. Possible options are “notification”, “alarm” and “silent”.
- **isCompleted (Boolean)**: A boolean value indicating whether the task has been completed.
- **expires (String)**: The expiration time of the task, represented in the format "HH:MM/DD/MM/YYYY".

## What operations the engine does?

The engine takes json data to manipulate todo database. 

It takes the following arguments to manipulate the database.