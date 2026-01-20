<link rel="stylesheet" href="style.css">

# OBSOLETE: This version of FF Scouter has been replaced by https://ffscouter.com.

# DO NOT USE THIS VERSION, IT WILL NOT WORK!

# For historical purposes only: Fair Fight Scouter - For [Torn](https://www.torn.com/2670953), by [rDacted](https://www.torn.com/profiles.php?XID=2670953)

**Please read this document all the way though**

If this page looks broken and links don't work, make sure you're looking at it from the right address: [https://rdacted2.github.io/fair_fight_scouter](https://rdacted2.github.io/fair_fight_scouter)

Provides a quick and easy way to gauge how difficult a fight will be with an opponent.

It's very accurate as it works by comparing your battle score against a database containing battle scores of other players. If the other player has a recent (or current) score the calculated fight difficulty should be near exact.

**NOTE** This script has been integrated into TornTools. If you have TornTools you won't need this script - just enable FF Scouter in the TornTools settings.

I've also quit Torn to focus on other areas of my life. This script is now powered by TornPal, and hopefully the bulk of this script won't need any maintenance. If you're interested in continuing the development of this script please feel free to fork this project or develop your own using the TornPal backend.

Discord server: [TornPal](https://discord.gg/HBgVjs8aVe)

Quick installation links - try the first one and move down the list if it doesn't work. Browsers should only need the first one. Torn PDA may require a few options depending on where you're clicking from
 * [https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)
 * [tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)
 * [https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter.user.js](https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter.user.js)

If you're wanting to participate in the beta test releases then these are the links you'll want:

Quick beta installation links - again try the first one and move down if it doesn't work:
 * [https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter_beta.user.js](https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter_beta.user.js)
 * [tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter_beta.user.js](tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter_beta.user.js)
 * [https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter_beta.user.js](https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter_beta.user.js)


# Table of Contents

 * [Description](#description)
 * [Installation](#installation)
   * [Desktop Installation](#desktop)
   * [TornPDA Installation](#tornpda)
 * [Additional Features](#additional-features)
 * [Frequently Asked Questions](#frequently-asked-questions)
 * [Obligatory Warning](#obligatory-warning)

# Description

The Fair Fight Scouter shows you how difficult a fight would be between yourself and that opponent. This is shown as a value named the “Fair Fight” (FF) value which is a number which represents how your battle score relates to their battle score.

   | Fair Fight Value | Expected Difficulty  |
   | :----            | :----                |
   | 1                | Extremely easy       |
   | 2                | Easy                 |
   | 2.5-3.5          | Moderately difficult |
   | 3.5-4.5          | Difficult            |
   | 4.5+             | May be impossible    |

(Just make sure it's not [over 9000](https://www.youtube.com/shorts/nl7M--nfQX0))

The actual difficulty you experience will be greatly affected by other factors such as how your build performs against their build, applicable buffs/debuffs and equipment used.

By knowing the FF value of your opponent you can get an accurate estimate of how likely you would win in a fight with them. This makes it an effective way to know which bounties could be collected safely and which to avoid.

When installed correctly you will see the fair-fight estimate at the top of a players profile page

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/profile_view.png" width="600"/>
</p>

As well as a new column when looking at factions

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/faction_view.png" width="400"/>
</p>

The numbers indicate the fair-fight range. The number should fall into one of these categories

* A single number
  * Means the fair fight value is expected to be exact
* A range
  * Means there’s some amount of uncertainty, but the FF value should fall within this range


The numbers can have some characters after it

* A question mark (?)
  * Indicates that the battle score is over 2 weeks old. Check the player’s last known activity to determine if they may have trained since the battle score was taken.
* A plus (+)
  * Indicates that only the lower bound is known. They are at least the specified value, but could be much more.
* A plus with a question mark (+?)
  * Indicates that only the lower bound is known, and the player battle score is over 2 weeks old.

Additionally wherever you find a honor bar you may also find an arrow indicating the Fair-Fight score for that individual.

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/honorview_1.png"/>
</p>

The arrow points to three different regions of the honorbar: easy, medium and hard. The regions are separated by small black bars.

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/honorview_2.png"/>
</p>

Long-pressing on the honor bar will bring up a mini-profile, and the fair-fight details have been added there too

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/mini.png"/>
</p>

Viewing the information in the mini profile will also show you how fresh the data is - so you can make a determination for how correct the value is likely to be.

# Installation

## Desktop

1. Install Tampermonkey or equivalent (Firefox needs tampermonkey to work)
2. Browse to: [https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)
3. You should see something similar to the following:

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/tamper_install.png" width="800"/>
</p>

4. Click Install
5. Navigate to any user profile on torn, such as yourself. It should indicate that a limited API key is needed. Click and enter your key

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/api_key_needed.png" width="600"/>
</p>

6. The script is now installed. Test it out by looking at different faction and member profiles.

### Troubleshooting

If you don't see the request for a limited API key, and you're using TamperMonkey on a Chrome based browser, then you're likely affected by a tampermonkey issue which requires developer mode to be enabled. Please follow the instructions on this link to enable it: [https://www.tampermonkey.net/faq.php?locale=en#Q209](https://www.tampermonkey.net/faq.php?locale=en#Q209) Otherwise ViolentMonkey is an alternative browser extension which seems to work well for both desktop and mobile (such as kiwi browser)

## TornPDA

Try this link first. Clicking it should trigger TornPDA to prompt to install the script [https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)

If that fails, try this link: [tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](tornpda://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)

If that fails, try this link: [https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter.user.js](https://kwack.dev/script-install?gmFix=false&scriptUrl=http%3A%2F%2Frdacted2.github.io%2Ffair_fight_scouter%2Ffair_fight_scouter.user.js)

If neither of those links work then please let rDacted know and try the following steps instead

1. Copy this URL into your paste buffer: [https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js](https://rdacted2.github.io/fair_fight_scouter/fair_fight_scouter.user.js)

2. Open TornPDA and go to settings

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/1_Settings.png" width="400"/>
   </p>

3. Advanced browser settings

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/2_Advanced_Browser_Settings.png" width="400"/>
   </p>

4. Manage scripts

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/3_Manage_Scripts.png" width="400"/>
   </p>

5. The \+ near the top

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/4_Add_Script.png" width="400"/>
   </p>

6. Configure

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/5_Configure.png" width="400"/>
   </p>

7. Paste the URL into the “Remote URL” bar at the top. Press Fetch. Then once the source is loaded below, press Load

   <p align="center" width="100%">
   <img src="https://rdacted2.github.io/fair_fight_scouter/images/6_Fetch_And_Load.png" width="400"/>
   </p>

8. The script is now installed. Test it out by looking at different faction and member profiles

# Additional Features

## Promotional extras

On occasion there will be extra features available to users of FF Scouter.

You can find these features by looking for the 'FF Scouter Extras' entry below the Settings entry under your profile image on the top right of the screen.

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/extras.png" width="400"/>
</p>

This will bring up a new tab showing the currently available extras.

This may include a list of 10,000 inactive targets for you to attach during Halloween. No need to search for targets when you have a large list you can select from!

It may also include a short chain list, to demonstrate the accuracy and usefulness of a proper chain list, which you can purchase through [rDacted](https://www.torn.com/profiles.php?XID=2670953) The short chain list will have a lifespan of two weeks, and when it expires it will generate a new one automatically.

## Chain support

In order to encourage high-respect hits during chains (and to a lesser extent, wars) the chain page can be colour coded to highlight the FF value of each hit made.

It can be disabled by clicking on the 'Toggle colours' link below the 'Recent attacks' label on that page.

Hits made with a perfect 3.0 FF are highlighted with green sparkles
Otherwise values made between 3.0 downwards are given various shades of green to brown
During chains and wars, however, any hits at 1.3FF or below are given a special poop emoji background to encourage hitting higher respect targets.

Green Sparkles

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/lime_green_stars.gif" width="600">
</p>

Poop

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/poop.gif" width="600">
</p>

Example chain view

<p align="center" width="100%">
<img src="https://rdacted2.github.io/fair_fight_scouter/images/chain_example.png" width="800"/>
</p>

# Frequently Asked Questions

## I'm concerned about giving you my api key. Why don't you do everything in script? Why send the api key to your server at all?

There are actually several reasons.

1. Firstly to prevent abuse I need to authenticate the requests somehow and identify the user. The easiest way to do this is to use an api key.
2. In order to calculate the FF value of a fight between yourself and your opponent I need your battle score, and it needs to be accurate
3. The database is populated with battle scores collected through the accurate calculation of recent battles. If the userscript pulled the attack logs and fed them to the server I would also need to somehow ensure it isn't maliciously modified to poison the database. It's a lot easier for me to pull the logs from the torn api than for me to sent logs by torn users and somehow architect a system thats resistant to a few users who may desire to abuse the system by feeding me fraudlent results.
4. It's actually easier for me to do everything in the backend. Doing everything in the userscript is challenging. It needs to be in javascript, using standard libraries, running in multiple tabs, in various browsers, possibly using old or broken versions of my userscript. In contrast the backend can be any technology stack I want, using any libraries, running in a controlled environment which I can update and synchronise as required. It's significantly easier to put the work into the backend and leave the frontend as light as possible.

The main reason I suspect this is asked is because people are worried about sending their api key to an external service. I understand this concern and suggest the following for consideration:

1. If I were doing anything improper with these keys then I expect I will be fedded pretty quickly, and I'm keen for that not to happen.
2. The keys don't have to be limited keys, they can be custom keys to limit your exposure. The only thing the key is needed for is to pull your battle stats and see your attack history (and to identify who you are). If you're interested in making a custom key then read the obligatory warning section which describes how to do that.
3. Your key isn't stored anywhere on my system. At most it's held in memory for as long as required, and hashed with a salt so I can locally validate your key without constantly hitting torn servers (note that the process of hashing your api key with a salt makes it practically irreversible, so I can store it and not worry about anyone taking the value and extracting your api_key from it)

## How frequently will you use my key?

Your key is primarily required to pull back your attack logs and battle score. It should be used once every 10 minutes or so.

## How do I remove my key from your server?

Easy! Your key isn't retained on the server. If you want my server to stop using your key then all you need to do is uninstall FF Scouter.

## Why do you need to pull down my attack logs?

Your attack logs are used to populate the battle score database for all players in torn. Regardless of whether you attack them or they attack you, the outcome of a successful fight means that I can get information about your opponent to store their information in my database.

## Why do you need my battle score?

Your battle score is required to figure out the battle score of your opponent. You can find out the relationship between the fair fight value and the two battle scores here: [https://wiki.torn.com/wiki/Chain\#Fair\_fights](https://wiki.torn.com/wiki/Chain\#Fair\_fights)

## Isn’t the battle score private information?

Your battle stats are somewhat private because they reveal your build, eg whether you’re balanced or dex-heavy or otherwise. However the battle score is each of your stats square rooted and then added together. This means that knowing your battle score gives your opponent no information as to what sort of build you’ve made.

Also your battle score can be calculated by any of the people you’ve fought in the past. It’s easily obtainable if you know the battle score of one of the combatants. Therefore while the battle stats are somewhat private, the battle score is essentially public information.

## Why isn’t a FF value showing for all targets?

It’s likely the person you’re looking at isn’t in my battle score database. If you defeat them (or they defeat you) then they should be added within a few hours.

## Why show a \+ at the end, how is that different to a question mark?

A question mark shows that the battle score is over 2 weeks old \- therefore you need to check whether the target has been active since then to determine if it’s still likely to be accurate.

Conversely values with a \+ at the end are likely to be inaccurate. This is because the fair-fight value of all fights is capped at 3.0. So when a target with a real fair-fight value higher than 3.0 is defeated my tools can’t tell how much higher it was over the 3.0. So it’s able to determine the floor for the targets battle score, but not the ceiling. As such, take any FF scores ending with a \+ as being very likely to be lower than the real value \- even if it was freshly taken.

## Why is this free?

I could charge for it, but that would slow adoption. I’d rather make something that gets great support from most people to populate my database faster. With a larger database I’m able to create better/more accurate chaining lists for people, which I can then sell. Of course you could make your own chain list if you wanted (by just browsing) but I’m hoping some people will pay for the convenience

# Obligatory Warning

This script requires a limited access api key, or a custom key generated with the following permissions
[https://www.torn.com/preferences.php\#tab=api?step=addNewKey\&title=rDacted\&user=basic,attacks,battlestats](https://www.torn.com/preferences.php\#tab=api?step=addNewKey\&title=torn\&user=basic,attacks,battlestats)
(TornPDA users won’t need to provide a key as it will use the key that TornPDA automatically provides to installed userscripts)

Your key is sent to a backend service which does the following

* Obtains your identity (for authentication)
* Obtains your battle stats
* Looks at your attack history

For the sake of your privacy, the following restrictions are observed

* Your key is not stored on the server
* Your battle stats are converted into a single battle score, which is the summation of the square root of each of your four stats. This information is not private, as it's leaked anytime you make an attack (or are attacked)
* The only data I use from the attack log is the identity of your opponent and the fair-fight value of the fight

Full disclosure
I have a separate service that I provide to unmask stealth attackers.
I DO NOT USE the attack data provided by your api key to find people you have attacked so I can report you to them.

I specifically released my stealth reveal capabilities to show that I can do it without any privileged access, and I promise not to abuse any privileged access provided to me by your key in order to reveal privileged information to any third party.

If I happen to reveal a stealthed attack you made against someone else, the source of that data is public information that everyone already has access to.

If you're concerned about sharing your battle score, note that anyone you defeat can calculate your battle score by simply using their own battle score and the fair-fight value of the attack to determine what your battle score is. It's not public information per se, but it's also not private.
