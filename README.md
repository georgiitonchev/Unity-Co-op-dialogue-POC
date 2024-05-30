# Unity Co-op-dialogue POC
A proof-of-concept project for a Co-op dialogue system in Unity, making use of an external canvas drawing app for creating the dialogue assets.  

An example snapshot of a part of a dialogue created using [Obsidian](https://obsidian.md/)'s canvas drawing app is displayed below, although support for any similar whiteboard app could be implemented. (Such as [tldraw](https://github.com/tldraw/tldraw)):

![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/8c3c267e-1e67-407e-966a-f9f2e7ac9e4a)

The file remains in the project's Resources folder and any changes are picked up by an `AssetPostprocessor` which then converts the file into a Dialogue ScriptableObject, making the process of editing and testing the dialogue extremely fast and easy.  

The result is a scriptable object with each "node" being its own scriptable object parented to the main dialogue scriptable object.

![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/b4a3f1e1-667e-44db-b358-7118e31a6f7a)  

The sytem features a node based approach, where each node ultimately leads to multiple others based on the **type** of connection.  
One of the main features of a co-op dialogue is that the response of one of the players might affect the available responses for the other.

This functionality is implemented using "Change" and "Disable" groups, that are subscribed to a player response event and either change or disable responses for the other player.  

![image](https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/51762a43-c0ae-475a-bb17-eca9d70a51d0)  

The results can be seen in the following videos: 

Change group:  

https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/fde37be0-bd6c-426b-8e04-d0ab411d46f7  

Disable group:  

https://github.com/georgiitonchev/Unity-Co-op-dialogue-POC/assets/16121911/9a77661c-b95a-4d25-ae79-b0037f77f1c4
