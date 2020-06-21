# Secure Browsers
The following list shows browsers that are capable of thwarting the technology implemented by nothing-private.
Be aware that this only covers one aspect the possibilities to track you online.

There are fundamentally two technologies to thwart fingerprinting implemented in nothing-private:

## Randomizing canvas data readout

Browsers implementing this approach randomize the readout of the canvas data obtainable by websites, making each read-out differ from the last.
Be aware that this opens up new fingerprinting opportunities as well as being easily detectable when the fingerprinting party checks for it.

Browsers that implement this approach include

| Browser | Platform | Version | Reported By |
| ------------- | ------------- | ------------- | ------------- |
| [BriskBard](https://www.briskbard.com/index.php?lang=en) | Windows| 1.6.9| [jatinsharma28](https://github.com/jatinsharma28)|
| [Pale Moon](https://www.palemoon.org/) [(See notes)](pale_moon_notes.md) | Windows/Linux | 28.5.2+ | [jragard](https://github.com/jragard) |
| [Ungoogled Chromium](https://github.com/Eloston/ungoogled-chromium) [(See notes)](ungoogled_chromium_notes.md) | Windows/Linux/Mac | 80.0.3987.149-2+ | [Nunbit](https://github.com/nunbit) |
| [Bromite](https://www.bromite.org/) | Android | v77+ | [Nunbit](https://github.com/nunbit) |

## Depriving websites of canvas data readout

This approach simply takes away the possibility to gain any information from the canvas read-out API alltogether by always blanking the returned value.
This in turn makes every browser look alike with regard to this property, but as it looks the same for every single browser, it is rendered entirely useless for tracking purposes.

Be aware that nothing-private may still look functional, but is rendered incapable of separating even entirely different browsers with this approach as every browser now looks the same with regards to the canvas property, see screenshot below.

![Firefox tracking in action](ff-trackingprotection.png)

Browsers that implement this approach include

| Browser | Platform | Version | Reported By |
| ------------- | ------------- | ------------- | ------------- |
| [Tor Browser](https://www.torproject.org/download/download) | Windows/Linux/Mac | 8.0.3+| [RickyRajinder](https://github.com/rickyrajinder) |
| [Firefox](https://www.mozilla.org/en-US/firefox/new/) | Windows/Linux/Mac/Android | v68+ | [cherti](https://github.com/cherti) |