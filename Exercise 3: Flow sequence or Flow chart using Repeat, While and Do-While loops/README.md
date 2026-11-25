# Exercise 3: Flow Sequence or Flowchart Using Repeat, While and Do-While Loops

## NAME: MENAKA M S

## REGISTER NUMBER: 212225040232

## AIM

To create a workflow in UiPath Studio using different loop structures such as Repeat, While and Do-While loops using Flow Sequence or Flowchart.

## SOFTWARE REQUIRED:

Software Used: UiPath Studio

## ALGORITHM

### Part A: Repeat (Using Assign + While)

Step 1:  
Launch UiPath Studio from the desktop or Start menu.

Step 2:  
Click on New Project → Process.

Step 3:  
In the project creation dialog box:

- Enter the process name as `LoopingDemo`.
- Set the project location (e.g., Documents\UiPathProjects).
- Click Create.

Step 4:  
Once the project opens, double-click Main.xaml to open the main workflow.

Step 5:  
From the Activities panel, drag and drop a Sequence activity onto the main design panel.

Step 6:  
Open the Variables panel and create the following variables:

- `counter` → Int32 → Default: 1
- `limit` → Int32 → Default: 5

Step 7:  
Search for the Assign activity and drag it into the Sequence.

Step 8:  
Set the Assign activity:

- To: `counter`
- Value: `1`

Step 9:  
Search for the While activity and drag it below the Assign activity.

Step 10:  
Set the While condition as:

```vb
counter <= limit
```

Step 11:  
Inside the While activity, add a Message Box activity and enter:

```vb
"Count: " + counter.ToString
```

Step 12:  
Below the Message Box, add an Assign activity.

Set the values as:

```vb
counter = counter + 1
```

Step 13:  
After the While loop, add a Message Box activity and enter:

```vb
"Loop ended"
```

Step 14:  
Save the workflow using Ctrl + S.

Step 15:  
Click the Run button (green play icon) at the top of UiPath Studio.

### Part B: Do-While Example

Step 1:  
Open the Main.xaml file in UiPath Studio.

Step 2:  
From the Activities panel, search for the Do While activity and drag it onto the Sequence.

Step 3:  
Open the Variables panel and create a Boolean variable:

- Variable name: `firstRun`
- Variable type: Boolean
- Default value: True

Step 4:  
Inside the Do While activity, add a Message Box activity.

Step 5:  
Enter the following message:

```vb
"This block runs at least once"
```

Step 6:  
Below the Message Box, add an Assign activity.

Set the values as:

```vb
firstRun = False
```

Step 7:  
Set the Do While condition as:

```vb
firstRun = True
```

Step 8:  
Save the workflow using Ctrl + S.

Step 9:  
Click the Run button to execute the workflow.

### Part C: Using Flowchart (Optional)

Step 1:  
Open the Main.xaml file in UiPath Studio.

Step 2:  
Delete the default Sequence activity if required.

Step 3:  
From the Activities panel, search for Flowchart and drag it onto the design panel.

Step 4:  
Add a Flow Decision activity with the following condition:

```vb
counter <= limit
```

Step 5:  
Add the required Assign and Message Box activities to create the loop.

Step 6:  
Connect the activities using the flow connectors.

Step 7:  
Save the workflow and click Run to execute it.

## PROGRAM WORKFLOW:

### Part A: Repeat (Using Assign + While)

The workflow uses Assign and While activities to display numbers from 1 to 5. The counter increases by 1 after each iteration. When the counter becomes greater than 5, the loop terminates.

```text
          START
             |
             v
       Assign counter = 1
             |
             v
       While counter <= 5
             |
             v
       Message Box
         Count: 1
             |
             v
       Assign counter + 1
             |
             |
       Repeat the loop
             |
             v
       Message Box
        "Loop ended"
             |
             v
            END
```

### Part B: Do-While Example

The workflow uses a Do-While activity to display a message at least once. The Boolean variable firstRun is initially True and is changed to False after displaying the message.

```text
          START
             |
             v
      firstRun = True
             |
             v
         Do-While
             |
             v
        Message Box
"This block runs at least once"
             |
             v
      Assign firstRun = False
             |
             v
     Check Condition
      firstRun = True
             |
          FALSE
             |
             v
            END
```

### Part C: Flowchart

The Flowchart uses a Flow Decision activity to check the condition. Based on the condition, the workflow continues the loop or terminates.

```text
          START
             |
             v
       Assign counter = 1
             |
             v
      Flow Decision
      counter <= limit
          /       \
       TRUE       FALSE
         |           |
         v           v
    Message Box     END
         |
         v
   Assign counter + 1
         |
         +------> Flow Decision
```

## UiPath Workflow.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/0ce6a7c2-7d7d-408e-b0fe-0d86399f3541" />

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/56a8387b-08dd-4053-ac6a-a44b33b66a48" />


## OUTPUT

<img width="210" height="225" alt="image" src="https://github.com/user-attachments/assets/17b37ec4-e699-42b5-b517-c117bc0218d1" />

<img width="147" height="170" alt="image" src="https://github.com/user-attachments/assets/a7447553-769f-4f10-aa4b-5e998cbdade9" />

<img width="210" height="246" alt="image" src="https://github.com/user-attachments/assets/3b1f5ccf-43c2-4ee0-8e62-de9ca30a1750" />

<img width="213" height="222" alt="image" src="https://github.com/user-attachments/assets/4ce50307-d1e2-4a28-abf7-0743baf74498" />

<img width="151" height="182" alt="image" src="https://github.com/user-attachments/assets/0a9b1dd6-2944-487d-9123-3f770240f638" />

<img width="227" height="232" alt="image" src="https://github.com/user-attachments/assets/6ebe46b6-9942-4e62-9fcb-a1e779608fae" />



## RESULT

Thus, the workflow was successfully created and executed in UiPath Studio using Repeat (Assign + While), While and Do-While loop structures. The looping activities were implemented successfully, and the expected outputs were displayed.
