# Github Actions / Coding Quiz Application

## Overview
The Coding Quiz Application is a web-based quiz platform designed to test users' knowledge on various coding topics. The application is built using React for the frontend and Node.js with Express for the backend. It features a set of multiple-choice questions that users can answer to test their coding knowledge. The application also includes a CI/CD pipeline using GitHub Actions to ensure code quality and automate deployment.

## Features
- **Multiple-choice questions**: Users can answer a series of multiple-choice questions.
- **Score tracking**: The application tracks the user's score and displays it at the end of the quiz.
- **Random questions**: The questions are fetched randomly from the server.
- **Responsive design**: The application is designed to work on various screen sizes.
- **CI/CD Pipeline**: Automated testing and deployment using GitHub Actions.

## Technologies Used
- **Frontend**: React, TypeScript, Bootstrap
- **Backend**: Node.js, Express, MongoDB
- **Testing**: Cypress, Vitest
- **CI/CD**: GitHub Actions

## Getting Started

### Prerequisites
- Node.js
- npm
- MongoDB

### Installation
#### Clone the repository:
```sh
 git clone <repository-url>
```

#### Install dependencies:
```sh
 npm install
```

#### Seed the database:
```sh
 npm run seed
```

#### Start the development server:
```sh
 npm start
```

## Running Tests
#### To run the Cypress tests:
```sh
 npx cypress run
```

#### To run the component tests:
```sh
 npx vitest
```

#### To open the Cypress GUI:
```sh
 npx cypress open
```

## GitHub Actions
The project uses GitHub Actions for continuous integration and continuous deployment (CI/CD). The workflow is defined in the `main.yml` file.

### Workflow
The workflow consists of two jobs:

1. **Cypress Tests**: This job runs Cypress component tests on pull requests to the `develop` and `main` branches.
2. **Deploy to Render**: This job deploys the application to Render when changes are pushed to the `main` branch.

### Configuration
The workflow is triggered on the following events:
- `pull_request` to the `develop` and `main` branches.
- `push` to the `main` branch.

### Steps
1. **Checkout repository**: Uses the `actions/checkout@v4` action to checkout the repository.
2. **Setup Node.js**: Uses the `actions/setup-node@v4` action to set up Node.js.
3. **Install dependencies**: Runs `npm install` to install the project dependencies.
4. **Run Cypress component tests**: Runs `npx cypress run --component` to execute the Cypress component tests.
5. **Deploy to Render**: Uses a `curl` command to trigger a deployment to Render.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Contact
For any questions or inquiries, please contact [William Hoenig](mailto:will.hoenig44@gmail.com).
