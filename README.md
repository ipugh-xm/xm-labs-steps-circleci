# CircleCI Steps

This step allows you to trigger a build in CircleCI.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [CircleCISteps.zip](CircleCISteps.zip) - Workflow zip file with the step and example flow
* [circleci.png](/circleci.png) - CircleCI logo

# How it works
The step pulls the commit information using the GitHub REST API GET `/repos/{Username}/{Repository}/commits/master`.


# Installation

## CircleCI Setup
Create an API Token
1. Go to Project Settings
2. Go to API Permissions
3. Generate an API Permission with scope all

## xMatters Setup
1. Download the [CircleCISteps.zip](CircleCISteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
The **CircleCI - Trigger Build** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **CircleCI Steps** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Username  | Yes | 0 | 2000 | The username or organization the repository lives under | | No |
| Repository | Yes | 0 | 2000 | The name of the repository | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| URL | URL of the repository |
| SHA | The SHA hash of the commit |
| Author_Name | Full name of the author. |
| Author_Email | Email address of the author. | 
| Timestamp | Timestamp of the commit. |
| Message | Commit message |



## Example

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

