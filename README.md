# Free Food Finder

A website that helps Texas A&M students find free food and events on campus, and checks whether the food is still there before they walk over.

Built at HowdyHack

**Live demo:** [(https://loquacious-squirrel-bf9eb5.netlify.app)]

**Demo video:** [(https://youtu.be/hrA62dmxbcY?si=ULvR-PCp8kzVVl0o)]

<p align="center">
  <img src="https://github.com/user-attachments/assets/977a171a-3c24-4675-b86e-f1d67b48885c" alt="Project Screenshot" width="100%">
</p>

Free food gets announced in group chats, posters, and instagram posts, but by the time you get there it's often gone or the line is huge. This site puts every event in one place and lets people tell each other what it's like right now.

## What it does

- **Events list** Events are grouped by day and sorted by start time. Events disappear automatically after they end.
- **Event popup** Includes the place, room number, time, and a "how busy is it?" bar.
- **"I'm Here!" check-in.** Event-goers slide the bar to report how busy it is, and the bar updates from the average of check-ins over a certain amount of time.
- **Add Event form** Create events with a date picker, typed locations with suggestions (MSC, Zachry, Evans Library, and more), and time boxes that only accept a valid 12-hour time. The map updates after events are added. 
- **Map and Nearby.** Events show as pins on a Leaflet map, and the Nearby box lists events by distance from your location in order to increase ease of attending events. 
- **Live chat for each event,** The live chat is updated in real time, so people can say things like "pizza is not worth it." and is specified to any active event. It's only possible to type in the chat if the user is logged in. 

## Built w/

- HTML, CSS, and vanilla JavaScript
- [Supabase](https://supabase.com) (Postgres database and realtime messages)
- [Leaflet](https://leafletjs.com) and OpenStreetMap for the map
- [Netlify](https://www.netlify.com) for hosting and continuous deployment
- Josefin Sans and Material Symbols from Google Fonts


## Run it yourself

1. Clone the repo:
   ```
   git clone https://github.com/kaavg07/howdyhack.git
   ```
2. Open the folder in VS Code and run `index.html` with the **Live Server** extension.
3. Add your own Supabase project URL and `anon` key in `db.js`.
4. Create the `events` and `messages` tables above, and turn on Row Level Security with policies that only allow the reads and inserts the app needs.

Never commit secret keys. Put them in a local `.env` file (already in `.gitignore`) or in Netlify environment variables.

## Challenges we ran into

- Coordinating three people in one repo, including resolving merge conflicts in the same file.
- Keeping the front end and the database in sync when field names changed.
- Ensuring that each teammate was sure of their roles and meeting the project deadline. 
 

## What's next

- Save check-ins to the database so everyone sees the same busy bar (currently each browser keeps its own).
- Notifications by text, email, and push for the food types people choose.
- Add to the bot that currently scrapes a dummy FFIN Group me, enabling it to actually add events to the website. 
- Anonymous tips, and organization accounts for posting leftovers.

