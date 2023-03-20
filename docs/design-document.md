# Software Design Documentation

## Meal Planner

Written By: Daniel Rosales

## Introduction

The goal of this project is to test the prototyping capabilities granted by large language models like GPT. For this a meal planner app will be developed. While an app like this would usually need large databases of nutitional information and many calculaitons, using GPT the team should be able to develop a functional version of the app in a fraction of the time that it would take to gather all that information.

While it is possible that costs could be reduced by limiting the usage of NLPs, hitting the market quickly could mean an important difference. Then, GPT usage could be replaced gradually and improve revenue.

## System Overview

The meal planner app will take user information about weight, height, age, level of activity and nutritional goals. With this information, the app will recommend a daily protein and caloric intake. Then, it will suggest meals that fit those parameters.

The user will be able to personalize suggestions. For examples, requesting an ingredient to be excluded.

If the user decided to "break the diet" and eat somehting that wasn't planned, they could register the amount of calories they ate and the app will ajust the next day to make up for it.

## Design Considerations

### Assumptions and Dependencies:

The main dependency of the project would be the functionality of GPT. This is ok in this case since the main goal is to explore the potential of GPT in an application. However, it would be worth considering for future projects.

It is assumed that developing the application using GPT will be easier than through regular means. While this will likely make is more expensive in the long run, it will allow to get the app to a production ready state in a shorter time.

It is assumed that GPT will be stable enough to substitude the necesary information in a production environment.

### General Constraints

The main constraint will be available time, since this is a personal project.

### Goals and Guidelines

The main goal would be to create a simple app that help the user plan their meals for a week, and ajust the diet to accomodate mid week changes.

### Development Methods

The software will be developed using the agile methodology with a continous deployment lifecicle. It will have a strong focus on gathering data that could be reused to minimize the use of GPT.

## System Architecture

This version of the app will be made mostly for testing and will have a simple architecture. It will be made as a local node.js app using express as the server. It will have the follwoing components.

### Manager

The manager component will be in charge of recieving the requests from the frontend and determine the calls that will be made. It is important to separate this component from the GPT component since we will be adding data gathering and data reusability features to the calls.

### GPT

This component will be in charge of managin the calls to the Open AI api. It will be relatively simple however we will want to find a confortable way of making GPT calls. It will be particularly important to focus on the single responsability principle so replacing the use of GPT is easier.

### Data Gathering

In order to reuse information and reduce the use of GPT, we will have a dedicated data gathering component that will be in charge of registering which meals are recommended to a particular user, how the ajustments are made, and any other information that could be reused for similar users.

### Auth

While this version of the app will be for local use, it will be started with a auth component to implement the data gathering component in a more consistent way. This component will focus on the creation of accounts, authentication and authorization of users.

## Detailed System Design

Describe components and subcomponents.
Module 1
Module 2
