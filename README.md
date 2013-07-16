deploy-mac
==========

How to create executables for mac running with Mono framework

1. Download the files of this repository.
2. Copy the folder "YourApp" to your project folder.
3. Rename the copied folder to the name of your app (without ".app" extension).
4. Copy the binary files to "{YourApp}/Contents/MonoBundle".
5. Open up "{YourApp}/Contents/Info.plist" in a text editor.
6. Replace "{YourApp.exe}" with the name of your executable.
7. Replace "{company}" with the name of your company.
8. Replace "{product}" with the name of your product.
9. Add ".app" extension to the folder that was called "YourApp".
10. Done!

This is a minimalistic setup for deployment to Mac OS.  
For further settings, such as file assosiations and app icon,  
edit the "Info.plist" file.  
This can be done in Xcode or with an editor.  
You can use MonoDevelop's Info.plist as example.  
