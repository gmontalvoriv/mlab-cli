# mLab CLI
[![npm version](https://img.shields.io/npm/v/mlab-cli.svg?style=flat)](https://www.npmjs.com/package/mlab-cli)
[![Dependency Status](https://david-dm.org/gmontalvoriv/mlab-cli.svg)](https://www.npmjs.com/package/mlab-cli)

#### A command-line power tool for mLab (PKA MongoLab).

```mlab-cli``` aims to speed up some basic database management operations for your [mLab](https://mlab.com/) account.

## Dependencies

Make sure you have NPM and NodeJS installed:

```
$ npm --version && node --version
```

## Installation

```
$ npm install --global mlab-cli
```

## Configuration

From the official [mLab Data API](http://docs.mlab.com/data-api/) documentation:

> ### [API Authentication](http://docs.mlab.com/data-api/#authentication)
>
> Each API request must pass an apiKey query parameter. By default, access to the Data API is disabled and must be enabled before you can obtain your API key.
>
>Follow these steps to enable Data API access and obtain your API key:

> 1. Log in to the mLab management portal
> 2. Click your username (not the account name) in the upper right-hand corner to open your account user profile
>   - If you are already in the account details page, then click on the row with your username in the Account Users section
> 3. If the status is showing as “Data API Access: Disabled” in the “API Key” section, click the “Enable Data API access” button
> 4. Once Data API access is enabled, your current API key will be displayed in the “API key” field 
> 5. (Optional) If you want to update the current key, click “Regenerate API key”

Once you've enabled an API key for your account use the ```authorize``` command to set up your key, otherwise you'll receive an error that looks like this:
 
 ```
 Error: account unauthorized, please provide a valid API key.
 ```
 
 Your account key is stored in a YAML-formatted file located at ```/usr/local/lib/node_modules/mlab-cli/.mlabrc.yml```.
 
 ***NOTE***: Your API key will give full access to all data within the databases belonging to your mLab account. If you distribute it to untrusted individuals, they can gain access to your account and your data.
 
## Usage Example

Typing ```help``` will list all the available commands. You can type ```help TASK``` to get help for a specific command.

```
$ mlab
mLab CLI version: x.x.x

> help
```

## License

[MIT](https://github.com/gmontalvoriv/mlab-cli/blob/master/LICENSE) © Gabriel Montalvo
