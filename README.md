# Weebo Bot

A salah times bot.

![Weebo](http://vignette2.wikia.nocookie.net/jadensadventures/images/9/9a/FlubberWeebo.jpg)


## Getting Started

1. Use bundle to install the exact gems and versions that are needed. 
2. Create client.rb 

		require_relative "weebo"
		require_relative "lib/bot"
		puts Weebo::VERSION
		
		require_relative "lib/wsample"
		puts "Weebo Bot"
		
		# Weebo Bot
		weebo = Weebo::Bot.new
		Weebo.perform
3. Run ruby client.rb 

## Add your own integration
		weebo = Weebo::Bot.new
		
		weebo.scheduler(:every, frequency:, '5h') do 
			# https://your_team_name.slack.com/services/new/incoming-webhook
      # Add a new Incoming WebHooks integration with your account credentials.
      Weebo::Slacky.new('hook','channel', 'username').say(text)
		end

## Third-party Adapters

Here is a list of known adapters, but please submit an issue to have yours added to the list:

* [Slack](https://slack.com)

Interested in adding your own adapter? [Say Hello](mailto:korab@mozaix.net)

## Contributing

If there is any thing you'd like to contribute or fix, please:

- Fork the repo
- Add tests for any new functionality
- Make your changes
- Verify all new &existing tests pass
- Make a pull request


## License

Distributed under the MIT License.