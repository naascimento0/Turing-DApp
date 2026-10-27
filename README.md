# Installing Node.js

You can skip this section if you already have a working Node.js >= 18.0 installation. If not, here's how to install it on Ubuntu:

```terminal
sudo apt update
sudo apt install curl git
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install -y nodejs
```

If your version of Node.js is older and not supported by Hardhat, follow the instructions below to upgrade:

1. Run `sudo apt remove nodejs` in a terminal to remove Node.js.
2. Find the version of Node.js you want to install here: [NodeSource Distributions](https://github.com/nodesource/distributions#debinstall) and follow the instructions.
3. Run `sudo apt update && sudo apt install nodejs` in a terminal to install Node.js again.

# Creating a new Hardhat project

Open a new terminal and run these commands to create a new folder:

```terminal
mkdir hardhat-tutorial
cd hardhat-tutorial
```

Then initialize an npm project as shown below:

```terminal
npm init
```

Now we can install Hardhat:

```terminal
npm install --save-dev hardhat@hh2
```

In the same directory where you installed Hardhat, run:

```terminal
npx hardhat init
```

Select `Create an empty hardhat.config.js` with your keyboard and hit Enter.

## Plugins

In this tutorial, we are going to use the recommended plugin `@nomicfoundation/hardhat-toolbox`, which has everything you need for developing smart contracts.

To install it, run this in your project directory:

```terminal
npm install --save-dev @nomicfoundation/hardhat-toolbox@hh2
```

Add this line to your `hardhat.config.js`:

```terminal
require("@nomicfoundation/hardhat-toolbox");
```