
<!--
Copyright © GOAST INC.
All rights reserved.
-->

# goastVS: Your AI Text-to-Diff Coding Assistant

<table style="width: 100%; border-style: none;"><tr>
<td style="width: 140px; text-align: center;"><a href="https://marketplace.visualstudio.com/items?itemName=goast-ai.goast"><img width="128px" src="docs/images/goast.png" alt="Goast logo"/></a></td>
<td>
<strong>Your AI powered Text-to-Diff Coding Assistant</strong><br />
<i>Ask Goast for changes to your application code. Goast will analyze your project and suggest code changes.<br />
<strong><a href="https://marketplace.visualstudio.com/items?itemName=goast-ai.goast"><img src="docs/images/download.png" alt="Download now!"/></a></strong></i><br>
</td>
</tr></table>

goastVS is a VS Code extension built by [goast.ai](https://goast.ai) - a company that’s using LLM technology to automate coding tasks so you can focus on building great software.

Prompt the tool to fix bugs, integrate external libraries, and automate coding tasks right in VS Code. The model will output a series of steps that satisfy the prompt. From there a single click will generate reliable, accurate code diffs for each step.

## Become a Beta Tester and get free tokens!!

We are searching for beta testers who are currently working on a project and would like to use goastVS. If you’re interested, send an email to [support@goast.ai](mailto:support@goast.ai) telling us what you’re working on. We will select a handful of users and provide them with an OpenAI API key with $10 in tokens to use with the extension.

## Getting Started

Step 1: Add the extension to VS Code.

Step 2: Click the goast icon from the side nav.

Step 3: Add your OpenAI API key to the input provided. If you want to change this later just search “goast” in the VS Code Settings window and change the API key in the corresponding input.

Step 4: After you API key has been added, click “RUN GOAST”. This will generate a description of your app based on the relevant files in your codebase.

Step 5: From there you can start prompting the tool to perform coding tasks. For each prompt, the tool will generate a series of steps needed to complete the task. For code-specific steps, you’ll have the option to generate a code diff by clicking “View Diff.” For non code-specific tasks, you may need to complete a task manually outside of VS Code (like creating a Docker account, for example, or initializing a Firebase project.)

## Best Practices

Better prompts generate better results. Being specific about what you want to achieve will yield more detailed steps and more accurate code diffs.

-   Instead of asking the bot “why isn’t something working?” give it a directive. You’ll get better results if you actually tell the bot to do something, like “I’m seeing *this*, but I want it to do *that*.”
-   For best results, install the VS Code extensions for any languages that your project is using. This helps the model understand any references between files.
- The tool works best when your project is split into smaller files instead of a single file that houses all your code.

## Demos

Fixing a scrolling bug: [https://youtu.be/u4qjUB5ZbIk](https://youtu.be/u4qjUB5ZbIk)

Adding Atomic Increment for Request to our Firestore Database: [https://youtu.be/RrpvO9KYnJU](https://youtu.be/RrpvO9KYnJU)

Adding a loading icon: [https://youtu.be/OS5Jt8sMb94](https://youtu.be/OS5Jt8sMb94)

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

## Get Support

If you’re experiencing issues with the extension, feel free to reach out to [support@goast.ai](mailto:support@goast.ai) and we’ll try our best to help solve your problem.

## License

By downloading and using the goastVS extension, you agree to the Privacy Policy and Terms of Service which can be found at www.goast.ai.

License for this repository:

Copyright © GOAST INC. All rights reserved.
