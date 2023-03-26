
![Wonderland](https://user-images.githubusercontent.com/38309438/227752369-60583dc3-9463-4651-bac7-818d6971a636.png)

# Wonderland

Wonderland is a collaborative AI art canvas: think r/place meets modern diffusion AI. We wanted to create a way for people to generate and modify images together, and observe how AI art evolves and changes based on their prompts. By using a combination of web-sockets and svelte and self hosted AI, we were able to achieve our goal: a collaborative, community-driven AI art experience.

## Tech

Our backend is a split model. We handle all AI between NodeJS Express + Python Flask.

The flask server is responsible for hosting the AI. It is held behind a local proxy, and used to mutate images based on user input. 

The NodeJS server is our central logic server. It handles all web-socket connections, and is responsible for sending and receiving data from the AI server. It also handles all user authentication, and is responsible for storing user data.

We used Socket.io for our web-socket implementation. We used Svelte for our frontend, Tailwind because CSS sucks. We decided not to use a database, and store all memory locally.

However, we log every single user action, ip, and image generated to a file. Over the course of the past few hours since we've lost, more than 20 people have generated over 200 unique images together.



