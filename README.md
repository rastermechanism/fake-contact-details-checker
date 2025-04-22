# Fake Contact Detector Project

## Overview
This project provides functionality to check whether an email address is associated with a fake domain. The core logic is implemented in the `faketester.js` file. It reads a JSON file with domain data and uses it to verify if an email's domain is considered fake, either via an exact match or a subdomain check.

## Installation
1. Clone the repository.
2. Ensure you have Node.js installed.
3. Run `npm install` to install any necessary dependencies.

## Usage
- Place your JSON file containing the fake domains at `./json/data.json`.
- Import and use the `isFakeEmail` function from `faketester.js` to determine if an email address is fake.

### Example
```javascript
import { isFakeEmail } from './faketester.js';

const email = "example@fake-domain.com";
if (isFakeEmail(email)) {
    console.log("This is a fake email.");
} else {
    console.log("This is a valid email.");
}
