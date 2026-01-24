I've created this repository in the process of self-teaching myself how to use Eclipse with JDK21 on Win11 for CS335.

To create a Personal Access Token, go to your profile icon menu > Settings > Developer Settings > Personal access tokens > Tokens (classic) > Generate new token

A token is used by Eclipse in replacement for your password when authenticating with Github. Be sure to set it for 90 days or to never expire. Once generated, you will have to save it in a safe place since you cannot retrieve it if lost, and will have to generate a new one if you cannot remember it.

To start a new project in Eclipse, you select File > New Java Project. Deselect **Use Default location** and click Browse to navigate to the location where you store your repositories locally. Select your local directory of local repositories and create a new folder in the dialog window and give it the same name as the repository you wish to set up on Github. Select this folder as the destination you wish save your project files. Click **Select Folder.** Your New Project dialog should now have automatically populated the project name with the same name as the new folder you created. **Deselect Create module-info.java file** in the New Project dialog box. Click finish. A new Java project should appear in your Package Explorer in your left panel in Package Explorer. It should have the following structure:

Right click the project name and go to New > File. Create a file called README.md Click Create. You should see it appear in the Package Explorer in the top level of your project. To edit it, you double-click it. When .md files open in Eclipse, they open in Preview mode. At the base of the README.md window, you should see that you can toggle to Markdown Source tab. Paste the following text. Click File > Save or Ctrl+S to save it.

```
### README.md
```

Right click the project name again, and go to New > File. Create a file called .gitignore like you did previously. Double the click the file once created to open it. Add the following text and save the file by clicking File > Save or Ctrl+S

```
/bin/
.settings/
.classpath
.project
```

Select your repository down arrow to expand the folders. Go to <your-repo-name>/src

Right click the src folder and create a package by going to New > Package. Let the location self-populate. Change the package Name to io.github.<yourgithubname>.<yourprojectname> and click Finish.

Right click the new package you just created, and select New > Class with the following settings:

Source folder: <yourprojectname>/src
Package: io.github.<yourgithubname>.<yourprojectname>
Deselect "Enclosing Type"
Name: YourProjectName 
Modifiers:
public
none
Superclass: java.lang.Object
Do not add Interfaces!
Under "Which method stubs would you to create?" select ONLY public static void main(String[] args)
Click finish

You should now see YourProjectName.java appear in the io.github.<yourgithubname>.<yourprojectname> package.

Add the following Hello World code to your NewProjectJava.java

```
package io.github.omicreativedev.newprojectjava;
// notice how the package name is the same.
// This is standard professional convention.
// It might look weird on your repo but it works.

public class NewProjectJava {

	public static void main(String[] args) {
		System.out.println("Hello World!");
	}

}
```

You should now be able to run this file. It should work.




