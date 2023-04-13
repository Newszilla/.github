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
