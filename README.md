# Test Driven Development Notes

## When you need a reminder pull up the phonebook code it's referenced in this document(wink to self)

Test-Driven Development, or TDD, is a way to write code by focusing on testing before we even start coding. I start with writing a test for what I want my code to do, and only then do I start writing the actual code to make the test pass. 

## How TDD works, step-by-step:

Write a Test: write a small test to check a specific piece of behavior that I want in my program. For example, in the PhoneBook code, I might want to check that adding a contact works.
Run the Test: I run the test, and since I haven’t written any code yet, it fails. This is expected!
Write the Code: Now I write just enough code to pass that test.
Run the Test Again: I run the test again. If it passes, I know that my code works for that specific case. If it doesn’t, I go back and fix it until it does.
Refactor: After my code works, I look for ways to clean it up without changing what it does. I want my code to be clear and simple.
By following these steps repeatedly, I build up my program with confidence that each piece works as expected.

## Testing Applications

When I create an application, testing helps me make sure it works correctly. Think of it as checking a recipe by tasting each ingredient one at a time before mixing them all together.

In my PhoneBook example, testing means checking that:

Adding a contact to the phone book works.
Removing a contact works.
Looking up a contact by name or by phone number works.

## Common Techniques for Testing Code

Unit Testing: This is where I test individual parts of the code, like checking if the add or remove methods work in the PhoneBook. Each test focuses on one small function.
Integration Testing: Here, I check that different parts of my program work together. For example, I could check if adding a contact and then looking it up by name works smoothly.
System Testing: This is testing the whole program as if it’s being used in real life. I’d check if all the phone book features work correctly together.
In our PhoneBook class, unit tests are a great place to start because we can test each function individually.

## Anti-Patterns in TDD

An anti-pattern is something that seems like a good idea at first but actually causes problems. In TDD, some common anti-patterns include:

Skipping Tests: Sometimes, I might think a feature is “too simple” to need a test. But skipping tests is risky; even simple things can break.
Over-Testing: This is when I write too many tests for the same thing or add unnecessary checks. For example, if I test the add method in PhoneBook 10 times with the same input, it’s probably overkill.
Testing Implementation, Not Behavior: TDD focuses on what the code should do, not how it does it. If I write tests that rely too much on my exact code structure, changing my code later becomes harder.

## Limitations of TDD

TDD is helpful, but it’s not perfect. Here are some limitations:

Time: Writing tests first and updating them can take more time than just writing code. But, in the long run, it often saves time by preventing bugs.
Complexity: For very complex systems, creating tests before fully understanding the design can be tricky.
Incomplete Testing: TDD doesn’t cover every possible problem. For example, performance or security issues need special kinds of testing.

## Performance Testing

Performance testing checks how fast and efficient our code is. In my PhoneBook, performance testing might involve adding hundreds or thousands of contacts and checking if the program can still look up a contact quickly.

In TDD, we don’t focus heavily on performance testing while building each feature, but once the main functions are tested, we can check performance separately to make sure our code isn’t slow.

## Production Testing

Production testing is testing code in its real environment, like a real phone book system with actual users. Sometimes bugs only show up when real people use the code in ways we(developers) didn’t expect.

While TDD helps prevent many bugs, testing in production is often necessary to catch things we might not think of during development.

## Security and Compliance Testing

Security testing ensures that code doesn’t have weaknesses that hackers could exploit. Compliance testing checks that the code follows certain rules or laws.

For PhoneBook, security testing would make sure that private information is stored safely. For example, it would test that people can’t access others’ contacts without permission.

While TDD is great for basic functions, security and compliance testing require extra attention.

