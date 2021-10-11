# Notes

## Hardhat Runtime Environment

you'll constantly notice that we use `hre.ethers`, but hre is never imported anywhere? What type of sorcery is this?

Directly from the Hardhat docs themselves you will notice this:

The Hardhat Runtime Environment, or HRE for short, is an object containing all the functionality that Hardhat exposes when running a task, test or script. In reality, Hardhat is the HRE.

So what does this mean? Well, every time you run a terminal command that starts with `npx hardhat` you are getting this hre object built on the fly using the `hardhat.config.js` specified in your code! This means you will never have to actually do some sort of import into your files like:

`const hardhat = require("hardhat")`
