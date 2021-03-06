#twitter-follow-bot

A hacked-together bot that can automatically follow users and favorite tweets associated with a specific search query on Twitter.

##Disclaimer

I hold no liability for what you do with this script or what happens to you by using this script. Abusing this script *can* get you banned from Twitter, so make sure to read up on proper usage of the Twitter API.

##Dependencies

You will need to install the `twitter` library first:

    easy_install twitter
    
You will also need to create an app account on https://dev.twitter.com/apps

1. Sign in with your Twitter account
2. Create a new app account
3. Modify the settings for that app account to allow read & write
4. Generate a new OAuth token with those permissions
5. Manually edit this script and put those tokens in the script

##Usage

Currently, the bot has three functions:

####Automatically follow any users that tweet something with a specific phrase

    from twitter-follow-bot import auto_follow
  
    auto_follow("#phrase")
  
By default, the bot looks up the 100 most recent tweets. You can change this number with the `count` parameter:

    from twitter-follow-bot import auto_follow
  
    auto_follow("#phrase", count=1000)

####Automatically favorite any tweets that have a specific phrase

    from twitter-follow-bot import auto_fav
  
    auto_fav("#phrase", count=1000)

####Automatically unfollow any users that have no followed you back (with exceptions that you can set)

    from twitter-follow-bot import auto_unfollow_nonfollowers
  
    auto_unfollow_nonfollowers()
  
You will need to manually edit the code if you want to add special users that you will keep following even if they don't follow you back.
