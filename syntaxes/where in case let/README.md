# `Where` statements in `case let`

```swift
func checkIfCooked2(for pasta: PastaTypesA) {
  switch pasta {
  case .spaghetti(let cookingTime) where cookingTime >= 8:
    print("Spaghetti is cooked, take it out of the water!")
  default: print("Pasta is not cooked.")
  }
}
checkIfCooked2(for: .spaghetti(cookingTime: 7))
```
