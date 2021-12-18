### Hey there <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">

<a href="https://career.habr.com/aregv">
  <img align="left" alt="Areg's Habr" width="24px" src="https://cdn.icon-icons.com/icons2/2389/PNG/512/habr_logo_icon_145210.png" />
</a>
<a href="https://twitter.com/aregvardani">
  <img align="left" alt="Areg's | Twitter" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/twitter.svg" />
</a>
<a href="https://www.linkedin.com/in/areg-vardanian-b21b34225">
  <img align="left" alt="Areg's LinkedIN" width="22px" src="https://raw.githubusercontent.com/peterthehan/peterthehan/master/assets/linkedin.svg" />
</a>
<a href="https://open.spotify.com/playlist/2L0AQS408a0bGKsYDEWsBx?si=1bb340613a3446e3">
  <img align="left" alt="Areg's Spotify" width="24px" src="https://www.freeiconspng.com/uploads/spotify-icon-0.png" />
</a>
<a href=aregvarda@gmail.com>
  <img align="left" alt="Areg's Gmail" width="24px" src="https://img.icons8.com/color/50/000000/gmail-new.png" />
</a>
<a href="https://github.com/aregvarda">
  <img align="left" alt="Areg's Counter" src="https://visitor-badge.glitch.me/badge?page_id=aregvarda.aregvarda" />
</a>

<br>
<br>

```swift

import Foundation

struct Profile: CustomStringConvertible {
    
    let name = "Areg Vardanian"
    
    var description: String {
        """
        \(name)\n
        I am an iOS developer.
        Working on teams with project managers, developers, 
        and designers, I have built mobile applications and 
        SDKs focused on excellent user experience and design.
        I am looking to work in a collaborative environment 
        where I can develop products that improve people's lives.\n
        """
    }
    
    enum Skill: String, CaseIterable {
        case swift, uIKit, swiftUI
        case testing, git
        case creativity, tolerance, effectiveness
    }
    
    func proficient(in skills: [Skill] = Skill.allCases) -> String {
        skills
            .map(\.rawValue)
            .map(\.capitalized)
            .map { "- " + $0 + "\n" }
            .reduce("Skills: \n", +)
    }
}

// Paste into a playground!
let profile = Profile()
print(profile.description)
print(profile.proficient())

```
