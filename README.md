# Lingo Rooms

A browser-based multilingual translation workspace that allows users to translate phrases, organise them into language-specific rooms, and store conversations directly in the browser.

## Overview

Lingo Rooms is a front-end web application built with **HTML**, **CSS**, and **Vanilla JavaScript**.

The app allows users to translate English phrases into many languages, organise them into language-based rooms, and store conversations using browser storage.

The goal of the project was to practice building a **dynamic frontend application** that goes beyond a simple static website by including real app behaviour such as persistent state, UI updates, and API communication.

Instead of using a basic translator input field, the app introduces a **room-based workflow** where phrases can be grouped and revisited by language.

## Features

- Translate English text into **50+ languages**
- Create and manage **language-based chat rooms**
- Save translations using **localStorage**
- Edit previously translated phrases
- Delete messages from conversations
- Rename and delete rooms
- Transliteration support for languages such as:
  - Japanese
  - Chinese
  - Arabic
- Basic **Right-to-Left (RTL)** layout support for Arabic
- Word highlighting to visually map English input with translated output
- Dynamic interface rendering using JavaScript

## Tech Stack

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Fetch API
- localStorage
- Google Translate endpoint (prototype usage)

The project intentionally avoids frameworks in order to demonstrate **core JavaScript concepts and DOM manipulation**.

## How It Works

1. The user selects a target language.
2. The application creates or opens a room associated with that language.
3. The user enters an English phrase.
4. The phrase is sent to a translation API.
5. The translated text and transliteration are returned.
6. The phrase is saved in the selected room.
7. All conversations are stored using **localStorage**, allowing the session to persist after page refresh.

## What This Project Demonstrates

This project focuses on practicing key frontend development concepts:

- dynamic DOM manipulation
- rendering UI elements from JavaScript data
- managing application state
- storing persistent data in the browser
- integrating external APIs
- handling multilingual text interfaces
- implementing right-to-left layout behaviour

## Data Structure

The application stores conversations using a nested JavaScript object structure:

```javascript
app_chat_data = {
  language: {
    roomName: [
      [englishText, translatedText, transliteration]
    ]
  }
}
