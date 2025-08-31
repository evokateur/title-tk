# title-tk

Order from Chaos task decider, inspired by the book by Jaclyn Paul. It doesn't have a name yet (like the Breeders album)

## Objective

A task queue for the neurodivergent that eliminates the trauma of deciding what to do next. Tasks can be stand-alone (doable right away, in the proper context) or part of a Project (anything that requires more than one step).

## Features

- Create a task, when something must be done outside of your current context
  - Generally, when you realize that something should be done you can either do it right away, or create a marker to remind you that it needs to be done, to keep your call stack from getting too large. The main thing is to not forget about it completely. You just need some kind of marker that will bring the idea of the task back to you in the future. For example, if I run out of a something, I'm going to need to add an item to my shopping list (AnyList). Instead of taking the time to open the app and add the item I'll often leave a physical marker for myself. I'll take the empty container and put it on my desk. That's just an example. I think it's similar to the idea of an inbox as described in the book. I'd like to make it as easy as it possibly can be to create a TODO/task in the app. What this possibly means is a widget, which I understand in terms of iOS, but not in Android. If you are creating this sort of marker (tossing something into your inbox) you may not actually know whether the thing is a task or a project, you just know that it's something to address. Deciding how to go about it, how simple or complex it is, requires some thought that wants to be put off until later.

- Create/Edit a project, with or without initial tasks, or with a starting task of figuring out the steps to complete it.
  - AI assistant to generate steps based on the project description, which works starting with zero or any number of existing tasks

- Generate TODOs, by context, for a bullet journal daily log

## Ubiquitous Language

- Task: something that involves only one step
- Project: something that involves more than one step; having Actions as a set of Tasks

## Task Properties

- 0..1 Project
- Status: Next Action (doable right now), Waiting (waiting for something else to happen), Delegated (waiting for someone else to do it)
- 1..1 Context (under what circumstances can the Task be performed?). The contexts should be defined by the user organically. If I cannot do this thing now, when can I do it? --> create the context
  Example contexts (taken from book):
  - House (anytime)
  - Outdoors
  - Weekend (requiring uninterrupted time)
  - Basement
  - Computer (any), Computer (depending on specific software)
  - Phone (talking) and Phone (texting)
  - Desk (no computer)
  - Errands (probably requiring a form of transportation)
  - Television (requires very little attention)
- Blocking Task (if status is Waiting, what is the task that must be completed before this one can be done?)
- Due date (if the task MUST be done by a specific time)
- Priority (ceteris paribus, how is it  positioned in the queue?)
