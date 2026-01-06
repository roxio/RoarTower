Roar Tower - JS platformer
===========================

An HTML5 rotating-tower platform game inspired by the old c64 game "Nebulus"

 * [read more about original](https://jakesgordon.com/writing/rotating-tower-platformer/)
 * [view the original source](https://github.com/jakesgordon/javascript-tower-platformer)

SUPPORTED BROWSERS
==================

Should work in any modern browser with canvas support

DEVELOPMENT
===========

The game is 100% client side javascript, html and css. It should run when served up by any web server.

FUTURE FEATURES
===============

 * ~~level exit~~ ✅
 * game menu
 * ~~multiple levels~~ ✅
 * ~~dissolving platforms~~ ✅
 * elevators
 * ~~shortcut doors~~ as ~~teleports~~ ✅
 * countdown timer
 * mobile touch support
 * sound fx and music
 * ~~animated coins~~ ✅
 * ~~features~~ ✅
 
 LEVEL DEVELOPMENT
=========
"e" (Exit): Last level final exit
"n" (Next): Entry to next level from list
"^" (Springboard): Place this sign to create an orange bounce block. Upon stepping on it, the player will be launched high into the air.
"t" (Teleport): Place at least two such points on the map. Upon stepping on one, the player will be teleported to the other. Thanks to the teleport cooldown, the player has time to exit the portal.
"d" (Disappearing Platform): This acts like a regular platform, but upon stepping on it, it begins to flash and disappears after less than a second, reappearing after 3 seconds.
"4" (Scorpion): This is a new enemy type in the MONSTERS table. It moves horizontally and fires red projectiles when the player reaches its height.


TECH DEBT
=========

 * should use an FSM to manage player state (standing/left/right/falling/climbing/hurt/etc)
 * allow monsters to overlap (make cell.monster an array instead of single object)
 * use images for tower gradient and platforms (instead of raw ctx stroke/fill calls)
 * direction-agnostic monster sprites (abstract)
 * tiny gap in ground rendering in FF/IE where image wraps (need to render image on (0.5, 0.5) boundaries)

License
=======

[MIT](http://en.wikipedia.org/wiki/MIT_License) license.

