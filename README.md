# rundeck-webexteams

A notification plugin for Rundeck to send notifications to WebEx Teams.

## Dependencies

* [spark-java sdk](https://github.com/webex/spark-java-sdk)

## Installation instructions

1. Build a snapshot from source using `gradle build`
2. Copy the `build/libs/rundeck-webexteams-1.0.jar` file to your `$RDECK_BASE/libext` folder
3. Get an App Token from WebEx.
     New Bot: https://developer.webex.com/my-apps/new/bot
     Existing Bot: https://developer.webex.com/my-apps
4. Add the token (only shown once when you generate it for your app), to the following key:
     project.plugin.Notification.WebExTeams.token=<token>
5. In Rundeck when you add a Notification you can now pick WebEx.  The room is the ID of the Room not the name.  You can get the ID by selecting the Gear and then the link to the room.  The space= part is the Room ID
6. Profit

## Configuration

You'll need a WebEx Teams Auth Token.  Easiest way is to register a bot and use it's token.  Make sure to add the bot to the room you want notifications in.

You'll also need the room UUID that you want to post notifications to.  You can [list rooms](https://developer.webex.com/docs/api/v1/rooms/list-rooms) from the interactive API using the bot Auth Token once you've added the bot to the appropriate room.
