# title-tk

Order from Chaos task decider, inspired by the book by Jaclyn Paul

## Objective

A task queue for the neurodivergent that eliminates the trauma of deciding what to do next. Tasks can be stand-alone (doable right away, in the proper context) or part of a Project (anything that requires more than one step).

## Features

- Create a task, when something must be done outside of your current context
- Create/Edit a project, with or without initial tasks, or with a starting task of figuring out the steps to complete it.
  - AI assistant to generate steps based on the project description, which works starting with zero or any number of existing tasks
- Generate TODOs, by context, for a bullet journal daily log

## Ubiquitous Language

- Task: something that involves only one step
- Project: something that involves more than one step; having Actions as a set of Tasks

## Task Properties

- 0..1 Project
- Status: Next Action (doable right now), Waiting (waiting for something else to happen), Delegated (waiting for someone else to do it)
- 1..1 Context (under what circumstances can the Task be performed?). These will be user defined on the fly in an organic way
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
