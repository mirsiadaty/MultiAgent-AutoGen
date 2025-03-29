# Multi agent system: AutoGen

Multi-Agent System, MAS

Using open-source AugoGen, and local LM language model

```
see: https://microsoft.github.io/autogen/0.2/docs/Use-Cases/agent_chat/
```

## Two-agent system

There are two agents in this MAS:
+ 1.assistant agent,
+ 2.user-proxy agent.

The following is the conversation between the agents where they get the job done.

The question we asked the MAS is:

```
What date is today? Which big tech stock has the largest year-to-date gain this year? How much is the gain?
```

assistant (to user_proxy):
```
To get the current date and find out which big tech stock has the largest year-to-date gain, we'll need to follow these steps:

1. Get today's date.
2. Fetch the year-to-date gains of major tech stocks.
3. Compare these gains to find the largest one.

First, let's get today's date using Python:
```

user_proxy (to assistant):

```
>>>>>>>> EXECUTING CODE BLOCK (inferred language is python)...

exitcode: 0 (execution succeeded)
Code output: Today's date is: 2025-03-28
AAPL has a year-to-date gain of -9.92%
GOOG has a year-to-date gain of -16.75%
MSFT has a year-to-date gain of -8.63%
AMZN has a year-to-date gain of -12.08%
META has a year-to-date gain of -2.31%
The big tech stock with the largest year-to-date gain is META with a gain of -2.31%
```

assistant (to user_proxy):

```
Based on the output, it appears that all of the big tech stocks listed ('AAPL', 'GOOG', 'MSFT', 'AMZN', 'META') have experienced a year-to-date loss as of March 28, 2025. The losses range from -2.31% for 'META' to -16.75% for 'GOOG'.

Since 'META' has the smallest loss among these stocks, it is considered the best-performing stock in this context, with a year-to-date "gain" of -2.31%, meaning it has lost the least amount of value compared to the others.

To summarize:

- Today's date: March 28, 2025
- The big tech stock with the largest year-to-date gain (smallest loss): META
- Year-to-date gain (loss) for META: -2.31%

Given that all stocks have experienced losses, this indicates a challenging market environment for these big tech companies as of the given date.

TERMINATE
```

