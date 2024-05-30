# Unity-Co-op-dialogue-POC
A proof-of-concept project for a Co-op dialogue system in Unity, making use of an external canvas drawing app for creating the dialogue assets.  

An example snapshot of a part of a dialogue created using [Obsidian](https://obsidian.md/)'s canvas drawing app is displayed below, although support for any similar whiteboard app could be implemented. (Such as [tldraw](https://github.com/tldraw/tldraw)):

![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/8c3c267e-1e67-407e-966a-f9f2e7ac9e4a)

The file remains in the project's Resources folder and any changes are picked up by an `AssetPostprocessor` which then converts the file into a Dialogue ScriptableObject, making the process of editing and testing the dialogue extremely fast and easy.  

The result is a scriptable object with each "node" being its own scriptable object parented to the main dialogue scriptable object.

![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/b4a3f1e1-667e-44db-b358-7118e31a6f7a)  

Example NPC and Player response nodes:  
![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/22272577-7aaa-4fe2-9dc8-20d70fac871d)  ![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/92d31bd6-1d98-45fe-9f18-6d0a6096345b)


