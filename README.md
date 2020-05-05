# GitLab Steps

This step allows you to get the commit details from a given project. Great for enriching notifications with relevant code commit information. 


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [GitLab.zip](GitLab.zip) - Workflow zip file with these steps and example flow
* [gitlab.png](/gitlab.png) - GitLab logo

# How it works
These steps pull from various API endpoints in GitLab to get commit detils.

[Get All Commits](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits)

[Get Single Commit](https://docs.gitlab.com/ee/api/commits.html#get-a-single-commit)

[Get Projects](https://docs.gitlab.com/ee/api/projects.html#list-user-projects)


# Installation

## GitLab Setup
If you are trying to access a public project, then none.

If your project is private, then you will need to authenticate with an API Token.

------------------------ Instructions here -------------------

## xMatters Setup
1. Download the [GitLab.zip](GitLab.zip) file onto your local computer
2. Navigate to the Developer tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded

Optionally change the GitLab endpoint if your project is hosted outside of GitLab.


## Usage
**Get All Commits**

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Project ID | Yes | 0 | 2000 | The ID or URL-encoded path of the project owned by the authenticated user | | No |

### Outputs
| Name | Description |
| ---- | ----------  |
| Commits | List of Commit Objects |

-----------
**Get Single Commit**

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Project ID | Yes | 0 | 2000 | The ID or URL-encoded path of the project owned by the authenticated user | | No |
| SHA | Yes | 0 | 2000 | The commit hash or name of a repository branch or tag | | No |

### Outputs
| Name | Description |
| ---- | ----------  |
| URL | URL of the project |
| Author_Name | Full name of the author |
| Author_Email | Email address of the author |
| Timestamp | Timestamp of the commit |
| Message | Commit message |

-----------
**Get Projects**

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| User ID | Yes | 0 | 2000 | The ID or username of the user | | No |

### Outputs
| Name | Description |
| ---- | ----------  |
| Projects | List of Project Objects |

## Example
This is an example using the GitLab steps in order to get commit details from a repo.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

