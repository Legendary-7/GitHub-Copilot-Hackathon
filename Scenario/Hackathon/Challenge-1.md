# Challenge 1: Getting Started with GitHub Copilot

### Estimated Time: 45 minutes

## Introduction

As a software developer at **Contoso Ltd.**, a leading software development company, you are tasked with researching and implementing innovative tools and technologies to enhance the company's coding process and productivity. The company is particularly interested in solutions that can improve code efficiency, streamline the development process, and enhance collaboration among its globally distributed teams.

**Contoso Ltd.** has identified **GitHub Copilot**, an AI-powered coding assistant, as a potential solution and enrolled you in a challenge series to explore and understand its capabilities. Your mission is to get started with **GitHub Copilot**, setting it up in your coding environment, exploring its features, and using it for code generation and suggestions. **GitHub Copilot** is a groundbreaking AI-powered coding companion seamlessly integrated into **Visual Studio Code**, designed to enhance your coding experience. By leveraging machine learning, Copilot assists developers in crafting code by intelligently suggesting completions and generating contextually relevant code snippets.

Imagine navigating a complex coding project and encountering puzzles that demand meticulous attention to detail. **GitHub Copilot** steps in as your coding ally, offering insightful suggestions and autocompletion tailored to the coding context. This not only boosts coding efficiency but also serves as a valuable learning tool, providing a deeper understanding of coding structures and patterns.

You will experiment with **GitHub Copilot** in various coding scenarios, such as creating a Python/JavaScript-based calculator and an application that fetches weather data from APIs. You will also leverage GitHub Copilot to refactor given code snippets and debug intentionally flawed code, thereby understanding the process of code improvement and effective debugging. Moreover, you will explore the integration of **GitHub Copilot** with GitHub Codespaces, a feature that extends the collaborative potential of your coding environment. This will allow you to understand how Copilot can be utilized in a collaborative coding environment, enabling teams to work seamlessly on projects regardless of geographical boundaries.

In this challenge series, you'll dive into **GitHub Copilot's** capabilities, starting with the setup and exploration of its features. From collaborative coding with GitHub Codespaces to experimenting with Copilot's suggestions and creating code for various tasks, you'll embark on a journey to harness the full potential of this revolutionary coding assistant. By the end of this challenge, you aim to demonstrate how **GitHub Copilot** can be effectively used to enhance coding productivity, improve code quality, and streamline the software development process at **Contoso Ltd**.

## Prerequisites

Make sure you have the following from the CloudLabs-provided integrated environment:

> **Note**: Prerequisites are already set up in the CloudLabs provided environment. If you're using your personal computer or laptop, please make sure that all necessary prerequisites are installed to complete this hackathon.

- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub account](https://github.com/)
- Python and NodeJs modules are installed in your Lab-VM in the directory **C:\Program Files**.

## Login to GitHub

1. In the LABVM desktop search for **Microsoft Edge** **(1)**, click on **Microsoft Edge** **(2)** browser.

   ![](../../media/Edge.png)

1. Navigate to GitHub login page using the provided URL below:
   ```
   https://github.com/login
   ```
   
1. On the **Sign in to GitHub** tab, you will see the login screen. In that screen, enter the following **email** **(1)** and **password** **(2)**. Then click on **Sign in** **(3)**. 

   >**Note**: To get GitHub credentials navigate to the **Environment Details** tab and click on the **GitHub Credentials** option to view the key-value pairs of the **GitHub UserEmail**, and **GitHub Password**. You can use the copy buttons under the actions column to have the values copied instantly. Alternatively, it is suggested to have the values copied over onto a notepad for easy accessibility. 
   
   ![](../../media/github-login.png)
          
1. Next, to get the authentication code, sign in to Outlook (https://outlook.office365.com/mail/) with the git credentials within the Environment tab from the previous step. Once you have logged into Outlook, find the recent email containing the verification code. Enter the verification code, and click on **Verify**.

   >**Note:** The email containing the verification code can somtimes creep into the archive/spam folders within your Outlook.

   ![](../../media/authgit.png)

## Challenge Objectives:

1. **Setup GitHub Copilot in VS Code:**
   - Install the GitHub Copilot extension from the VS Code Marketplace.
   - Configure the extension settings to suit your preferences.

   <validation step="afc73673-26ad-4c49-b013-4632e09d8634" />

2. **Login with a GitHub account:**
   - Login to GitHub within Visual Studio Code using the provided GitHub credentials. You can find these credentials under **Environment > GitHub Credentials** tab.
   - On the GitHub sign-in page, enter your GitHub credentials and click on **Sign in**.
   - To verify your GitHub account login, sign in to **Outlook** in the Lab VM through in a Private window (https://outlook.office365.com/mail/) using your GitHub credentials, locate the email containing the verification code, and select **Verify**.
   - Click on Authorize Visual-Studio-Code to provide additional permissions to GitHub for VS Code.

3. **Using GitHub Codespaces with Copilot:**
   - Create a Codespace for your GitHub repository.
     >**Note:** Navigate to **https://github.com/CloudLabsAI-Azure/MyMvcApp-Contact-Databse-Application** repository and fork this repository into the CloudLabs-provided GitHub account to create a new codespace. You will use this repository in Challenge 02.
   - Understand how Copilot can be utilized in a collaborative coding environment.
   - Use the GitHub Codespaces to push/commit the local files from VS Code to GitHub in the next challenges.

4. **Explore GitHub Copilot Features:**
   - Experiment with Copilot in various coding scenarios.
   - Use Copilot's suggestions to speed up your code-writing process.
     >**Hint:** Access the GitHub Copilot Suggestions window by **Ctrl+Enter** shortcut in your VS Code.

5. **Code Generation with Copilot and Copilot Chat:**
   - Create Python/JS-based code to build a calculator.
      - Utilize GitHub Copilot to generate Python or JavaScript code that creates a basic calculator.
      - Save the files as *calculator.py / calculator.js* at **C:\Users\azureuser**.
      - Experiment with different mathematical operations and user interactions.
   - Create a Python/JS-based app to get weather data from OpenWeatherMap APIs.
      - Sign up for the OpenWeatherMap website (https://openweathermap.org/).
      - Leverage Copilot to generate Python/JS code that interacts with weather APIs to retrieve weather data.
      - Save the files as *weather_script.py / weather_script.js* at **C:\Users\azureuser**.

   <validation step="b5244888-2b42-4686-b326-465182a86561" />

6. **Code Refactoring & Debugging:**
   - Refactor given code snippets using Copilot, understanding the process of code improvement.
     >**Hint:** Utilize GitHub Copilot's **Refactor** feature.

      ```
      #A poorly written example of a program in Python. It prompts the user for the number of elements to sum, takes those integers as input, and handles some basic error cases
      
      MAX = 100

      def calculate_sum(arr):
         result = 0
         for num in arr:
            result += num
         return result

      def main():
         try:
            n = int(input("Enter the number of elements (1-100): "))
            if not 1 <= n <= MAX:
                  print("Invalid input. Please provide a digit ranging from 1 to 100.")
                  exit(1)

            arr = []

            print(f"Enter {n} integers:")
            for _ in range(n):
                  try:
                     arr.append(int(input()))
                  except ValueError:
                     print("Invalid input. Please enter valid integers.")
                     exit(1)

            total = calculate_sum(arr)

            print("Sum of the numbers:", total)

         except KeyboardInterrupt:
            print("\nProgram terminated by user.")
            exit(1)

      if __name__ == "__main__":
         main()
      ```
   - Debug code effectively with Copilot's assistance, addressing and fixing identified issues.
     >**Hint:** Utilize GitHub Copilot's **Fix** feature.

      ```
      # Intentionally flawed Python program

      # importing modules
      import itertools, random

      # make a deck of cards
      deck = list(itertools.product(range(1,14),['Spade','Heart','Diamond','Club'])

      # shuffle the cards
      random.shuffle(deck)

      # draw five cards
      print("You got:")
      for i in range(5)
         print(deck[i][0], "of", deck[i][1]

      ```

## Success Criteria:

- Verify that GitHub Copilot is successfully installed and configured in Visual Studio Code and logged in.
- Successfully explored GitHub Codespaces integration and understood its collaboration features.
- Successfully tried out Copilot in coding scenarios, experiencing its code generation capabilities.
- Verify that Python/JS code for a calculator and an app to get weather data using Copilot were created and run successfully.
- Verify that your chosen piece of code is refactored successfully, with improved readability and overall quality.
- Verify that a piece of code with intentional errors is fixed successfully using Copilot's suggestions.

## Additional Resources:

- [GitHub Copilot Documentation](https://github.com/github/copilot-docs)
- [GitHub Codespaces Documentation](https://docs.github.com/en/codespaces)

### Conclusion

In this challenge, you successfully set up GitHub Copilot in Visual Studio Code, configured extension settings, and logged in with your GitHub account. You were also successful in creating Python/JS code for a calculator and an app to fetch weather data from OpenWeatherMap APIs. Additionally, you refined your coding skills by refactoring code snippets and debugging with Copilot's assistance.
