# Activity-Diagram-Generator
This code includes the parser module, generator module, and command-line interface (CLI) for the Activity Diagram Generator. Users can input textual descriptions of activities and transitions via the CLI, and the generator will produce the corresponding activity diagram in YUML syntax.

To add activity diagram generation functionality to the Activity Diagram Generator using YUML, we'll implement a module that translates parsed activity descriptions into activity diagrams using YUML syntax.

The ActivityDiagramGenerator class initializes with an empty constructor.
The generate_diagram method takes the parsed activities as input and generates YUML code for the corresponding activity diagram.
It starts by adding a "Start" node to represent the start of the activity diagram.
It iterates through each activity and target activity in the parsed activities list.
For each activity, it adds a node to represent the activity in the YUML code.
If there is a target activity, it adds a transition arrow between the current activity and the target activity.
Finally, it adds an "End" node to represent the end of the activity diagram.
The method returns the generated YUML code as a string.
You can use this activity diagram generation module along with the parser module to create activity diagrams from textual descriptions of activities and transitions. The generated YUML code can then be used to visualize the activity diagram using YUML tools or libraries. Feel free to extend and customize this module to support additional features or formatting options as needed.

To add a command-line user interface (CLI) for the Activity Diagram Generator using YUML, we'll create a simple CLI interface that allows users to input textual descriptions of activities and transitions and view the generated activity diagrams. We'll also provide options for specifying actions, decisions, loops, concurrency, and transitions. 

The ActivityDiagramCLI class initializes with instances of the ActivityDiagramParser and ActivityDiagramGenerator classes.
The run method displays a welcome message and prompts the user to input textual descriptions of activities and transitions.
The input text is then parsed using the ActivityDiagramParser instance.
The parsed activities are passed to the ActivityDiagramGenerator instance to generate the activity diagram YUML code.
Finally, the generated YUML code is displayed to the user.
Users can input their textual descriptions of activities and transitions, and the CLI will parse them and generate the corresponding activity diagram in YUML format.

You can further enhance this CLI interface by providing additional options for specifying actions, decisions, loops, concurrency, and transitions. These options could be implemented as command-line arguments or interactive prompts, allowing users to customize the generated activity diagrams according to their requirements.

To add error handling and validation to the Activity Diagram Generator CLI, we will ensure that the input provided by the user is properly validated and that appropriate error messages are displayed in case of any issues.

Inside the run method, the input provided by the user is enclosed within a try-except block to catch any potential exceptions.
If an exception occurs during parsing or diagram generation, an appropriate error message is displayed to the user.
This ensures that the CLI interface gracefully handles errors and provides feedback to the user, making the tool more robust and user-friendly.
With the last implementation, users will receive informative error messages if there are any issues with the input or the generation process, allowing them to correct the errors and generate activity diagrams successfully.
