# Quality Assurance & Testing 🪳

## Introduction
In the world of software development, ensuring that your application functions as intended is not just beneficial—it's crucial. Quality Assurance (QA) and Testing are the safeguards that help maintain the integrity, performance, and reliability of your application.

## Functional Testing vs Non-functional Testing
The major difference between these categories of Software Testing is that Functional Testing tests the functionality of a software product while non-functional testing concentrates on performance and security.

### Functional Testing
- Unit testing
- API testing
- UI testing
- Integration testing
- Regression testing
- Compatibility testing with different devices and platforms
- End-to-end testing

### Non-Functional Testing
- Security testing
- Performance testing

## Benefits of QA Testing
QA testing provides numerous benefits, including:

- **Improved software quality**: Identifies and eliminates defects, ensuring the software meets required quality standards.
- **Reduced risk**: Minimizes the risk of software failures, downtime, and reputational damage.
- **Increased user satisfaction**: Ensures the software meets the requirements and expectations of end-users.
- **Cost savings**: Reduces the cost of software maintenance and support by identifying and fixing issues early on.

By understanding the importance of QA testing and following best practices, you can ensure the quality and reliability of your software products or services, leading to increased user satisfaction and business success.

## Types of QA Testing

![](assets/api-testing.gif)

[Source](https://blog.bytebytego.com/p/ep83-explaining-9-types-of-api-testing)

There are various types of QA testing, including:
<!-- TODO: provide how-to guides -->
- **Smoke Testing**: Verifies critical functionalities and identifies show-stopper issues.
- **Manual Testing**: Traditional method of testing, often used for complex or creative testing scenarios.
- **Automation Testing**: Uses software tools (like [Selenium](https://www.selenium.dev/)) to execute tests and reduce testing time and effort.
- **Regression Testing**: Verifies that changes or fixes did not introduce new defects or affect existing functionality.
- **Integration Testing**: Tests how different components or systems interact with each other.
- **System Testing**: Tests the entire software system, including all its components and interactions.
- **User Acceptance Testing (UAT)**: Verifies that the software meets the requirements and expectations of the end-users. (sometimes called "beta" testing)

<!-- 
### Performance Testing
Ensure your application performs well under stress and high traffic by using tools like:

- [New Relic](https://newrelic.com/): Monitors and tunes the performance of your application.
- [JMeter](https://jmeter.apache.org/): Tests performance both on static and dynamic resources. 
-->


## Best Practices for QA Testing

To ensure the effectiveness of QA testing, follow these best practices:

- **Plan and prioritize testing**: Identify critical test cases and prioritize them based on risk and business impact.
- **Use automation testing**: Leverage automation testing to reduce testing time and effort.
- **Involve stakeholders**: Involve stakeholders, including developers, product managers, and end-users, in the testing process.
- **Continuously test and iterate**: Continuously test and iterate throughout the development process to ensure the software meets the required quality standards.

## The QA process
A good QA process checks whether the product meets your specifications and needs. While software testing can vary slightly depending on the company’s practices, the main stages remain the same:

- **Analysis of Requirements**: QA analysts review and analyze the specific requirements of a project. They develop clarity on the parameters of their involvement. Analyzing requirements is crucial as it sets the framework for effective and executable quality control.

<aside>
Creating a Functional Specification document is critical. It guides both developers and QA teams on what needs to be tested and assures that all features work as intended. This document should detail:

- **User Stories**: What the user can do with the application.
- **Expected Behaviors**: How the application should behave under various conditions.
- **Edge Cases**: Special cases or unusual conditions that need handling.
</aside>

- **Planning**: QA professionals start the test planning phase once they have a good understanding of project requirements. They must define the scope of their work and come up with a testing strategy specific to the project. Planning also involves laying out the QA approach for each stage of the software engineering cycle, the type of testing called for, and the tools required.
- **Test Case Development**: A test case is a combination of actions that must be performed on a system to ensure it functions correctly. It ensures that separate features within software fall within applicable guidelines and standards. Test case development sets out step-by-step processes for each testing sequence and includes checklists for both manual and automated testing methods.
- **Test Execution**: This is the process of executing the prepared test cases and determining the differences between expected and actual results. It involves capturing test results and reporting bugs, errors, and other problems. QA testers create additional sub-tests to test these issues. Final test results are brought before the team members for further action.
- **Verification**: This involves retesting the product once the development team has fixed all issues brought up in the test execution stage. Verification involves regression testing and analysis, where QA testers check if identified bugs have been successfully resolved and whether new bugs have appeared. The verification process ensures the optimal functionality of the product.
- **Documentation and Reporting**: This stage involves preparing a document outlining all tests conducted during the product development cycle, along with their results. It provides detailed insights into the number and nature of errors and anomalies detected. The document lists the entire chronology of the testing process and can be used to reinforce future product testing cycles.

## End-to-End Testing
End-to-end testing (E2E testing) is the process of testing a piece of software from start to finish as it will be used by the actual users. For a web application, you would start a browser, navigate to the correct URL, use the application as intended, and verify the behavior. This usually happens in a staging or test environment before going into production.

### Practical steps to get started with E2E testing
1. Identify test scenarios
2. Map the steps in each scenario
3. Use the mapped steps to perform manual testing
4. Automate the tests
5. Add your tests to the CI pipeline

Get together with business owners, developers, and testers and think about some scenarios that you want to test before every release. This doesn’t have to be an exhaustive list. It’s better to have a minimal set running first, and then expand on it later.

### End-to-End Testing Example
Here’s an example of a (manual) E2E test:

1. Go to https://demoblaze.com.
2. Click on the first product (the Samsung Galaxy s6 phone, with a price of $360.)
3. On the product’s page, ensure the name and the price of the product are correct.
4. Then, click on the “Add to cart” button.
5. Ensure you see an alert with the message “Product added.”
6. Click on the “Cart” link, in the main navigation menu.
7. Ensure the cart has a single product with the correct info, and the total is $360.
8. Finally, click on the “Delete” link and verify whether the product got deleted.

This is a simple test case for testing whether the cart functionality of an e-commerce site works as intended. With a test automation tool, you could automate this test to prevent future regressions.

## Automated vs Manual Testing

tldr; you should automate every test that you can, and manually test what you can't automate.

### Manual Testing
- Cost depends on human resources deployed in testing.
- Slower and prone to human errors.
- Not suited for many types of testing (like stress testing).
- Hard to test complex cases manually.
- Good for finding visual or UX bugs.

### Automated Testing
- More reliable and quicker than manual testing.
- Increases the development team’s productivity (quicker feedback).
- Allows for different, complex types of testing.
- Improves project quality.
- Doesn’t find visual or UX bugs.

### Automated Tests Can Save You From Regressions
Software applications are susceptible to regressions. There’s no way to have confidence in the quality of your app unless you completely test it after each change.


## Example End to End Test Plan

```md
### Objective
The objective of this end-to-end test plan is to ensure that the application functions as expected from start to finish, covering all the necessary steps and interactions.

### Scope
This test plan covers the entire application workflow, from user login to the final result.

### Test Environment
- **Hardware**: [Specify the hardware requirements, e.g., laptop, desktop, mobile device]
- **Software**: [Specify the software requirements, e.g., operating system, browser]
- **Network**: [Specify the network requirements, e.g., internet connection]

### Test Cases

#### Login Test
- Step 1: Enter valid username and password
- Step 2: Verify successful login
- Step 3: Verify access to restricted areas

#### Search Test
- Step 1: Enter search query
- Step 2: Verify search results
- Step 3: Verify search filters

#### Product Details Test
- Step 1: View product details
- Step 2: Verify product information
- Step 3: Verify product images

#### Add to Cart Test
- Step 1: Add product to cart
- Step 2: Verify cart contents
- Step 3: Verify cart total

#### Checkout Test
- Step 1: Proceed to checkout
- Step 2: Verify checkout process
- Step 3: Verify order confirmation

#### Order History Test
- Step 1: View order history
- Step 2: Verify order details
- Step 3: Verify order status

### Test Data
- Valid username and password
- Search queries
- Product information
- Cart contents
- Order details

### Test Environment Setup
- Set up the test environment according to the specified requirements
- Ensure all necessary software and hardware are installed and configured correctly
- Ensure a stable internet connection

### Test Execution
- Execute each test case in the order listed
- Verify each step and result
- Document any issues or defects found

### Test Reporting
- Document all test results, including pass/fail status
- Identify any defects or issues found during testing
- Provide recommendations for improvement

### Test Schedule
[Insert test schedule, including start and end dates, and test duration]

### Test Resources
[Insert test team members, including their roles and responsibilities]
[Insert any additional resources required, such as test equipment or software]
```

## Quiz

- What is the primary difference between functional and non-functional testing?
- Functional testing focuses on testing the functionality of the software, while non-functional testing concentrates on performance and security.
  - Correct! Functional testing checks if the software functions correctly, whereas non-functional testing checks performance and security aspects.
- Functional testing checks the performance of the software, while non-functional testing checks its functionality.
  - Not quite. Functional testing is about functionality, and non-functional testing is about performance and security.
- Functional testing is done manually, while non-functional testing is automated.
  - Not quite. Both functional and non-functional testing can be done manually or automated.
{: .choose_best #functional_vs_nonfunctional title="Difference between Functional and Non-Functional Testing" points="1" answer="1" }

- Which type of testing verifies that changes or fixes did not introduce new defects or affect existing functionality?
- Smoke Testing
  - Not quite. Smoke testing verifies critical functionalities and identifies show-stopper issues.
- Regression Testing
  - Correct! Regression testing verifies that changes or fixes did not introduce new defects or affect existing functionality.
- Integration Testing
  - Not quite. Integration testing tests how different components or systems interact with each other.
{: .choose_best #regression_testing title="Purpose of Regression Testing" points="1" answer="2" }

- Why is end-to-end (E2E) testing important?
- It tests individual units of code in isolation.
  - Not quite. E2E testing tests the entire application workflow, not just individual units.
- It ensures that the application works as intended from start to finish, covering all necessary steps and interactions.
  - Correct! E2E testing ensures that the application functions correctly from start to finish, covering all user interactions.
- It is only used for performance testing.
  - Not quite. E2E testing is not limited to performance testing; it covers the entire application workflow.
{: .choose_best #e2e_testing title="Importance of End-to-End Testing" points="1" answer="2" }

- What is one key benefit of automated testing?
- It is always more reliable than manual testing.
  - Not quite. While automated testing can be more reliable, it does not always find visual or UX bugs that manual testing can.
- It increases the development team’s productivity by providing quicker feedback.
  - Correct! Automated testing increases productivity by providing quicker feedback.
- It completely replaces the need for manual testing.
  - Not quite. Automated testing complements manual testing but does not entirely replace it.
{: .choose_best #automated_testing title="Key Benefit of Automated Testing" points="1" answer="2" }

- What should be included in a Functional Specification document?
- Code snippets and technical implementation details.
  - Not quite. A Functional Specification document details user stories, expected behaviors, and edge cases.
- User stories, expected behaviors, and edge cases.
  - Correct! A Functional Specification document should include user stories, expected behaviors, and edge cases.
- Test case results and bug reports.
  - Not quite. Test case results and bug reports are typically included in testing documentation, not the Functional Specification document.
{: .choose_best #functional_specification title="Content of a Functional Specification Document" points="1" answer="2" }

## Conclusion
Quality Assurance and Testing are not afterthoughts but integral parts of the development process. By implementing thorough testing and integration procedures, you can ensure that your applications are reliable, robust, and ready for anything that comes their way.

Remember, "An ounce of prevention is worth a pound of cure." Happy testing! 🚀

## Resources

- [Software Testing – Beginner's Guide](https://freecodecamp.org/news/software-testing-for-beginners/)
- [End to End Testing Guide](https://www.testim.io/blog/end-to-end-testing-guide/)
- [Test Automation vs Manual Testing](https://www.testim.io/blog/test-automation-vs-manual-testing/)
- [Software Testing Basics](https://www.testim.io/blog/software-testing-basics/)
- [What is QA Testing](https://www.upwork.com/resources/what-is-qa-testing)
