# Quality Assurance & Testing 🪳

As a developer, you can use the [built in rails testing framework](https://guides.rubyonrails.org/testing.html) (or [rspec](https://rspec.info/)) to write unit tests to assert your code is written as intended.

When your app is deployed, you may want to use a service like [airbrake](https://github.com/airbrake/airbrake) or [rollbar](https://github.com/rollbar/rollbar-gem) to track exceptions. These services track exceptions, notify you, and save the context so you can easily track down the root cause to fix the issue. Otherwise, your deployed app could be broken and you'd never know! 🤯 

Besides tracking exceptions, it's helpful to know whether your app is working as intended. Your app could be quietly broken. 😶 That's why it's helpful to write a Functional Specification so you (or your QA team) know what to test against.

![](assets/api-testing.gif)

[Source](https://blog.bytebytego.com/p/ep83-explaining-9-types-of-api-testing)


[Lecture Video](https://youtu.be/aIbkLU8av0A)
