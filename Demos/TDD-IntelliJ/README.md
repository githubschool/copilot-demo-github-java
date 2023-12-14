# Test Driven Development (TDD) with Java through IntelliJ

**Test-Driven Development (TDD)** is a software develpment proces relying on software requirements being converted to test cases before software is fully developed. Since unit testing or any type of functional or performance testing is very important in Java development, TDD is highly encouraged among Java developers. Copilot is a great tool to help Java developers write unit tests for their Java code as it can helps to bootstrap a lot of repetitive code for unit tests.

As you can see in the picture below, the TDD process involves writing tests first, see if it fails (red), then write code to make the test pass (green). Copilot can help you write the test code and you can focus on writing the code to make the test pass.

![TDD](./images/tdd.jpg)

This demo is focusing around how to use Copilot to easily write unit tests for Java code. We will be using IntelliJ IDEA for this demo.

## Prerequisites

- [Installed IntellI IDEA](https://www.jetbrains.com/idea/download/)
- [GitHub Copilot Extension for IntellJ](https://plugins.jetbrains.com/plugin/17718-github-copilot)
- [Maven](https://maven.apache.org/download.cgi)
- [Download a sample project codes called TDDJava](./TDDJava)

[See this documentation on how to install Copilot extension for IntelliJ](/CopilotExtnsion4IntelliJ)

## Steps

Welcome! In this Copilot demo for **Test Driven Development (TDD) using IntelliJ**, you will start with a sample **Java + Maven** project that contains some starter code that can help you to implement TDD using Copilot.

### Step 1: Download a sample project

First, you need to download a sample project called [**TDDJava**](./TDDJava). This is a simple Java project that contains some starter code that can help you to implement TDD using Copilot.

### Step 2: Open the project in IntelliJ

Open the project in IntelliJ. You can open the project by clicking on **Open** in IntelliJ and selecting the **TDDJava** folder.

![Open Project](./images/1_OpenProject.jpg)

When you see a message like the one below, select **Trust Project**.

![Trust Project](./images/2_TrustProject.jpg)

### Step 3: Explore code and fix some structure

You can explore the code in the project. You can see that there is a Java class called `StringCalculator` under `src/main/java` and a sample unit test class called `StringCalculatorTest` under `src/test/java`. You can also see that there is a `pom.xml` file that contains the Maven configuration for this project.

![Explore Code](./images/3_GeneralProject.jpg)

You might need to configure Maven if you run into some problems building because the project requires a few dependencies like Junit. In addition, your test code `StringCalculatorTest` might not recognized as a Java file in some cases. If that is the case, please follow this optional step.

#### Optional: Convert a plain code to Java code

Select the file name `StringCalculatorTest` and while holding the control button, click on the file name. Then, select **Override File Type**.

![Convert to different file type](./images/4_OverrideFileType1.jpg)

Then, select **Java**.

![Convert to Java](./images/5_OverrideFileType2.jpg)

### Step 4: Fix Project Structure

You probably also need to fix the **Project Structure** by setting the right **Java Development Kit (JDK).** You can do that by clicking on **File** and selecting **Project Structure**.

![Project Structure](./images/6_ProjectStructureGoto.jpg)

Then, select **Project** and select the right **Project SDK**. 

![No SDK](./images/7_NoSDK.jpg)

In this case, I am using **Java 20 version 20.0.1**, but IntellJ also has an option to download JDK for you. You can click on **Download JDK** and select a correct version of JDK.

![Install SDK](./images/8_InstallSDK.jpg)

### Step 5: Test out first test and fix it

Now, you can run the test by right clicking on the test class `StringCalculatorTest` and selecting **Run 'StringCalculatorTest'**. Or, you can select an individual test function and run it by right clicking on the test function and selecting **Run 'add_TwoNumbers...'**.

![Run Test](./images/9_RunTest.jpg)

You will see that the test fails because the test is expecting the result to be 1504, but the actual result is 1500. What's going on? Well, let's find out!

![Test Fail](./images/10_FirstTestWillFail.jpg)

If you check the code in `StringCalculator` class, you will see that the `add` function just returns the first `number`. So, how do we fix this?

![Add Function incorrectness](./images/11_NeedToFix.jpg)

No worry! GitHub Copilot is smart enough to fix this right away by just making a space after number. However, it is still your job to make sure that the code is correct. After all, your are the main pilot, and Copilot is just your AI assistant.

![Copilot to the rescue](./images/12_SuggestionCopilot.jpg)

After you take the suggestion, let's go back and run the test again. You can run the test by right clicking on the test class `StringCalculatorTest` and selecting **Run 'StringCalculatorTest'**. And it is successful this time! We just went from a failure to a success. That is a great progress!

![Test Success](./images/13_MakeSuccessfulFirst.jpg)

### Step 6: Adding a second test function called concatenateTwoStrings

Now, we will implement a second test function called `concatenateTwoStrings` that will concatenate two Strings. You can do that by adding a new test function in the `StringCalculatorTest` class. After making new lines, just add `@Test`, and your Copilot is giving you some suggestions. 

![Add a second test](./images/14_AddSecondTest.jpg)

However, that is not what we want. Let's override by typing a test function name that reflects what we really want to do. In this case, we want to concatenate two Strings. So, let's type `concatenateTwoStringsAbrahamLincoln`, and Copilot will give you some suggestions.

![Override test function name](./images/15_OverrideSecondTest.jpg)

Once we accept the generated code, we have a few options. IntelliJ does have a built-in feature to generate the code based on function name, etc, like this.

![IntelliJ built-in feature](./images/16_IntelliJHasOption.jpg)

But, we want to focus on Copilot driven development. So, let's go to `StringCalculator` class and implement the function. As soon as you type, it will give you a suggestion for the function name by cross-referencing what you typed in `StringCalculatorTest` class.

![Suggestion for function name](./images/17_CopilotAddSecondFunction.jpg)

Run the test again, and it will become successful! Great job.

![Pass second test](./images/18_PassSecondTest.jpg)

### Step 7: Last exercise for implementing a third test function called findLargestNumberFromList

We could stop there, but let's do one more exercise. We can implement a unit test and a method to find the largest number from a provided list. We start typing a test function name in the `StringCalculatorTest` class.

![Add a third test](./images/19_AddThirdTest.jpg)

Once we are happy with what Copilot suggests, we can accept the solution. Just like last time, let's go create this function in the `StringCalculator` class.

![Implement a third test](./images/20_NeedToAddThird.jpg)

Although this is a slightly more complex function, Copilot really makes this super easy. Just look at how fast it can generate the result.

![Copilot got it](./images/21_AddingThirdFunction.jpg)

Let's accept the solution.

![Accept the solution](./images/22_CompleteThirdFunction.jpg)

Now, let's run the test again. And it is successful! Congratulations! You just finished Test Driven Development using GitHub Copilot.

![Test Success](./images/23_PassThirdTest.jpg)






