---
name: weird-movie-greeting
description: Use this skill whenever the user's message is just a greeting, in any language or script. Triggers include "Hi", "Hello", "Hey", "Ahoj", "Čau", "Servus", "Hola", "Bonjour", "Ciao", "Hallo", "Cześć", "Привет", "Merhaba", "Olá", "Hej", "Konnichiwa", "こんにちは", "你好", "안녕하세요", "Salam", "Shalom", "Yo", "Howdy", "Good morning" and any other way of saying hi. Responds with a totally weird movie quote.
---

# Weird Movie Greeting

When the user greets you, answer with one strange, absurd or wonderfully out-of-context quote from a real movie instead of a normal greeting.

## Steps

1. Detect the language of the greeting.
2. Pick a real line of movie dialogue that sounds bizarre when read on its own. Good picks are surreal, oddly specific, or hilariously out of context. Prefer cult films, B-movies and odd moments from famous films over the obvious "greatest quotes" lists. Vary the choice every time; never reuse the same quote twice in one conversation.
3. Keep the quote short: a single line, under 15 words. Only quote lines you are confident are real and correctly attributed. If unsure, pick a different one.
4. Reply in this format:

   > "<quote in the original language>"
   >
   > <character>, *<Movie Title>* (<year>)

5. If the greeting was not in English, add a one-line translation of the quote in the greeting's language, then return the greeting in that language.
6. End with one short, dry sentence of fake context that makes it weirder (for example, "I say this to everyone on Tuesdays.").

## Rules

- Never explain that this is a skill or why the reply is weird. Play it straight.
- Do not use em dashes.
- If the message contains a greeting plus a real request (for example "Hi, can you fix my code?"), skip the quote entirely and just help with the request.
- Keep it safe for work: no slurs, gore or sexual lines.
