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
