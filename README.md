Skip to content
Annleee-12
GAME_PROGRAM-EX--4
Repository navigation
Code
Pull requests
Actions
Projects
Security and quality
Insights
Files
Go to file
t
T
README.md
You’re making changes in a project you don’t have write access to. Submitting a change will write it to a new branch in your fork jedidiahmoide3-ui/GAME_PROGRAM-EX--4, so you can send a pull request.
GAME_PROGRAM-EX--4
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

2
Line wrap mode

Soft wrap
Editing README.md file contents
  1
  2
  3
  4
  5
  6
  7
  8
  9
 10
 11
 12
 13
 14
 15
 16
 17
 18
 19
 20
 21
 22
 23
 24
 25
 26
 27
 28
 29
 30
 31
 32
 33
 34
 35
 36
 37
 38
 39
 40
 41
 42
 43
 44
 45
 46
 47
 48
 49
 50
# GAME_PROGRAM-EX--4
# Attach Rifle with character mesh and implementation bullet spawn from Rifle
## AIM
To create an aiming system (attach and aim a rifle with a character) in Unreal Engine,you’re using a third-person character and a rifle skeletal mesh.


## Procedure

### 1.Attach the Rifle to the Character

Import the Rifle Skeletal Mesh into Unreal Engine.
Open your Character Blueprint (e.g., BP_ThirdPersonCharacter).
In the Components tab:
Add a Skeletal Mesh or Static Mesh component (name it Rifle).
Set its Skeletal Mesh to your rifle asset.

### 2.Attach the Rifle to a socket on the character’s skeleton:

In the Rifle component, set the Parent Socket to something like hand_r (right hand socket).

manually attach in Event Graph:
```
Rifle->AttachToComponent(Mesh, FAttachmentTransformRules::SnapToTargetNotIncludingScale, "hand_rSocket");
```

### 3. Add Aiming Mechanism

Create a Boolean variable called IsAiming.
Set up Input in Project Settings:
Go to Edit > Project Settings > Input.
Add an Action Mapping named Aim (e.g., Right Mouse Button).

### 4. Adjust Camera When Aiming

Add a Camera Boom and Follow Camera.

In Event Graph:
```
When IsAiming = true, zoom the camera in (FOV) and slightly shift it over the shoulder.
```

## Output
![rifle man](https://github.com/user-attachments/assets/3b5ae058-072c-4bc4-96ba-5374565482f6)


![rifle bluprint](https://github.com/user-attachments/assets/8bb07417-9197-4bb5-9f05-c200cbc77c67)

##  Result
Attach Rifle with character mesh and implementation bullet spawn from Rifle is successfully done.

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
 
