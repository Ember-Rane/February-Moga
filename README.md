# February19
To setup an Unreal Engine git repository: 

1) Install and prepare git on your desktop
2) Install and prepare git-LFS on your desktop
+ https://git-lfs.github.com/ (Step 1)
3) Create an EMPTY repository on your computer where you will eventually have the project. 
4) Setup git-LFS to track all .uasset and all .umap files 
+ https://git-lfs.github.com/ (Step 2)
+ git lfs track *.uasset
5) Create (or copy over) your Unreal Engine project into the repository you just created.
6) Check all the files to make sure they are being tracked correctly
+ git lfs status
+ git add filepath\filename\*
+ git lfs status
+ Repeat until done.
Make sure that all your .uasset and .umap files appear in the 'Git LFS objects to be committed' section. Make sure all over files are not. 
7) Commit your git LFS changes through terminal. 
+ git commit -m "Setting up git LFS"
8) Commit any deleted or modified files from the github desktop GUI (these didn't go through the git LFS commit?)
9) Push
