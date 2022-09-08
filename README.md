# Project title
Self Hosted Alt

# What and why?
A lot of cool (often open source) software is built to replace non self hosted products. However, it can be difficult to find projects to replace the products that you are currently using. It would be useful to have an interactive website that can intelligently suggest self hosted alternatives to non self hosted applications.

# For whom?
This is for technical people who want to switch more of their internet usage to self hosted projects, but are not able to figure out which projects to implement and run.

It can also be for people who are interested in self hosting, and want to know what they will be able to do.

# How?
When a user queries the website with an action, then the website should respond with a list of projects. That list should include the project mainpage, short description, and potentially pros/cons

## Example
1. User searches for file storage
2. Website responses with `nextcloud` `onlyoffice` `openmediavault` `truenas`

# Scope

## Components
1. Projects Database
   * Acquire through searching of popular hosting sites - e.g. `gitlab` `sourceforge`
   * Store: 
     * Project name
     * Project page
     * Description
     * Text/Markdown Files
2. Query Logic
   * Pretty much just word searching algorithm
3. Frontend
   * Single Page
     * Search bar on top
     * Results underneath

### Searching simplification
For a first version we can just use word matching in order to find projects that relate to the initial query.

If time permits, we may be able to expand to some popular searching engines such as `elasticsearch`.

### Indexing simplification
For a first version, we can limit our indexing to a few specific sites like `gitlab`, `sourceforge`, or `artifacthub`.

If time permits, we may be able to expand indexing to the whole of the internet. We can also keep with the Elastic stack and implement `elastic web crawler`. We can also use something like `scrapy` and implement something ourselves.

## Time Justification
I believe this project is completable within the semester. This is because there is little work to on the frontend/API. Also, the hardest parts of the project (searching and indexing) are simplified to fit within the time constraints of a semester.

