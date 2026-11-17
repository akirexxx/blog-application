# Blogg Application

## Overview

A simple console-based blogging application written in C#. The program allows users to create, view, search, edit and delete a blog post 
through a menu-driven interface. The application uses a list to store blog posts during run time. 

Each blog post contains three pieces of information:
```C#
        Date - the publication date;
        Title - the title of the post;
        Text - the content of the post;
```

## Features

**Create posts** - Add a new post with date, title and text. Date input is validated before the post is saved.
**View posts** - Display saved posts, sorted by publication date.
**Search posts** - Find a post by its exact title using binary search. The search is case-insensitive.
**Delete posts** - Remove a selected post from the list.
**Latest post review** - Automatically display the most recent added post when returing to the home menu. 

## Methods and Implementation

The application is structured around a main menu, a separate class and six helper methods.

| Method | Description |
|---|---|
|`Main()` | Controls the application flow and handles user input through the main menu
|`BubbleSortDatum()` | Sorts blog posts by publication date using the Bubble Sort algorithm
|`VisaSenasteInlägg()` | Displays the latest added blog post
|`BubbleSortTitle()` | Sorts blog posts alphabetically by using Bubble Sort
|`VisaInlägg()` | Displays all saved blog posts
|`BinärSökning()` | Searches for a post by title using the Binary Search algorithm
|`återMeny()` | Pauses the program and allows the user to return to the main menu

## Class Structure

A class representing an individual blog post. The constructor accepts a string array containing three values and asigns them 
to the corresponding fields.

```C#
        public string Datum;
        public string Titel;
        public string Text;
```

## Technologies and Concepts

**C#** – Programming language.
**.NET** – Application framework.
**Lists and arrays** – Used to store and organize blog post data.
**Classes and constructors** – Used to represent individual blog posts.
**Bubble Sort** – Used to sort posts by date and title.
**Binary Search** – Used to search for posts by title.
**Input validation** – Uses TryParse() to validate date and numerical input.

## How to Run

- Clone the repository.
- Open the project in Visual Studio.
- Build and run the application.
- Follow the instructions in the console menu.

## Example output

```C#
-------------------------------
Senaste inlägg #1:
Publicering: 2026-11-17
Titel: Github
Inlägg: Welcome to my page!
-------------------------------
Välkommen till din blogg!

        [1] Skriv ett inlägg
        [2] Visa dina inlägg
        [3] Sök bland dina inlägg
        [4] Redigera ett inlägg
        [5] Ta bort ett inlägg
        [6] Avsluta programmet

Välj ett alternativ:
```

## Notes

Blog posts are stored in memory while the application is running. No external database or file storage is implemented, 
which means all posts are lost when the program is closed.

## Author

Lotta Reiman
