# Catching errors

After the `catch` keyword, place the enum of the error alongside which case it is, to pin down exactly what error occured.

```swift
enum Mistake: Error {
  case miscounted
  case misread
}

func checkForMistakes() throws {
  throw Mistake.misread
}

do {
  try checkForMistakes()
}
catch Mistake.miscounted {
  print("You miscounted")
}
catch Mistake.misread {
  print("You misread")  // prints "You misread"
}
catch {
  print("Something's off")
}
```
