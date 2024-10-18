# CNU Media 2024 Unity

## What is Unity ?

Unity is a versatile and widely-used game engine developed by Unity Technologies

Ddesigned for creating both 2D and 3D games. Known for its user-friendly interface and flexibility

Unity is popular among developers ranging from beginners to professionals

### How to Install

Unity is currently installed and managed through Unity Hub, so you need to download and install Unity Hub first

Unity Hub [Download link](https://unity.com/download)


### Install Unity

In Unity Hub, switch to the "Installs" tab to manage installed Unity versions or install different versions of Unity

※ Before using Unity Hub, you must sign in with your Unity ID

![Image](./images/UnityHub_InstallsTab.png)

## Let's start a new Unity project!

First, switch to the "Projects" tab in Unity Hub

Here, you can manage previously opened Unity projects

You can directly click on a project from the list to open it, or click the "New Project" button in the top-right corner to create a new project

Now let's click on "New Project" to continue the introduction

![Image](./images/UnityHub_ProjectsTab_NewProject.png)

### Create a new project

On the project creation page

select 3D under the Templates section in the middle of the screen.

On the right side of the screen, enter the project details, such as the "project name" and "storage path"

Check whether to use "Unity Cloud" or "Unity Version Control" services

Finally, click the "Create Project" button to create the project

![Image](./images/CreateNewProject.png)

## In Unity

### Create terrain and Player

First, use "Plane" and "Cube" to create the floor and walls of the scene

Combine "Capsule" and "Cube" to form the Player

![Image](./images/CreateTerrainAndPlayer.png)

Let's decorate the Player with a Material. Otherwise, it will be too plain with just white

Right-click on the "Assets" folder in the "Project" panel

Then select "Create" and click on "Material" to add a new material

After adding the Material, you can give it a recognizable name

Use different Materials to decorate your Player!

※ You can create additional folders within the "Assets" folder to manage different types of assets

![Images](./images/CreateMaterial.png)

### Add C# Script

Create a new folder within the "Assets" folder and name it "Scripts"

Right-click on the "Scripts" folder, then select "Create" and click on "C# Script" to add a new C# file

Name this C# file "Player"

![Image](./images/CreateCSharpScript.png)

![Image](./images/CreatePlayerScript.png)

## Let's make the Player move!

Click on the "Player" script file to open it

Add the following code in the "Update" method

Allow the user to move the Player's position using the "W" , "A" , "S" and "D" keys

```cs

if (Input.GetKey(KeyCode.W))
{
    this.gameObject.transform.Translate(0, 0, .01f);
}

if (Input.GetKey(KeyCode.S))
{
    this.gameObject.transform.Translate(0, 0, -.01f);
}

if (Input.GetKey(KeyCode.A))
{
    this.gameObject.transform.Translate(-.01f, 0, 0);
}

if (Input.GetKey(KeyCode.D))
{
    this.gameObject.transform.Translate(.01f, 0, 0);
}

```

Next, move the mouse to rotate the Player's angle

Add the following code in the "Update" method.

```cs

gameObject.transform.Rotate(0, Input.GetAxis("Mouse X") * 5, 0);

```
