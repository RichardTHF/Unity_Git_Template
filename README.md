# Welcome to the Unity / GitHub template. 
 [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)]

This repository is a template repository to be used by Birmingham City University Students and Staff when using GitHub with Unity.

### For programmers
You'll want to set up **Unity SmartMerge** on your repository to make it easier to handle merge conflicts with Unity files. To do this, go into your `.git` folder and change the `config` file to include the following (Please note that you will need to 'display hidden' in order to see the config file and the .git folder):

```
[merge]
	tool = unity_yaml

[mergetool "unity_yaml"]
	cmd = 'C:\\Program Files\\Unity\\Hub\\Editor\\2019.1.10f1\\Editor\\Data\\Tools\\UnityYAMLMerge.exe' merge -p "$BASE" "$REMOTE" "$LOCAL" "$MERGED"
	trustExitCode = false
	keepTemporaries = true
	keepBackup = false
```

replacing the `C:\...` with a path to **your computer's installation of Unity 2019.1.10f1**, if it's different to the above. Running `git mergetool` will then try and fix merge conflicts that Git can't handle itself for you.

### For artists and sound engineers
You're welcome to keep project files in this repository (such as .psd, .blend and .aup)! However, bear in mind that while Unity will automatically import the contents of these files for the programmers to use, this may not always work as intended. It's preferable that you also manually export images to **PNG**, 3D models to **FBX**, and sound files to **WAV** or **OGG Vorbis** to ensure everything is as expected.


Many thanks to @tonaxite for helping to put this together. 

