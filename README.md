<br>

<h4 align="center">Correlations Recorder Templates</h4>

<p align="center">
  <a href="#about">About</a> •
  <a href="#prerequisites">Prerequisites</a> •
  <a href="#creating-templates">Creating Templates</a> •
  <a href="#sharing-templates">Sharing Templates</a>
</p>

# About

Correlations Recorder Central Repository its a community where users can share their Correlation Templates to be used, and automatically downloaded into the [Correlation's Recorder JMeter Plugin](https://github.com/Blazemeter/CorrelationRecorder).

# Prerequisites

In order to download, update and share templates you need to:

1. Download and Install JMeter
1. Install JMeter Plugin Manager
1. Install Correlations Recorder Plugin

# Creating Templates

From there, you can either start creating your templates from scratch or, load and edit one from the Central Repository, loaded by default into your machine.

## Building from Scratch

Here you can use the Template we prepare for you or, just add the Component as it is. 

### Using the Template

1. Go to JMeter Templates
1. Select "Correlation Recorder"
1. Select the "Correlation Recorder" component

### Adding the Component

1. Click in your Test Plan
1. Follow this route: Add > Non-Test Element > "Correlation Controller"
1. Select the "Correlation Recorder" Component

---

From this point onwards, its just about adding Rules by clicking the "Add Button" and, when you are ready, save your Correlation Template.

## Using one from This Repository

Loading one from the Central Repository saves you time and effort for the setting up part.

1. Just go to Load Template button. (If the desired template its installed, go to the "Installed" Tab, if it isn't, then go to the "Available" Tab)
1. Pick the template that you want to use
1. Select the Version you want to load
  1. If the template's version ain't installed: you must click on install button, before loading it.
  1. If the template's version is installed: click the load button to load it.

Note: If you installed a template that required external dependencies, this will trigger a JMeter reset (or ask you to manually reset other wise). After that, just repeat the process until the point where you can load it, and click the load button.

---

Just like in the [Building from Scratch](#building-from-scratch) section, after doing this, you only need to edit and save the template.

# Sharing Templates

When it comes to load and share the Correlations Templates, there are some steps you need to follow to do so. In this section, we will talk about them.

## Process to contribute with this repository

1. Clone the actual repository into your machine

> git clone https://github.com/Blazemeter/CorrelationsRecorderTemplates.git

2. Edit the central-repository.json file 

## If its your first time

* Adding the name of the template, follow by a pair of `{}`

	"myTemplate" : {}
	
* Adding a version array inside, with all the versions you want to add

	"myTemplate" : {
		"versions": ["1.0", "2.0"]
	}
	
## If you are updating

* Just add the new version into the array

3. Copy the files for those versions into the same level of that central-repository.json file

4. Add the files into git

The easiest way always is

```git
git add .
```

or one by one

```git
git add central-repository.json 
git add myTemplate-1.0-template.json
git add myTemplate-2.0-template.json
````

5. Push to our repository and make a PR. 

At the end, should look like this

```
+ central-repository.json (updated)
+ myTemplate-1.0-template.json
+ myTemplate-2.0-template.json
```

# Some considerations 

1. Remember that, if your template contains dependencies, those must be uploaded into public external cloud were everyone can access without logging in. 
1. All the versions mentioned in your template **MUST** be in the same level as the central repository (don't create sub folders for any reason)
1. Don't edit others template but your own
1. Be nice

# License

Apache License 2.0

```text
A permissive license whose main conditions require preservation of copyright and license notices. 
Contributors provide an express grant of patent rights. Licensed works, modifications, and larger 
works may be distributed under different terms and without source code.
```

To know more about it, read the license [here](https://github.com/Blazemeter/CorrelationsRecorderTemplates/blob/master/LICENSE)
