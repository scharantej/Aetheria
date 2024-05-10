## Flask Application Design for Maplestory Bot

### HTML Files

- **maplestory_bot.html:** This HTML file will serve as the main interface for the bot. It will include a form that allows the user to specify the parameters of the bot, such as the character name, server, and the actions to be performed.
- **maplestory_bot_results.html:** This HTML file will display the results of the bot's actions. It will show a list of the tasks that the bot has completed, along with any errors that have occurred.

### Routes

- **@app.route('/maplestory_bot', methods=['POST'])**: This route will handle the form submission from the maplestory_bot.html file. It will parse the form data, create a new MaplestoryBot instance, and start the bot.
- **@app.route('/maplestory_bot_results')**: This route will serve the maplestory_bot_results.html file. It will query the database to retrieve the results of the bot's actions.
- **@app.route('/maplestory_bot_stop')**: This route will handle the stop button in the maplestory_bot.html file. It will stop the bot and redirect the user to the maplestory_bot_results.html file.

### Additional Notes

- The MaplestoryBot class will be responsible for performing the actions specified by the user. It will use the MapleStory API to control the character and perform tasks such as looting items, killing monsters, and completing quests.
- The bot will run in a separate thread so that it does not block the web application.
- The database will store the results of the bot's actions, such as the number of items looted, the number of monsters killed, and the quests completed.