Hybridauth 3.0-rc7

Build Status Scrutinizer Code Quality Latest Stable Version Join the chat at https://gitter.im/hybridauth/hybridauth


Hybridauth enables developers to easily build social applications and tools to engage websites visitors and customers on a social level that starts off with social sign-in and extends to social sharing, users profiles, friends lists, activities streams, status updates and more.


The main goal of Hybridauth is to act as an abstract API between your application and the various social networks APIs and identities providers such as Facebook, Twitter and Google.

Usage

Hybridauth provides a number of basic examples. You can also find complete Hybridauth documentation at https://hybridauth.github.io


    $config = [
        'callback' => 'https://example.com/path/to/script.php',
        'keys' => [ 'key' => 'your-twitter-consumer-key', 'secret' => 'your-twitter-consumer-secret' ]
    ];


    try {
        $twitter = new Hybridauth\Provider\Twitter($config)

        $twitter->authenticate();

        $accessToken = $twitter->getAccessToken();
        $userProfile = $twitter->getUserProfile();
        $apiResponse = $twitter->apiRequest('statuses/home_timeline.json');
    }

    catch (\Exception $e) {
        echo 'Oops, we ran into an issue! ' . $e->getMessage();
    }


Requirements

- PHP 5.4+
- PHP Session
- PHP cURL


Installation

To install Hybridauth we recommend Composer, the now defacto dependency manager for PHP. Alternatively, you can download and use the latest release available at Github.

Versions Status

    Version	       Status	     Repository	    Documentation	   PHP Version

      2.x	     Maintenance	 v2	          v2	              >= 5.3
  
      3.x	     Development	 v3	          v3	              >= 5.4
  
  
Questions, Help and Support?

For general questions (i.e, "how-to" questions), please consider using StackOverflow instead of the Github issues tracker. For convenience, we also have a [low-activity] Gitter channel if you want to get help directly from the community.


License

Hybridauth PHP Library is released under the terms of MIT License.


For the full Copyright Notice and Disclaimer, see COPYING.md.
