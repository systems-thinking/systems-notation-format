# Systems Notation Format Project

The Systems Notation Format Project is an attempt to create an RFC for a notation format that can be used to describe and display systems.

The initial goals (set by myself [Tane Piper](https://github.com/tanepiper)) are not set in stone, but here to capture a *Guiding Star* that can allow ideas to be captured and developed.

## Inspiration

I've recently been working more with Systems Thinking - and honesty the pen & paper (or pen & tablet) and hand-drawn systems are still the best way for me to work, but I'd like to start making them more sharable, but also allow them to be used to simulate systems (like [Loopy](https://ncase.me/loopy)).

Currently, there is no one tool that I see that can accuratly allow Systems Thinkers to map and experiment with their system. As I thought about my own tool, I started to define the data structure requirements for Stocks, Connections and Decisions - at this point I saw a really close parallel to [BPMN](https://en.wikipedia.org/wiki/Business_Process_Model_and_Notation) - a way to represent business processes.

With this, it inspired me to capture the idea of a notation (or "language") that can itself be used to define systems.

## Goals

### Portable and Friendly

The format should be portable and friendly to use.  Portable means that it can exist as a file or it can be embedded for example in Markdown code blocks for use with rendering.  From a technical perspective, and libraries for using this format should be seperated as much as possible - parsing, rendering, writing and modifying.

Here the format could be JSON, XML or another kind of text notation format

### System Components

The format should allow for the definition of different parts of systems - Stocks, Connections and Decisions

#### Stocks

Stocks can be considered variables that can have a set of pre-existing values set, as well as some system values

|Property|Type     |Description|
|--------|---------|-----------|
|`id`    |`string` |Internal ID property for the stock, most likely a UUID or custom ID from user|
|`label` |`string` |The display label for the stock
|`shape` |`string` |The display shape for the stock - used for programs that will display fixed shapes based on this, UI properties are seperate|
|`startValue`|`number`|The start value of the stock, the sensible default is 0
|`maxValue`|`number`|The maximum value the stock can be, the sensible default is 100. The value is ignored if set to 0

### Meta Components

The format should allow for the definition of Goals, Seperation of system domains, taxonomy and other graph-based values

### System States

The format should allow for the setting of initial conditions, and for capturing states (this allows playback)

## Todo

- [ ] Set up webpage with more information
- [ ] Create tickets to discuss different requirements of the format
- [ ] Set up POC
- [ ] Create OpenAPI files
