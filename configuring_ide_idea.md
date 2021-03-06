---
layout: default
title: Configuring your IDE
sitemap:
priority: 0.7
lastmod: 2015-05-22T18:40:00-00:00
---

# <i class="fa fa-keyboard-o"></i> Configuring Intellij IDEA

## Import your project

- Simply open your project normally
- Maven should be detected, and your project will build automatically

## Exclude directories

- Right-click on the `src/main/webapp/bower_components` folder
- Select "Mark Directory As" and select "Excluded"
- You should also exclude
    - `.tmp/`,
    - `node_modules/` and
    - `src/main/webapp/dist` (the `dist` folder will be created when you generate a production build)

![Exclude](images/configuring_ide_idea_1.png)

## Java Code Support

To add code support to many of the JHipster modules from a new project first go to `File → Project Structure`.

![Project Structure](images/configuring_ide_idea_2.png)

Then go to the Modules tab, click on the `+` button, and then click on "Spring" to add Spring code assistance to your project.

![Spring](images/configuring_ide_idea_3.png)

It will tell you there are unmapped Spring configuration files, click on the `+` sign on the  bottom right (not the original one) and select all the Spring files that belong to your project, just clicking the folder is enough to select everything.

![Spring Application Context](images/configuring_ide_idea_4.png)

After that click `OK`, and Spring should be configured with proper code assistance.

Now click on the original `+` button which you used to add Spring in the first place, and add Hibernate. You do not need to add any files on this one, just adding it there will give you Hibernate based code assistance. Remember to click `OK` on the Project structure dialog.

You should now have Java support for most of the codebase. You have to repeat this step every time you start a new project, as these settings are project-specific.

## Javascript Code Support

Go and open `File → Other Settings → Default Settings...`.

![Settings](images/configuring_ide_idea_5.png)

Navigate to `Languages & Frameworks → Javascript → Bower` (or type "Bower" on the top search bar)

![Navigate to Bower](images/configuring_ide_idea_6.png)

Point to your `bower.json`, which is located at the root of your project. The project's libraries, like Angular.js, should be automatically recognized.

After configuring this you should have fairly extensive code support for the Javascript libraries in JHipster.
