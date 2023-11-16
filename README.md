
<!--
Copyright © GOAST INC.
All rights reserved.
-->

# goastVS: A Task Driven Text-to-Code Extension

<table style="width: 100%; border-style: none;"><tr>
<td style="width: 140px; text-align: center;"><a href="https://marketplace.visualstudio.com/items?itemName=goast-ai.goast"><img width="128px" src="docs/images/goast.png" alt="Goast logo"/></a></td>
<td>
<strong>Autopilot for software engineers</strong><br />
<i>Ask Goast for changes to your application code. Goast will analyze your project and suggest code changes.<br />
<strong><a href="https://marketplace.visualstudio.com/items?itemName=goast-ai.goast"><img src="docs/images/download.png" alt="Download now!"/></a></strong></i><br>
</td>
</tr></table>

## goastVS

### Autopilot for software engineers

 Our AI-powered extension thinks like an engineer and writes code with a deep understanding of your entire project. 

![goastVS in action](https://uploads-ssl.webflow.com/64603153d90c23a771387a87/64e7e180bb3400e2d40ffb48_goastVS-clip.gif)

**Automatically find and fix bugs**
Prompt goastVS to fix bugs and resolve errors. Get reliable, accurate fixes.
 - "Fix the chat so it opens showing the newest message instead of the oldest."
- "I’m getting this error: Warning: Failed prop type: invalid prop ‘children’ supplied to ‘ForwardRef(Model)’... Fix it!"
- "There is an error using the modal in TokenModal. Fix it. This is the obfuscated stack trace: ..."


**Stand up projects in no time**
Instantly integrate external code without merge conflicts. Ask goastVS to help setup your backend infrastructure.
- "Package this app for a docker container."
- "Install the Material UI React framework to my app and add button components where necessary."
 - "Add Firebase Remote Config to this app and set default parameter values."


## Getting Started
Watch the Getting Started [video tutorial](https://youtu.be/-N1Hk6tRU0M?feature=shared)

Check out demos and tutorials on the [goast.ai Youtube Channel](https://www.youtube.com/@goast-ai/videos) 

By default, goastVS uses GPT-4 via the OpenAI API. You can change when the extension uses GPT-4 or GPT-3.5 in  Settings. We recommend using GPT-4 for better results. 

![enter image description here](https://uploads-ssl.webflow.com/64603153d90c23a771387a87/64e7ea402b2ceb25536d31ee_goastVS-example.png)


## Features

**Editing a Step**
For any generated step, you can click the edit button to change the filename and step instructions. If you do edit a step, the original filename and instructions will be saved and you can scroll between versions using the “</>” buttons under the chat avatar.

**View Diff**
Click the “View Diff” button to generate and view the code diff for any given step.

**Regen Diff**
Click “Regen Diff” to regenerate the code diff that you’re currently viewing. The tool does not save the original code diff when it is regenerated. When a step’s instructions are clear and simple, a regenerated code diff may the be same as the original diff.

**Feedback Icons**
Feedback helps us improve the model. Give a thumbs up if the tool generated a correct step with clear instructions and correct filename. If the tool generates an incorrect step, you can click the thumbs-down button and then send us more information about what went wrong.

**Delete Step**
Delete an unneeded step from the chat. This feature is located within each step’s menu.

**Clear Chat**
Clear all your prompts and any generated steps by clicking “Clear Chat” in the chat menu located at the top of the chat window.


## Settings

In the VS Code Settings window, search “goast” to display the following settings for the extension:

-   **OpenAI API Key:** Your developer key for OpenAI API access. This is needed for the tool to function.
-   **Use GPT4:** When toggled ON, the tool will use GPT4 for every request. This will increase cost and time to compute, but will generally give better results. When toggled OFF, the tool will use GPT3.5.
-   **Use GPT4 For Diff Generation:** When toggled ON, the tool will use GPT4 for Diff Generation only. This will increase cost and time to compute, but will generally give better results. GPT3.5 is used when toggled OFF (unless “Use GPT4” is on, which will override this toggle).
-   **Use GPT4 for Instruction Generation:** When toggled on, the tool will use GPT4 for step instruction generation. This will increase cost and time to compute, but will generally give better results. GPT3.5 is used when toggled OFF (unless “Use GPT4” is on, which will override this toggle).
-   **Ignore File Patterns:** A list of file patterns to exclude from the project description.
-   **Use Git Ignore:** Use the patterns in .gitignore files when excluding files.
-   **Maximum Search Depth:** The maximum depth of files to traverse when looking for relevant files. The larger the depth, the more likely important files will be included, but the cost and time could be significantly increased especially if Use GPT4 is enabled.  (Minimum: 0, Maximum: 5, Default: 2)


## Known Issues & Limitations

-   The tool is not very conversational at this point - as mentioned, it’s better at taking directives and generating steps to complete a task rather than explaining stuff or having conversations.
-   **There is no short-term memory within your chat.** Each prompt and resulting steps are siloed from your other prompts and steps.
-   You’ll get better results if your project is split into smaller files instead of a single file that houses all your code.
-   Like other AI coding tools on the market, goastVS will sometimes hallucinate or give results that aren’t quite right when it’s working in unfamiliar territory or doesn’t have enough context. We’ve found that even when the tool is a bit wrong, it still gets us moving in the right direction. That’s why we added the step editing functionality - so you can correct the tool when it’s wrong.
-   Error code 429 means you’ve hit your OpenAI API key’s cost limit for usage.

## Troubleshooting
[Join our Discord](https://discord.com/invite/MqqSZGETUb) for support! 
Or email support@goast.ai

## License

By downloading and using the goastVS extension, you agree to the [Privacy Policy](https://goast.ai/privacy) and [Terms of Service](https://goast.ai/terms).

Copyright © GOAST INC. All rights reserved.
