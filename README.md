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
This step uses [this](https://circleci.com/docs/api/#trigger-a-new-build-by-project-preview) API call to trigger a new project build.


# Installation

## CircleCI Setup
Create an Personal API Token
1. Go to [Personal API Tokens](https://app.circleci.com/settings/user/tokens)
2. Create a new Personal API Token

## xMatters Setup
1. Download the [CircleCISteps.zip](CircleCISteps.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Put your Personal API Token from CircleCI into a constant for use in steps.
5. Create an Endpoint for CircleCI (Probably `https://circleci.com/api/v1.1`)


## Usage
The **CircleCI - Trigger Build** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **CircleCI Steps** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| API Token | Yes | 0 | 2000 | Personal API Token | | No |
| VCS Type | Yes | 0 | 2000 | Refes to your chosed VCS (either `github` or `bitbucket`) | | No |
| Organization | Yes | 0 | 2000 | Name of CircleCI Organization (might be username) | | No |
| Repository | Yes | 0 | 2000 | Name of repository | | No |
| Branch | Yes | 0 | 2000 | Name of branch | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| Results | Results of requesting build |



## Example
This is an example of triggering a build with a webhook.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

