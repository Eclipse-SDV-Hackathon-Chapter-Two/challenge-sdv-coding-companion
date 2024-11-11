# Challenge: SDV Coding Companion

Welcome to the SDV Coding Companion Hackathon challenge! This guide will walk you through accessing your free AWS credits, setting up your project, and building a GenAI model on AWS Bedrock. Follow each step to make the most of your AWS Bedrock credits and successfully develop your project.

---

## How to Access Your Free AWS Credits

1. **Access the Registration Page**
   - Visit [genai.digital.auto](http://genai.digital.auto/).
   - Register a new account and log in. Logging in with a GitHub account is also available.
     <img src="./fig/onboarding.png" alt="onboarding" style="width: 80%; height: auto;">
2. **Complete Your Team Information**
   - Enter your team details. Ensure all team members (up to 5) have registered accounts.
     <img src="./fig/register-team.png" alt="register-team" style="width: 80%; height: auto;">
3. **Apply for AWS Bedrock Credits**
   - Provide a clear description of your project idea to apply for AWS credits.
     <img src="./fig/apply-credits.png" alt="apply-creditsg" style="width: 80%; height: auto;">
   - Submit your application and wait for approval, which may take some time.
   - <img src="./fig/waiting-for-approval.png" alt="waiting-for-approval" style="width: 80%; height: auto;">

4. **Review Your Team’s AWS Credentials**
   - Once approved, your IAM user credentials and password will be available.
     <img src="./fig/review-team.png" alt="review-team" style="width: 80%; height: auto;">
   - **Note:** Access keys provided here cannot be used for direct AWS API calls due to security restrictions. They are exclusively for submitting your GenAI.

---

## How to Access the AWS Bedrock Console

1. **Log in to AWS**
   - Copy your IAM user credentials and password, then click "Open AWS Bedrock."
   - Enter your IAM username and password, then sign in.
     
     <img src="./fig/fill-username-password.png" alt="fill-username-password" style="width: 80%; height: auto;">

2. **Navigate to the AWS Bedrock Console**
   - Use the search bar to find "AWS Bedrock," then access the Bedrock Console.
      <img src="./fig/search-bedrock.png" alt="search-bedrock" style="width: 80%; height: auto;">
3. **Set Your Region**
   - Change the AWS region to **US East (N. Virginia) - us-east-1** to ensure access to all available LLM models.
      <img src="./fig/bedrock-console.png" alt="bedrock-console" style="width: 80%; height: auto;">

---

## Building Your GenAI Model on Bedrock

1. **Access the Playground**
   - In the AWS Bedrock Console, navigate to the **Playground/Chat** section to begin experimenting.
     <img src="./fig/playground-chat.jpg" alt="playground-chat" style="width: 80%; height: auto;">
2. **Choose Your Model**
   - Select a provider and model, then click “apply” to return to the Playground chat interface.
     <img src="./fig/select-model.jpg" alt="select-model" style="width: 80%; height: auto;">
      <img src="./fig/apply-model.jpg" alt="apply-model" style="width: 80%; height: auto;">
3. **Experiment with a Simple Prompt**
   - Try entering a prompt such as: “Generate an SDV Python code to open the driver’s door.”
     <img src="./fig/input-prompt.jpg" alt="input-prompt" style="width: 80%; height: auto;">
     <img src="./fig/general-result.jpg" alt="general-result" style="width: 80%; height: auto;">
   - Note that the initial output may include extra comments—adjustments are often needed to refine the response.

4. **Refining Model Responses with System Messages**
   - Use “system messages” to provide context and instructions for the model, improving accuracy and relevance. Below are example system messages to use as templates (do not copy them directly):
     - [GenAI Python Template](https://bewebstudio.digitalauto.tech/data/projects/alSxlS1Qkf20/GenAI_Python.md)
     - [GenAI Dashboard Template](https://bewebstudio.digitalauto.tech/data/projects/alSxlS1Qkf20/GenAI_Dashboard.md)
     - [GenAI Widget Template](https://bewebstudio.digitalauto.tech/data/projects/alSxlS1Qkf20/GenAI_Widget.md)
      <img src="./fig/system-message.jpg" alt="system-message" style="width: 80%; height: auto;">
   - **Tip:** Use these templates as a base. Under “Instruction,” enter general guidelines, and under “Requirement,” place specific requests for your project’s needs. Once you identify an effective instruction or system message, save it and consider submitting it to [marketplace.digitalauto.tech](https://marketplace.digitalauto.tech) for public use.
5. **Testing the Refined Code**
   - After adding instructions, the output should contain only the code, optimized for the Playground environment.
     <img src="./fig/pure-code.jpg" alt="pure-code" style="width: 80%; height: auto;">
   - Paste the code into the **Code** tab, run the prototype, and observe any API value changes.
     <img src="./fig/code-test.jpg" alt="code-test" style="width: 80%; height: auto;">
     <img src="./fig/code-test2.jpg" alt="code-test2" style="width: 80%; height: auto;">
6. **Enhance with Widgets**
   - To visualize API values more effectively, add widgets to your prototype. If you are new to the Playground, start by building a basic prototype for hands-on practice.

---

## How to Submit Your GenAI Model

1. **Access the Marketplace**
   - From the previous **Review Your Team** screen, click "Go to marketplace," or directly visit [https://marketplace.digital.auto](https://marketplace.digital.auto).

2. **Log In**
   - If you’ve previously logged into the GenAI website, your login should carry over. If you are not logged in, please use the same account you registered with.

3. **Add a New Package**
   - Click **Add Package** to create a new submission.
     
      <img src="./fig/add-package.png" alt="add-package" style="width: 80%; height: auto;">
1. **Fill in the Package Information**
   - **Basic Information:** Include a package name, short description, and detailed description. Set visibility to **Public**.
   -   <img src="./fig/basic-info.png" alt="basic-info" style="width: 80%; height: auto;">
   - **Category:** Select **GenAI** and choose the corresponding type of GenAI model.
   - **Credentials and Config:** Copy these from the **Review Your Team** screen from the previous step. For endpoint URL, follow the syntax provided below.

     **Endpoint URL Syntax:**
     ```
     https://bedrock-runtime.us-east-1.amazonaws.com/model/<model_id>/invoke-with-response-stream
     ```
     For model-specific details, refer to [AWS documentation](https://docs.aws.amazon.com/bedrock/latest/userguide/model-ids.html#model-ids-arns).  
     Example: If you’re using the Claude 3 Sonnet model:
     ```
     https://bedrock-runtime.us-east-1.amazonaws.com/model/anthropic.claude-3-sonnet-20240229-v1:0/invoke-with-response-stream
     ```
     <img src="./fig/fill-credentials-and-config.png" alt="fill-credentials-and-config" style="width: 80%; height: auto;">
   - **Add Images:** Upload a **Package Icon**, **Package Cover**, and **Feature Images** (at least one required for feature images).

2. **Submit Your GenAI**
   - Once you’ve filled in all the information, click **Submit** to submit your GenAI.

3. **View Your Submissions**
   - To view all your submissions, click on the **My Package** tab in the website header.

**Note:** To submit another GenAI model, start over from step 1.

---

## How to Update Your GenAI Model

1. **Access the Marketplace**
   - Navigate to **My Package** on marketplace.digital.auto after logging in.
     <img src="./fig/navigate-package.jpg" alt="navigate-package" style="width: 80%; height: auto;">
2. **Select Your GenAI Package**
   - Find and select the GenAI package you wish to update.

3. **Update the Package**
   - Click the **Update** button to modify your submission.
     
      <img src="./fig/update-package.jpg" alt="update-package" style="width: 80%; height: auto;">
4. **Adjust the Deployment URL, Credentials, and Instructions**
   - Make necessary changes to your endpoint URL, credentials, and system instructions, then save the updated package.

     <img src="./fig/deployment-adjust.jpg" alt="deployment-adjust" style="width: 80%; height: auto;">
---

## How to Use GenAI on the Playground

### 1. **SDV ProtoPilot (GenAI Python)**

- Click on the **SDV ProtoPilot** button.

  <img src="./fig/sdv-protopilot.png" alt="sdv-protopilot" style="width: 80%; height: auto;">
- Enter your input prompt and select a generator.

  <img src="./fig/sdv-protopilot-prompt.png" alt="sdv-protopilot-prompt" style="width: 80%; height: auto;">
- Choose a generator from the marketplace. Your own generator will appear once approved by the admin.
- Click **Generate** and wait 30-90 seconds for the code to be generated. The time may vary depending on model training.

  <img src="./fig/sdv-protopilot-result.png" alt="sdv-protopilot-result" style="width: 80%; height: auto;">
- If you are satisfied with the generated code, click **Add new generated code**.
  
  <img src="./fig/sdv-protopilot-add.png" alt="sdv-protopilot-add" style="width: 80%; height: auto;">
  

### 2. **Dashboard ProtoPilot (GenAI Dashboard)**

- Go to the **Dashboard Config** tab and click the **Dashboard ProtoPilot** button.
    <img src="./fig/dashboard-config.png" alt="dashboard-config" style="width: 80%; height: auto;">
- Select a generator from the marketplace. Your own generator will appear once approved by the admin.
    <img src="./fig/select-generator.png" alt="select-generator" style="width: 80%; height: auto;">
- Enter your input prompt and click **Generate**. Wait for the dashboard to be generated.
    <img src="./fig/input-prompt.png" alt="input-prompt" style="width: 80%; height: auto;">
- Once generated, you’ll see the dashboard configuration. Click **View Dashboard** to view the raw configuration.
  <img src="./fig/view-dashboard.png" alt="view-dashboard" style="width: 80%; height: auto;">
- If satisfied, click **Add new dashboard config** to add it.

  <img src="./fig/add-config.png" alt="add-config" style="width: 80%; height: auto;">

### 3. **Widget ProtoPilot (GenAI Widget)**

- Go to the **Dashboard Config** tab and add a widget by clicking the **Widget ProtoPilot** button.
  <img src="./fig/add-widget.png" alt="add-widget" style="width: 80%; height: auto;">
- Select a generator from the marketplace. Your own generator will be displayed once approved.
    <img src="./fig/widget-generator.png" alt="widget-generator" style="width: 80%; height: auto;">
- Enter your prompt and click **Generate**. Wait for the widget to be generated.
   <img src="./fig/input-widget-prompt.png" alt="add-widget" style="width: 80%; height: auto;">
- After it’s generated, you can preview it embedded in an iframe. If it meets your expectations, click **Add Widget** to add it to your selected dashboard box.

  <img src="./fig/add-widget-to-dash.png" alt="add-widget-to-dash" style="width: 80%; height: auto;">
- To view or modify the widget code, hover over the widget box and click the icon linking to **Widget Studio**. You can edit the HTML, CSS, and JavaScript of the widget.

  <img src="./fig/widget-studio1.png" alt="widget-studio1" style="width: 80%; height: auto;">
  <img src="./fig/widget-studio2.png" alt="widget-studio2" style="width: 80%; height: auto;">

### 4. **How Playground Handles GenAI Responses**

When interacting with GenAI models via the Playground, responses are structured for effective processing and presentation across different platforms, including Amazon Bedrock.

- **HTTP POST Method:** Requests to your model’s endpoint will include user input (and optionally system messages) for secure and structured communication.
- **AWS Bedrock Models:** Requests sent to Bedrock will return responses in a specific JSON format. This ensures smooth integration with the Playground system.

---

Good luck with your Hackathon project! Experiment, iterate, and take full advantage of the tools and templates available.
