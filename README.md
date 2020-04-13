# Alex's 100DaysOfSwiftUI

Logging my progress of the 100DaysSwiftUI challenge

## Track Course

### Introduction to Swift

- [ ] Day 1 - 
- [ ] Day 2 - 
- [ ] Day 3 - 
- [ ] Day 4 -
- [ ] Day 5 -
- [ ] Day 6 -
- [ ] Day 7 - 
- [ ] Day 8 -
- [ ] Day 9 -
- [ ] Day 10 -
- [ ] Day 11 -
- [ ] Day 12 -

### Consolidation I

- [ ] Day 13 -
- [ ] Day 14 -
- [ ] Day 15 -

### Starting SwiftUI

- [ ] Day 16 -
- [ ] Day 17 - 
- [ ] Day 18 -
- [ ] Day 19 -
- [ ] Day 20 -
- [ ] Day 21 -
- [ ] Day 22 -
- [ ] Day 23 -
- [ ] Day 24 -

### Consolidation II

- [ ] Day 25 -

### Expanding your skills

- [ ] Day 26 -
- [ ] Day 27 -
- [ ] Day 28 -
- [ ] Day 29 -
- [ ] Day 30 -
- [ ] Day 31 -
- [ ] Day 32 -
- [ ] Day 33 -
- [ ] Day 34 -

### Consolidation III

- [ ] Day 35 -

### Scaling up to bigger apps

- [ ] Day 36 -
- [ ] Day 37 -
- [ ] Day 38 -
- [ ] Day 39 -
- [ ] Day 40 -
- [ ] Day 41 -
- [ ] Day 42 - 
- [x] Day 43 - Project 9, Part one
- [ ] Day 44 - Project 9, Part two
- [ ] Day 45 - Project 9, Part three
- [ ] Day 46 - Project 9, Part four

### Consolidation IV

- [ ] Day 47 -
- [ ] Day 48 -

### Focus on data

- [ ] Day 49 -
- [ ] Day 50 -
- [ ] Day 51 -
- [ ] Day 52 -
- [ ] Day 53 -
- [ ] Day 54 -
- [ ] Day 55 -
- [ ] Day 56 -
- [x] [Day 57](https://www.hackingwithswift.com/100/swiftui/57) - [Project 12 - Part 1](#Day-57)
- [ ] Day 58 -
- [ ] Day 59 -

### Consolidation V

- [ ] Day 60 -
- [ ] Day 61 -

### Views and view controllers

- [ ] Day 62 -
- [ ] Day 63 -
- [ ] Day 64 -
- [ ] Day 65 -
- [ ] Day 66 -
- [ ] Day 67 -
- [ ] Day 68 -
- [ ] Day 69 -
- [ ] Day 70 -
- [ ] Day 71 -
- [ ] Day 72 -
- [ ] Day 73 -
- [ ] Day 74 -
- [ ] Day 75 -
- [ ] Day 76 -

### Consolidation VI

- [ ] Day 77 -
- [ ] Day 78 -

### Controlling UI flow

- [ ] Day 79 -
- [ ] Day 80 -
- [ ] Day 81 -
- [ ] Day 82 -
- [ ] Day 83 -
- [ ] Day 84 -
- [ ] Day 85 - 
- [ ] Day 86 -
- [ ] Day 87 -
- [ ] Day 88 -
- [ ] Day 89 -
- [ ] Day 90 -
- [ ] Day 91 -
- [ ] Day 92 -
- [ ] Day 93 -
- [ ] Day 94 -

### Consolidation VII

- [ ] Day 95 -

### One last project

- [ ] Day 96 -
- [ ] Day 97 -
- [ ] Day 98 -
- [ ] Day 99 - 

### Wrap up

- [ ] Day 100 -


## Project 9 - Drawing

*“I sometimes think there is nothing so delightful as drawing.”* - Vincent Van Gogh

### [Day 43](https://www.hackingwithswift.com/100/swiftui/43)

#### [Drawing: Introduction](https://www.hackingwithswift.com/books/ios-swiftui/drawing-introduction)

- SwiftUI uses the following frameworks for performing drawing: Core Animation and Metal. These 2 are almost interchangeable depending on your use case.

#### [Creating custom paths with SwiftUI](https://www.hackingwithswift.com/books/ios-swiftui/creating-custom-paths-with-swiftui)

- Path is a low level API for drawing custom shapes, aka “the building block”. Usually you are going to wrap it inside another View to make it more useful.

#### [Paths vs shapes in SwiftUI](https://www.hackingwithswift.com/books/ios-swiftui/paths-vs-shapes-in-swiftui)

- Paths are a single purpose object for creating paths :]
- Shapes focus on reusability in mind because of:
  - flexible drawing space
  - custom init parameters for further customization

- **Warning** shapes measure their coordinates from bottom-left rather than top-left

#### [https://www.hackingwithswift.com/books/ios-swiftui/adding-strokeborder-support-with-insettableshape](https://www.hackingwithswift.com/books/ios-swiftui/adding-strokeborder-support-with-insettableshape)

- SwiftUI draws its border from the centerline both inwards & outwards, therefore the shape’s border expand beyond the frame by half its lineWidth. Use strokeBorder to draw borders inside.


## Project 12 - CoreData Deep Dive

*"succes is neither magical nor mysterious, success is the natural consequence of consistenly applying the basic fundamentals"* - Jim Rohn

### [Day 57](https://www.hackingwithswift.com/100/swiftui/57)

#### [Core Data: Introduction](https://www.hackingwithswift.com/books/ios-swiftui/core-data-introduction)

- **Warning**: Xcode ignores changes made inside the CoreData editor -> make a habit out of pressing CMD+S to save files (experienced this myself, not funny 😤)

#### [Why does \.self work for ForEach?](https://www.hackingwithswift.com/books/ios-swiftui/why-does-self-work-for-foreach)


#### [Creating NSManagedObject subclasses](https://www.hackingwithswift.com/books/ios-swiftui/creating-nsmanagedobject-subclasses)


#### [Conditional saving of NSManagedObjectContext](https://www.hackingwithswift.com/books/ios-swiftui/conditional-saving-of-nsmanagedobjectcontext)

- Sometimes it’s common to bulk saves together, which has a lower performance impact.
- Apple specifically states that you should always check for uncommitted changes before calling **save()**, to avoid unnecessary work
- Every managed object and context variables are given a **hasChanges** property 

```swift
if self.moc.hasChanges {
    try? self.moc.save()
}
```
- Even though this is a small change, over it adds up and it will make a big difference


#### [Ensuring Core Data objects are unique using constraints](https://www.hackingwithswift.com/books/ios-swiftui/ensuring-core-data-objects-are-unique-using-constraints)

