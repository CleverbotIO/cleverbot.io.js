# cleverbot.io

[![Slack Status](https://slack.cleverbot.io/badge.svg)](https://slack.cleverbot.io)

To use this package, simply download it, place *cleverbot.io.min.js* in the web directory add the following to your page

    <script type="text/javascript" src="cleverbot.io.min.js"></script>
  Note: It is a good practice to include *--save* to add this to your dependencies in your package.json
  
Before using this module, please get your API keys at [http://cleverbot.io/keys](http://cleverbot.io/keys)

To initialize cleverbot, create a new instance of cleverbot

    var bot = new cleverbot("YOUR_API_USER", "YOUR_API_KEY");
    
*cleverbot.io* allows you to save cleverbot sessions to access later
If you've already created a session previously, simply add the following code to reference it

    bot.setNick("sessionname")

To create or access a cleverbot session, start with the following

    bot.create(function (err, session) {
      // session is your session name, it will either be as you set it previously, or cleverbot.io will generate one for you
      
      // Woo, you initialized cleverbot.io.  Insert further code here
    });
    
Now querying cleverbot is simple, you pass the text to the *.ask()* method

    bot.ask("Just a small town girl", function (err, response) {
      console.log(response); // Will likely be: "Living in a lonely world"
    });
    
Well, that's it for now!  Happy hacking!

**Cleverbot.io is free and open source, and will remain so.**
