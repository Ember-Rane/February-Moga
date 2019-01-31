# February 2019 - Moga

4 Weeks Timeline  
Code 1 - Implement a portal that spawns an NPC  
Code 2 - Implement NPC AI  
Code 3 - Improve NPC AI  
Code 4 - Bug Fixes  

Animation 1 - Crab left, right, jump, fall, blendspaces  
Animation 2 - Attack animations, Puzzle solving animations  
Animation 3 - ?  
Animation 4 - Bug fix/upgrades/smoothing out  

Level Design 1 - Camera bugs worked out & Platforms generated  
Level Design 2 - Add in background assets/change material colors etc  
Level Design 3 - Have assets dynamically render/load and remove as level moves  
Level Design 4 - UI addition of time  


-------------------------------------------------------------------


This is a game about a crab who travels through time, sorta.  

Notes:   
To setup an Unreal Engine git repository:   
  
1) Install and prepare git on your desktop
2) Install and prepare git-LFS on your desktop
- https://git-lfs.github.com/ (Step 1)
3) Create an empty repository on your computer where you will eventually have the project XOR Navigate to your project and `git init`
4) Setup git-LFS to track all .uasset and all .umap files 
- https://git-lfs.github.com/ (Step 2)
- `git lfs track *.uasset`
5) Add in the following to the .gitattributes file in the repo  
 
```
# 3D models
*.3dm filter=lfs diff=lfs merge=lfs -text
*.3ds filter=lfs diff=lfs merge=lfs -text
*.blend filter=lfs diff=lfs merge=lfs -text
*.c4d filter=lfs diff=lfs merge=lfs -text
*.collada filter=lfs diff=lfs merge=lfs -text
*.dae filter=lfs diff=lfs merge=lfs -text
*.dxf filter=lfs diff=lfs merge=lfs -text
*.fbx filter=lfs diff=lfs merge=lfs -text
*.jas filter=lfs diff=lfs merge=lfs -text
*.lws filter=lfs diff=lfs merge=lfs -text
*.lxo filter=lfs diff=lfs merge=lfs -text
*.ma filter=lfs diff=lfs merge=lfs -text
*.max filter=lfs diff=lfs merge=lfs -text
*.mb filter=lfs diff=lfs merge=lfs -text
*.obj filter=lfs diff=lfs merge=lfs -text
*.ply filter=lfs diff=lfs merge=lfs -text
*.skp filter=lfs diff=lfs merge=lfs -text
*.stl filter=lfs diff=lfs merge=lfs -text
*.ztl filter=lfs diff=lfs merge=lfs -text
# Audio
*.aif filter=lfs diff=lfs merge=lfs -text
*.aiff filter=lfs diff=lfs merge=lfs -text
*.it filter=lfs diff=lfs merge=lfs -text
*.mod filter=lfs diff=lfs merge=lfs -text
*.mp3 filter=lfs diff=lfs merge=lfs -text
*.ogg filter=lfs diff=lfs merge=lfs -text
*.s3m filter=lfs diff=lfs merge=lfs -text
*.wav filter=lfs diff=lfs merge=lfs -text
*.xm filter=lfs diff=lfs merge=lfs -text
# Fonts
*.otf filter=lfs diff=lfs merge=lfs -text
*.ttf filter=lfs diff=lfs merge=lfs -text
# Images
*.bmp filter=lfs diff=lfs merge=lfs -text
*.exr filter=lfs diff=lfs merge=lfs -text
*.gif filter=lfs diff=lfs merge=lfs -text
*.hdr filter=lfs diff=lfs merge=lfs -text
*.iff filter=lfs diff=lfs merge=lfs -text
*.jpeg filter=lfs diff=lfs merge=lfs -text
*.jpg filter=lfs diff=lfs merge=lfs -text
*.pict filter=lfs diff=lfs merge=lfs -text
*.png filter=lfs diff=lfs merge=lfs -text
*.psd filter=lfs diff=lfs merge=lfs -text
*.tga filter=lfs diff=lfs merge=lfs -text
*.tif filter=lfs diff=lfs merge=lfs -text
*.tiff filter=lfs diff=lfs merge=lfs -text
```

6) If you don't have a UE4 project already, create one now. If you do, update your .gitignore to contain the following: 
```
# Visual Studio 2015 user specific files
.vs/

# Compiled Object files
*.slo
*.lo
*.o
*.obj

# Precompiled Headers
*.gch
*.pch

# Compiled Dynamic libraries
*.so
*.dylib
*.dll

# Fortran module files
*.mod

# Compiled Static libraries
*.lai
*.la
*.a
*.lib

# Executables
*.exe
*.out
*.app
*.ipa

# These project files can be generated by the engine
*.xcodeproj
*.xcworkspace
*.sln
*.suo
*.opensdf
*.sdf
*.VC.db
*.VC.opendb

# Precompiled Assets
SourceArt/**/*.png
SourceArt/**/*.tga

# Binary Files
Binaries/*
Plugins/*/Binaries/*

# Builds
Build/*

# Whitelist PakBlacklist-<BuildConfiguration>.txt files
!Build/*/
Build/*/**
!Build/*/PakBlacklist*.txt

# Don't ignore icon files in Build
!Build/**/*.ico

# Built data for maps
*_BuiltData.uasset

# Configuration files generated by the Editor
Saved/*

# Compiled source files for the engine to use
Intermediate/*
Plugins/*/Intermediate/*

# Cache files for the editor to use
DerivedDataCache/*
```
7) Commit your changes to .gitignore and .gitattributes
8) Check all the files to make sure they are being tracked correctly. Add one location at a time and check in the `git status` results that it shows (LFS -> ###) for the LFS files and (Git -> ###) for the Git files. 
- `git lfs status`
- `git add folderpath\filepath\*`
- `git lfs status`
Make sure that all your .uasset and .umap files appear in the 'Git LFS objects to be committed' section. Make sure all over files are not. 
9) Commit your git LFS changes through terminal. 
- `git commit -m "Setting up git LFS"`
10) Push
