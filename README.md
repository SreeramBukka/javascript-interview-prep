# javascript-interview-prep

Thanks for interviewing at Stripe.

To make sure that we can use our time best in the interviews, we'd like to have you do some setup on your laptop in advance. If you don't have a laptop, let your recruiter know, and they will supply you with a loaner laptop for your in-person interviews.

First, clone or download this repository to your computer via the links on the right (creating a fork of the repository is not necessary).

```sh
git clone https://github.com/stripe-interview/javascript-interview-prep.git
```

# JavaScript Toolchain

We will be working with Node.js (Long term support vesrsions 22 or later). If you haven't installed Node.js yet, please follow the Node.js [installation guide](https://nodejs.org/en/learn/getting-started/how-to-install-nodejs).

## Validate your toolchain

First, we will use NPM to try installing some JavaScript packages.

Install dependencies for this project by running the following command:
```sh
# If you're using npm
npm install
```
​
This will set up the `node-fetch` package specified in the package.json file. Don't read too much into the particular packages that are installed.

To test your toolchain run the `hello-world.mjs` script using Node.js with the following command:

```sh
node hello-world.mjs
```

This will fetch some data from an open api and print it out.
​
If you need further assistance, check out the Node.js documentation.

## Debugging
We've included a `launch.json` with this project that will setup debugging in VSCode. Try setting a breakpoint in `hello-world.mjs` and using the `launch-program` command on the `Run and Debug` tab to enter debugging mode. VSCode is recommended, but use whichever editor you are most comfortable with.

Happy interviewing!


Q:
We have an existing JavaScript application that communicates with an external payment service. Implement a function that fetches payment records, processes the JSON response, and returns a simplified list of payments.
Each payment should contain:
- id
- amount
- currency
- status
- customerId
Expected behaviour: Return the transformed payment list without exposing unnecessary fields from the original API response.

Task:

Handle API failures
The external API sometimes returns an error or is unavailable. Modify the existing function to handle failed HTTP responses and network errors without crashing the application.
Tests: HTTP 500, HTTP 404, network failure, malformed JSON.


Add filtering
Modify the function so it accepts an optional status and customerId. Return only matching payments. If no filters are provided, return all payments.
Tests: one filter, both filters, no matches, no filters.
