# Rocket Chat Notification Plugin for Jenkins

[![Build Status](https://travis-ci.org/jenkinsci/rocketchatnotifier-plugin.svg?branch=master)](https://travis-ci.org/jenkinsci/rocketchatnotifier-plugin)

## Usage

You can use it in the Workflow/Pipeline DSL
```
node {
    try {
     ...
    } catch (e) {
        rocketSend channel: 'abc', message: 'test'
        throw e
    }
}
```
If you omit channel you can shorten it as it would now use the global default channel:
```
node {
    try {
     ...
    } catch (e) {
        rocketSend 'test'
        throw e
    }
}
```

The message looks then like this:

![sampel message](rocket_sample_message.png)

It also works with normal jobs:


![job config](rocket_job_config.png)

## Admin settings

You can define a default notification channel:


![sampel message](rocket_admin_settings.png)
