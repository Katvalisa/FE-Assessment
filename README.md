# CGM Front-End (React) Coding Assessment

## Prerequisites

Ensure the following are installed on your PC.

1. [Git](https://git-scm.com/)
1. [Docker](https://www.docker.com/)
1. [VSCode](https://code.visualstudio.com/)
1. VSCode Extensions
   - [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Overview

To complete this assessment, you will need to write a simple [React](https://facebook.github.io/react/) web app that is built with [Next.js](https://nextjs.org/), and provide us the source files to be built.

The purpose of this assessment is to assess your **skills and approach to composing a simple web app** given an API feed. We will also assess the **generated HTML, Styling, and JS** output.

This assessment is expected to take about 1-2 hours.

## Getting Started

- Using VSCode install the [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension.
- Press `F1` to bring up the Command Palette and type in `Remote-Containers`
- Select `Clone Repository in Container Volume...`
- Copy the clone link from this repository and paste it into the input box

## What to do?

Your goal is to implement a simple React application, where users will be able to view a job candidate's resume and written responses, comment on the responses & save the data. The UX/UI is totally up to you.

Although its a very basic exercise, we will be looking for simple, well-designed, well-commented code in the submission.

Once you complete your implementation, create a new branch that has the following nameing scheme.

```bash
<Fistname>_<Lastname>
```

If your name is Jane Doe your branch name would be `Jane_Doe`. Push the branch to the origin.

## How should the application work?

The user of this react application should be able to view the resume of job candidates applying for a job at their company. The application should have the following workflow,

1. Choose candidate from a list.
2. Depending on the selection in the first step, if the selected candidate has an application, display the resume and the written responses of the candidate with the relevant question displayed in text. If the selected candidate does not have an application, display appropriate message.
3. For each written response of a candidate, provide an option to enter comments.
4. Provide a "Save" button that saves the comments to the api.

## Requirements

- Only step 1 should be visible when no candidate is picked. Step 1,2,3 and 4 should be visible when a candidate is picked.

- User should be able to change candidate selection at any time.

- You can use whatever libraries, task runners and build processes you like. React and plain JavaScript are the only requirements (ES6+ encouraged, but no TypeScript, CoffeeScript, etc).

## API Usage

| Endpoint                                                     | Method | Result                                                         |
| ------------------------------------------------------------ | ------ | -------------------------------------------------------------- |
| /api/candidates                                              | GET    | Lists all available candidates                                 |
| /api/candidates/applications/application-responses/questions | GET    | Lists all database relations                                   |
| /api/questions                                               | GET    | Lists all available questions                                  |
| /api/applications                                            | GET    | Lists all available applications                               |
| /api/applications/{id}                                       | GET    | List application by candidate id                               |
| /api/applications/{id}/application-responses                 | GET    | List application with responses by candidate id                |
| /api/application-responses                                   | GET    | Lists all available application responses                      |
| /api/application-responses/{id}                              | GET    | List application responses by application id                   |
| /api/application-responses/{id}/comment                      | PATCH  | Update application response comment by application response id |

---
