# Newszilla

Project "MegaNews" or Newszilla (because others have used the name already): Object-oriented, structural, logical, programmable. No bullshit. News for busy people. Naming: MegaConnect.

Across: Language, same-meaning symbols.

Formal language: Subject, Verb, Object. Attributes.

Coverage: Chinese and English and French media.

Categories (Flat): Finance, Economy, Game.

Source is pure text, DSL driven, Markdown. Will be transformed before database use (likely as objects or prolog terms as dynamic patch). The time structure allows merging from multiple source during compilation process.

Main applications:

1. Simplify reading process for users
2. See features

Terminology:

1. Instead of "news" which is ambiguous from local/world news, recent events, media annoucements and magazine posts, statements at Newszilla are physically based and termed "events".

Guidelines:

1. Instead of a typical news format, statements are entity-driven and maybe event-driven.
2. No bullshit headlines, content is deep and diggable.
3. All mentioned entities must be thoroughly linked (in terms of semantics, the elaborated description can be relayed to external sources like Yahoo Finance and Wikipedia)
4. Most stuff from local news (e.g. CP24) and focused community news (e.g. PC Gamer) are TOTALLY IRRELEVANT because they are very sensational. Instead, we should focus on timeless news that are of research-grade value. Unless we can provide specific research grade information, including broader range statistics (e.g. crime rates, or recent trends), links to academic study resources, we shouldn't collect such items. Infographics in general are useless to end user for our system, but underlying raw data tables are useful if available.
    * In fact, one way to generalize such requirement is to require presence of one or more raw tabular data.
    * (THE REQUIREMENT OF THIS OVERWHELMS THE BASIC WORK OF CATEGORIZING NEWS)

Philosophy:

1. "Drillable" news with additional metadata
2. Searchable news
3. Physicallly based and event driven, though on the surface we may simply the presentation and make it look like "news headline" like format

## Features

* (Entity) Strongly typed and related entities with snapshot and real-time time-varying data (all attributes are by default time-varying, including entity names, company size, stock value)
* (Finance) Detailed sentiment analysis per entity rather than per news
* (Finance) Auto-digestion and future prediction based on aggregates

## Components (Server Stack)

* Real-time automatic news digest: process to secondary machine-sourced database
* Human news digest: process to primary human-sourced database
* Compiler: Compiles raw database content to programmable formats

## Usage

* Frontend: PENDING, with programmable functions (considering exposing query directly)
* API: PENDING
* Raw Source: Raw data source in plain text are directly readable

# Technical

## Entity Definitions

All entities are internally linked through ID, but for user digestion, explicit contents must be provided for learning. Those do not need to be provided by Newszilla and can be provided by external providers instead through hyperlinks.

* Anything that exists on Wikipedia should provide pointer to Wikipedia, including but not limited to: companies, events, individuals.
* Any companies that's listed on Yahoo Finance should provide pointer to Yahoo Finance.
* Any games that's listed on Steam should provide pointer to Steam store page.

Newszilla is technical news, not layman news - for entity definition elaborations we care more about technical data, not descriptive information that anyone can easily find on the web. This includes:

1. Publically available implementation details and conference information in summarized formats, e.g. gameplay mechanics, investment strategies, technical stacks.
