# TwitterBot
A series of automation scipts written in Python by [Michael Sterpka](https://github.com/michaelsterpka).

##Use Guide
Please read the following in order to better understand how to properly use TwitterBot.

* __Fields__
   * `Verification URL:` For your first time use, copy the link into your browser and follow the instructions in order to obtain your verification PIN.
   * `PIN:` The PIN gathered from the verification URL. The PIN is only needed upon first use, or additional token generation.
   * `Amount:` The amount to be followed/unfollowed, depending on choice.
   * `Target:` Used in the follow command. 
   
* __Tokens__
   * Access tokens are stored in a `tokens.txt` text file. 
   * If you have an issue authenticating your account, delete the tokens file and re-follow the steps to authenticate your account. 
   
##Commands

* <b>Follow</b> - Allows for the following of a specific set of users. This set is generated by selecting a single user and fetching his or her followers. 

    _Required:_
    * `Amount:` The amount to be followed.
    * `Target:` The user you wish to follow.
  
  
* <b>Unfollow</b> - Allows for the unfollowing of already followed users. 

    _Required:_
    * `Amount:` The amount to be unfollowed.  
    
    _Optional:_
    * `Stable Mode:` Implements a random sleep timer in order to reduce the chance of a `RateLimitError`.
    * `Skip Mutual Followers:` Only unfollows users who are <b>not</b> following you back. 


##Notice
Rapid following and unfollowing of users is against [Twitter's Terms of Service](https://twitter.com/tos?lang=en) and may result in either an account closure or suspension. Please be weary when spam (un)following. By using this application, you aknowledge the risks and consequences.

##Libraries
A few public libraries were used to make this project possible. Thank you to the following:
* [Tweepy](http://www.tweepy.org/), an open-source Python library built for accessing the Twitter API.
* [PyQt5](http://pyqt.sourceforge.net/Docs/PyQt5/index.html), a GPL licensed Python binding for the Qt application framework
