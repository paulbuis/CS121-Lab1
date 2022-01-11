
# CS 121 - Lab 1 - January 13, 2022

## Objective

Create a Java project in IntelliJ that does simple
arithmetic in a console window.

We will be computing an average of 3 integers. The result
will be a floating point number

# Create a project in IntelliJ

## Step 1 - Welcome to IntelliJ IDEA

When IntelliJ starts up, it presents you with a dialog titled
`Welcome to IntelliJ IDEA.` In the center will be a list of
projects that you have started (maybe empty now).
Along the top on the right will be buttons labelled
`New Project`, `Open`, and `Get from VCS`.
These are the buttons we will be using in this session.

## Step 2 - New Project

From the `Welcome to IntelliJ IDEA` dialog, click on the `New Project`
button and a dialog titled `New Project` should appear.
From this dialog, we will go with the default project
type `Java` on the left, and not select any `Additional Libraries and Frameworks`
in the middle. Along the top will be a dropdown labelled `Project SDK`
which I am hoping says something like `Oracle OpenJDK version 17.0.1`.

If the dropdown does not display a version 16 or 17 JDK,
click on the dropdown arrow on the right and choose `Download JDK...`
This will open yet another dialog labelled `Download JDK`.
With the `Version` dropdown, select `17`. and with the `Vendor Dropdown`
select `Oracle OpenJDK` and then click the `Download` button. This
should return you to the `New Project` dialog (after a brief wait).

In the `New Project`, dialog, click the `Next` button along the bottom.
Click the `Next` button again to skip the next screen.
You should now be seeing a text box on the top of the dialog labelled "Project name:"

Put `Lab1` (capitalize the first letter) in the text box labelled "Project name:"
and click on `Finish` at the bottom of the dialog.
A directory by this name will be created in your `IdeaProjects` folder.

## Step 3 - Create a `package` in your new project

At this point, you will enter the main window of the IntelliJ 
integrated development environment.
In the middle of the screen will be a window that is currently blank,
but later will hold a tabbed set of source code editing windows.
Along the left edge will be a pane labelled `Project`.
In the `Project` pane will be a hierarchy of Names with `Lab1`
(with a folder icon next to it) at the top. Under `Lab1`, choose `src`
(also with a folder icon), right click and choose `New` (at top), then `Package`
(about the fifth on the list). A dialog labelled `New Package` will appear.
Enter `cs121` (lowercase) over the prompt for `Name`.
You should now see a `cs121` folder highlighted in the the `Project` pane
that is a subfolder of the `src` folder.


## Step 4 - Create a `class` in your `package`

Right-click on the `cs121` package folder in the `Project` pane and
choose `New` -> `Java Class`. The "New Java Class" dialog box should
appear with `Class` highlighted in the bottom.
Along the top will be a text box labelled `Name`.
In the `Name` field type `Average` (capitalize the first letter).

At this point, there should be a tab labelled `Average.java`
in the middle of the IntelliJ window with code that looks like:

``` Java
package cs121;

public class Average {
}
```

## Step 6 -  Add a `main` method to `class Average`

Change it so `Average.java` looks like (copy-paste from your browser window)

``` java
package cs121;

public class Average {
    public static void main(String[] args) {
        int x = 1;
        int y = 2;
        int z = 4;
        int sum = x + y + z;
        int average = sum / 3;
        System.out.println("average = " + average);
    }
}
```

## Step 7 - Run the code to see the results

While the `Average.java` editor is selected, in the menu bar chose `Run...` and you should be prompted with a dialog called `Run`.
The dialog should allow you to select `Edit Configurations` or `Average`.
What it is essentially asking is where to find the `main` where the program 
should start. Choose `Average` to indicate that you
want to run the `main` in Average.java.

After a brief pause to compile the code and then run it,
a `Run` pane should appear at the bottom of the window,
below the editor and project panes. The first line will be
an unintelligible mess (ignore it), but the next line should be the output
of your program. After your output there will be a line saying something
like `Process finished with exit code 0`
indicating the compile/run process as one would normally expect.

## Step 8 - Swap roles between pilot and navigator

The pilot should choose `File` -> `Close Project` and swap places with the navigator.

You should now be at the `Welcome to IntelliJ IDEA` dialog that
appears when you first started IntelliJ. However, in the main pane
of the window, you should see the `Lab1` project you started earlier.
You could simply click on the `Lab1` entry in the main pane, and you would be
returned to the main IntelliJ window looking much as it did at the beginning of Step 7.

However, instead, what I want you to do click the `Open` button along the top edge.
The `Open file or project` dialog will appear.
In the main pane of the dialog you should see
a set of folders from your computer listed with your home directory selected.
From there, scroll (down) until you see the folder labelled `IdeaProjects`.
Select the `IdeaProjects` folder and then select the `Lab1` subfolder.
The point is that the list of project in the `Welcome to IntelliJ IDEA` dialog
is just the list of folders under `IdeaProjects` in your home directory
on your computer.

Click on `OK` at the bottom of the `Open file or project` dialog, and
you will be back at the main IntelliJ window looking much as it did at
the beginning of Step 7.

## Step 9 - Experiment with changing the code and running the modified code.

Make changes to the code such as changing `int average` to `float average` and
changing `3` to `3.0` to see if that gives more satisfactory results.
What is desired is output that approximates 7/3 in decimal.

## Step 10 - Use my GitHub source code repository

Again, choose `File` -> `Close Project` and return to the initial
`Welcome to IntelliJ IDEA` dialog. This time, we will use the third
button labelled `Get from VCS`. When prompted for a URL, enter:
`https://github.com/paulbuis/CS121-Lab1.git` and then click the `Clone`
button at the bottom of the dialog.

If prompted, go ahead and "Trust" the Gradle project. This version of the Lab
project is slightly messier looking in the `Project` pane. Instead of a `Java`
project type, it was created as a `Gradle` project type. In the `Project` pane,
drill down to `src` -> `main` -> `java` -> `cs121` -> `Average` and click on `Average` to open
the file `Average.java` in the editor.
Note that it is using `printf()` instead of `println()`.

Again, use `Run` to compile and execute the program.
This time, a more complex process is used to build the project,
so it will take a tad longer and result in more verbose output in the `Run` pane.
Scroll up in the `Run` pane until you see `> Task :Average.main()`
followed by the output of the program.

Replace the values being assigned to `x`, `y` and `z` with `1000`, `2000` and `3000`. Replace the format specifier of `%f` with a format specifier of `%,8.2f`. This says to present the output in an 8 column wide format with 2 digits to the right the decimal point and use comma separator(s) and to use a comma separator to the left of the decimal point.

Run the program again.

# When done, signal instructor to record completion of lab

You will get 20 points for the lab when the result appearing in the run pane
is 2,333.33 with both a comma and a decimal point.

After your points have been recorded, you may leave,
or you may repeat any part of the lab you are uncomfortable
with until you feel comfortable with it.

If you only complete Step 9 you will get 15 points.

If you only complete Step 8 you will get 10 points.

If you only complete Step 7 you will get 5 points.

You must complete at least step 7 to get points for this lab.