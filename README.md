![Reward Rally](https://rewardrally.in/assets/favicon.svg)

# Reward Rally - React NPM Integration Documentation

## Overview

Reward Rally is a platform that leverages gaming techniques to motivate user participation, engagement, and collaboration.

## Scope

This document provides detailed instructions for integrating Reward Rally into a React application. It is intended for developers and technical teams who need to implement Reward Rally's gamification and leaderboard features.

## Audience

- Developers integrating Reward Rally into their React applications.
- Technical teams responsible for configuring and maintaining the integration.

## Prerequisites

- Reward Rally account.
- Credentials needed for integration.

## Integration Steps

### Installation

Install the Reward Rally React NPM package:

```bash
$ npm install @theproindia/react-rewardrally
```

## Usage

## Render Leaderboard

To use Reward Rally in your React application, follow these steps:

Insert the `RewardRally` component into your React component where you want the leaderboard to appear. Provide the required parameters:

```jsx
import { RewardRally } from "@theproindia/react-rewardrally";

const App = () => (
    <RewardRally
        userId={<UserId>}
        applicationId={<ApplicationId>}
        clientId={<ClientId>}
        clientSecret={<ClientSecret>}
    />
);

export default App;
```

### Parameters:

- `userId` (string): Unique User ID from your client application.
- `applicationId` (string): Application ID configured in the Reward Rally admin panel.
- `clientId` (string): Client credential provided by the Reward Rally team.
- `clientSecret` (string): Client credential provided by the Reward Rally team.

## Create User with Reward Rally

This section provides instructions on how to create a new user in the Reward Rally system using the `createUser` function.

The `createUser` function is used to register a new user in the Reward Rally system. This function requires specific user details to be provided and returns a response with information about the newly created user.

## Function Syntax

```jsx
import { createUser } from "@theproindia/react-rewardrally";

const response = await createUser({
  userId: "<UserId>",
  userName: "<UserName>",
  application: ["<ApplicationId>"],
});
```

## Updating a Game Action

This section provides instructions on how to trigger a gameaction in the Reward Rally system using the `createUser` function.

To trigger a game action, use the `updateGameAction` function provided by the Reward Rally package. This function allows you to notify the system of actions performed by a user.

## Function Syntax

```jsx
import React from "react";
import { updateGameAction } from "@theproindia/react-rewardrally";

const MyComponent = () => {
  const handleAction = () => {
    updateGameAction(
      <userId>
      <gameactionId>,
      <correspondingUserId>(optional),
      <correspondingUserApplicationId>(optional)
    );
  };

  return <button onClick={handleAction}>Complete Action</button>;
};

export default MyComponent;
```

### Parameters:

- `userId` (string): The ID of the user performing the action. This is a required parameter.
- `gameActionId` (string): The specific action being reported. This should be a predefined action ID or type.
- `correspondingUserId` (string, optional): Works Only with Rival Points configuration
- `correspondingUserApplicationId` (string, optional): Works Only with Rival Points configuration

## Security Reporting

If you find a security issue with our libraries or services, please report it to [contact@rewardrally.in](mailto:contact@rewardrally.in) with as much detail as possible. We will contact you shortly upon receiving the information.

## License

Copyright (c) Peninsular Research Operation. All rights reserved.

## Contact

For questions, issues, or feedback, please contact [contact@rewardrally.in](mailto:contact@rewardrally.in).
