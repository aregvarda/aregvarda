### Hey there <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="25px">

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
