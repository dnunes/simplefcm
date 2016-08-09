simplefcm
=========
Finally a simple Firebase Cloud Messaging (FCM) lib that really works!

A library **should help you, not get in your way**. This lib was made with that goal: help you, not fight you. It has a very simplistic interface with callback style functions and works exactly as you would expect.

This code was losely based on the [nandarustam/fcm-push][1]. I forked it for a simple fix but it ended up becoming a total refactor.


## <a id="install">Installation</a>

Via [npm][2]:

    $ npm install simplefcm


## <a id="basicusage">Basic Usage</a>

In your code:

```javascript
//???
    var FCM = require('simplefcm');

    var serverKey = '';
    var fcm = new FCM(serverKey);

    var message = {
        to: 'registration_token', // required
        collapse_key: 'your_collapse_key',
        data: {
            your_custom_data_key: 'your_custom_data_value'
        },
        notification: {
            title: 'Title of your push notification',
            body: 'Body of your push notification'
        }
    };

    fcm.send(message, function(err, response){
        if (err) {
            console.log("Something has gone wrong!");
        } else {
            console.log("Successfully sent with response: ", response);
        }
    });
//???
```


## <a id="conventions">Conventions</a>

### <a id="a">???</a>

???


## <a id="advancedusage">Advanced Usage</a>

???

```javascript
//???
```


## <a id="releaseh">Release History</a>

* 0.1.0 Initial release


## <a id="credits">Credits</a>

Created and maintained (with much ♡) by [diego nunes](http://dnunes.com)

Donations with Bitcoin to _1H6Z1xbq1Lh3zKhEnDBxHZgEjcFPPjkpKF_:

![1H6Z1xbq1Lh3zKhEnDBxHZgEjcFPPjkpKF](http://chart.apis.google.com/chart?cht=qr&chs=200x200&chl=bitcoin:1H6Z1xbq1Lh3zKhEnDBxHZgEjcFPPjkpKF)





## Usage


See [FCM documentation][2] for details.

[1]: https://github.com/nandarustam/fcm-push
[2]: http://github.com/isaacs/npm
