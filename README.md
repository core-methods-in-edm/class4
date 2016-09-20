# Class 4 - Swirl

##Instructions

This week you will be acquiring and submitting some work through Github. To do this you will need to have RStudio & Github connected. If you have not already done this, please follow the instructions [here](http://www.molecularecologist.com/2013/11/using-github-with-r-and-rstudio/) (Mac) or [here](http://www.r-bloggers.com/rstudio-and-github/) (Windows). This can be a non-trivial step, so save some time to do it. If you are having trouble either Tweet your anguish or email me directly. (The crucial step is that in RStudio under Tools -> Global Options -> Git/SVN you must fill in the both the boxes: Git executable and SVN executable with the locations of both of those files.)

Once you have set up this connection we will be using an R package named Swirl, Swirl is an interactive R lesson generator. Your task will be to do an introductory lesson in R and pull the data back to the Github repository.


**Step 1:** Fork the class4 repository to your personal Github Account.

**Step 2:** Copy the URL for your forked class4 repository.

**Step 3:** Open RStudio and start a new project (File -> New Project...)

**Step 4:** Within the "Create Project" dialog box choose "Version Control" and then "Git: Clone a project from a Git repository"

**Step 5:** Paste the URL for your class4 repository under "Repository URL"

**Step 6:** Name the directory "Class 4 - Swirl" and save it to a place on your computer that you will be able to locate

**Step 7:** Install the "Swirl" package either by typing `install.packages("swirl")` into the Console window or installing through the "packages" tab on the bottom right window.

**Step 8:** Load swirl by typing `library(swirl)` into the Console window.

**Step 9:** Initiate Swirl by typing `swirl()`

**Step 10:** Follow the instructions Swirl gives you to complete the lesson - you want to do the Data Science in Education course, **not** a preloaded Swirl course.

**Step 11:** Once you have completed and exited the lesson, type the following code into the RStudio Console window to export your lesson data. (You may need to change the file path in the first line. To do so search for "history_database" and replace the file path to pint at that location on your computer).

        H <-read.table("~/.rstudio-desktop/history_database", sep=":", fill=T, stringsAsFactors=F) 
        H <- H[which(H$V2 == "Lesson One"):which.max(as.numeric(H$V1)), ]
        names(H) <- c("time", "answer")
        H$id <- "YOUR NAME"
        write.csv(H, file = "lesson1.csv")

**Step 12:** Now commit all changes to your cloned repository by clicking the "Git" button on the top of the left hand pane and then "Commit" from the drop-down menu.

**Step 13:** Check all the boxes in the top left of the Review Changes window and describe the nature of your commit in the right hand pane.

**Step 14:** Once you have commited your assignment, click the "push" button in the top right hand of the corner of the window to "push" your commit to your online repository.

**Step 15:** Return to the your Github page to check that the files appear there and then create a "Pull Request" to submit your work.


        
