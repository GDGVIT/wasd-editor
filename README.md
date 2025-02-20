# WASDEditor Project

<p align="center">
<a href="https://dscvit.com">
	<img width="400" src="https://user-images.githubusercontent.com/56252312/159312411-58410727-3933-4224-b43e-4e9b627838a3.png#gh-light-mode-only" alt="GDSC VIT"/>
</a>
</p>

<h2 align="center">WASDEditor: A Simple Open-Source Dialogue System</h2>

<p align="center">
	<a href="https://gdscvit.itch.io/wasdeditor">
		<img width="400" src="https://github.com/GDGVIT/nonlinear-info-editor/blob/dev/Assets/UI%20Art/WASDEditor_logo_darkmode.png" alt="WASDEditor"/>
	</a>
</p>

---

[![Join Us](https://img.shields.io/badge/Join%20Us-Developer%20Student%20Clubs-red)](https://dsc.community.dev/vellore-institute-of-technology/)
[![Discord Chat](https://img.shields.io/discord/760928671698649098.svg)](https://discord.gg/498KVdSKWR)
[![DOCS](https://img.shields.io/badge/Documentation-see%20docs-green?style=flat-square&logo=appveyor)](INSERT_LINK_FOR_DOCS_HERE) 
[![UI](https://img.shields.io/badge/User%20Interface-Link%20to%20UI-orange?style=flat-square&logo=appveyor)](INSERT_UI_LINK_HERE)

## Project Components

This project consists of three main components:

1. [WASD Editor](https://github.com/GDGVIT/nonlinear-info-editor) - Core editor implementation
2. [WASD Editor Unity Interpreter](https://github.com/GDGVIT/nonlinear-info-unity-interpreter) - Unity integration package

## Features

### Editor
- Character Creation
- Branching Dialogue Trees
- Designer Friendly Interface
- JSON Export Format

### Unity Integration
- Sample Dialogue System Implementation
- Easy Integration with Existing Projects
- Dialogue Callbacks Support
- Compatible with Editor Output

## Dependencies

### Editor Development
- Unity Engine (2023+)
- Newtonsoft JSON (com.unity.nuget.newtonsoft-json)

### Unity Interpreter
- Newtonsoft JSON Package
- Unity 2023+

## Installation & Usage

### Editor
1. Download the binaries from [gdscvit/itch.io](https://gdscvit.itch.io/wasdeditor)
2. Run the application directly - no additional dependencies required

### Unity Interpreter
1. Import the Unity package into your Unity 2023+ project
2. Add the provided prefab to your scene
3. Import JSON files exported from the editor
4. Call `DialogueTreeInterpreter.StartDialogue(TextAsset t)` to initiate dialogue
5. Implement dialogue callbacks as needed

## Technical Details

### Data Format
The following class is used to generate the json output of the program. It uses the newtonsoft.json library to Serialize and Deserialize data

```csharp
// Core Data Classes
public class DialogueTree
{
    public Dictionary<string, float> variables;
    public Character[] chars;
    public DialogueData[] dialogues;
}

public class DialogueData
{
    public int id;
    public string title;
    public string line;
    public OptionData[] options;
    public int[] charIDs;
    public int charCurrentlySpeaking;
}

public struct Character
{
    public int id;
    public string Name;
}

public struct OptionData
{
    public string title;
    public int id;
}
```

## External Libraries

- [UnityUILineRenderer](https://github.com/graphicmismatch/UnityUILineRenderer)

## Contributors

<table>
	<tr align="center">
		<td>
		graphicmismatch (Rayan Madan)
		<p align="center">
			<img src = "https://avatars.githubusercontent.com/u/48159187" width="150" height="150" alt="graphicmismatch(Rayan Madan)">
		</p>
			<p align="center">
				<a href = "https://github.com/graphicmismatch">
					<img src = "http://www.iconninja.com/files/241/825/211/round-collaboration-social-github-code-circle-network-icon.svg" width="36" height = "36" alt="GitHub"/>
				</a>
				<a href = "https://www.linkedin.com/in/rayan-madan/">
					<img src = "http://www.iconninja.com/files/863/607/751/network-linkedin-social-connection-circular-circle-media-icon.svg" width="36" height="36" alt="LinkedIn"/>
				</a>
			</p>
		</td>
	</tr>
</table>

<p align="center">
	Made with ❤ by <a href="https://dscvit.com">GDSC-VIT</a>
</p>
