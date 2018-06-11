Title: Minimum PyCharm configuration to run pytest
Slug: First Post
Category: Python
Tags: Python, PyCharm, Pytest setup
Date: 2018-06-06
Modified: 2018-06-06
Author: Abhishake Gupta

## Background 

[PyCharm 2017.3.5](https://www.jetbrains.com/help/pycharm/2017.3/meet-pycharm.html?top=&utm_medium=help_link&utm_source=from_product&utm_campaign=PC&utm_content=2017.3) is a dedicated Python and Django IDE providing a wide range of essential tools for Python developers,
 tightly integrated together to create a convenient environment for productive Python development and Web development.

[pytest](http://pytest.org/) Starting to test your project with py.test is very easy. This is because there is very little boiler plate code required in your tests. It may be quick to start testing with py.test but it is far from a basic library. It has a full set of tools and testing capabilities when you need them. The traceback reporting is fantastic, it has really effective test collection and execution, test skipping and the ability to write parameterised tests.
 For more information see the py.test web site [here]((http://pytest.org/))

## What this post is about !!
This post will focus on the settings to be made in pycharm so a developer could run its test cases in just one click 
and generate a report of how many lines of the actual code is being covered by the test cases.

### Steps to follow:

1. **Make `tests` folder in the current project directory:**
Let's say my project name is `ab_calculator`, then create a `tests` directory in which 
the test cases would be written for the calculator app.

2. **Set the Project Interpreter:**
Go to `File -> Settings -> Project:[] -> Project Interpreter`
you may use any of the available python interpreters or can add an existing virtual/conda environment interpreter.
(Make sure the interprter is locally available on your system)
Click on `Apply`

3. **Set the Project Structure:**
Go to `File -> Settings -> Project:[] -> Project Structure`
Click on the Add Content Root and add the directories that contain your code and tests both.
(They could be network mount drives as well.)  
Click on `Apply`

4. **Set Default Test Runner:**
Go to `File -> Settings -> Tools -> Python Integrated tools`
set Default Test Runner as pytest.
Click on `Apply`

5. **Set configurations for the current script:**

Go to `Run -> Edit configurations -> Defaults`
    
* **Set interpreter** (optional)
    Under `Defaults` click on `Python`
    and choose the interpreter from available interpreters specific for this script.
    and in working directory provide the path for the current project.
    Set `environment variables` if any specific to the project.
    
* **Set tests**
    Under `Defaults` click on `Python Tests`
    click `python` and choose the interpreter from available interpreters specific for this script.
    and in working directory provide the path for the `tests` directory of the current project.
    Set `environment variables` if any specific to the project.

* **Add pytest in tests**
    In the top menu click the `+` symbol, then `python tests`
    on this page Add the `Name: pytest in tests` and check the python interpreter and working directory, it should be same as the directories set above.   


## References below:
1. [Stack Overflow: How to configure pycharm for pytest](https://stackoverflow.com/questions/6397063/how-do-i-configure-pycharm-to-run-py-test-tests)
2. [Why to use pytest](http://halfcooked.com/presentations/pyconau2013/why_I_use_pytest.html)


