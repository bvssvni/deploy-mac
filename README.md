deploy-mac
==========

How to create executables for mac running with Mono framework

##Step 1: Minimum Setup

1.1 How To Create Folder & Copy Files

1.1.1 Create a new folder "SETUP Mac" in your project folder.

1.1.2 Inside "SETUP Mac", create a new folder "{your app}".

Do not add ".app" extension yet! We will do this later.

1.1.3 Inside "{your app}", create a new folder "Contents".

1.1.4 Inside "Contents", create a folder "MacOS".

1.1.5 Inside "MacOS", copy & paste files from your project "bin/Debug" or "bin/Release" folder.

If you like to get line numbers in uncaught exceptions, use "bin/Debug".

1.2 How To Create Metadata.

1.2.4 Open TextEdit.

This is a text editor that is included with Mac OS X.

1.2.5 Goto Format->Make Plain Text.

If you see "Make Rich Text" instead, skip this step.

1.2.6 Paste the following code into TextEdit.

    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE plist PUBLIC "-//Apple Computer//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
    <plist version="1.0">
    <dict>
    	<key>CFBundleExecutable</key>
    	<string>{executable}</string>
    	<key>CFBundleIdentifier</key>
    	<string>com.{company}.{product}</string>
    </dict>
    </plist>
    
1.7 Replace "{executable}" with the file name inside "MacOS" that starts the program.

1.8 Replace "{company}" with the name of your company.

If you do not have a company, make up one name.

1.9 Replace "{product}" with the name of your product.

1.10 Save the file in the "Contents" folder.

1.11 Rename the "{your app}" folder to "{your app}.app".

The folder structure should now seem like one file in Finder.

1.12 Double-click the icon to test.

If something is wrong, remove the ".app" ending to get back the folder structure.

##Example Info.plist From MonoDevelop

    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE plist PUBLIC "-//Apple Computer//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
    <plist version="1.0">
    <dict>
      <key>CFBundleDocumentTypes</key>
    	<array>
    		<dict>
    			<key>CFBundleTypeIconFile</key>
    			<string>monodevelop.sln.icns</string>
    			<key>CFBundleTypeExtensions</key>
    			<array>
    				<string>sln</string>
    			</array>
    			<key>CFBundleTypeName</key>
    			<string>MonoDevelop Solution</string>
    			<key>CFBundleTypeRole</key>
    			<string>Editor</string>
    			<key>LSIsAppleDefaultForType</key>
    			<true/>
    		</dict>
    		<dict>
    			<key>CFBundleTypeIconFile</key>
    			<string>monodevelop.sln.icns</string>
    			<key>CFBundleTypeExtensions</key>
    			<array>
    				<string>mdw</string>
    			</array>
    			<key>CFBundleTypeName</key>
    			<string>MonoDevelop Workspace</string>
    			<key>CFBundleTypeRole</key>
    			<string>Editor</string>
    			<key>LSIsAppleDefaultForType</key>
    			<true/>
    		</dict>
    		<dict>
    			<key>CFBundleTypeExtensions</key>
    			<array>
    				<string>cs</string>
    			</array>
    			<key>CFBundleTypeName</key>
    			<string>C# Source File</string>
    			<key>CFBundleTypeRole</key>
    			<string>Editor</string>
    			<key>LSIsAppleDefaultForType</key>
    			<true/>
    		</dict>
    	</array>
    	<key>CFBundleDevelopmentRegion</key>
    	<string>English</string>
    	<key>CFBundleExecutable</key>
    	<string>MonoDevelop</string>
    	<key>CFBundleIconFile</key>
    	<string>monodevelop.icns</string>
    	<key>LSApplicationCategoryType</key>
    	<string>public.app-category.developer-tools</string>
    	<key>LSMinimumSystemVersion</key>
    	<string>10.6</string>
    	<key>CFBundleIdentifier</key>
    	<string>com.xamarin.monodevelop</string>
    	<key>CFBundleInfoDictionaryVersion</key>
    	<string>6.0</string>
    	<key>CFBundleName</key>
    	<string>MonoDevelop</string>
    	<key>CFBundlePackageType</key>
    	<string>APPL</string>
    	<key>CFBundleShortVersionString</key>
    	<string>3.1.1</string>
    	<key>CFBundleSignature</key>
    	<string>xmmd</string>
    	<key>CFBundleVersion</key>
    	<string>3.1.1</string>
    	<key>NSAppleScriptEnabled</key>
    	<string>NO</string>
    	<key>QuartzGLEnable</key>
    	<false/>
    	<key>NSHighResolutionCapable</key>
    	<true/>
    </dict>
    </plist>
    
