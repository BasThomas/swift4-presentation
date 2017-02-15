slidenumbers: true
build-lists: true
autoscale: true

# [fit] **Swift �**

## Bas Broek
### @basthomas

^ Oops, something wrong here. We'll get into that.

---

# [fit] **Swift ④**

## Bas Broek
### @basthomas

^ That's better. Let's talk about Swift 4.

---

# [fit] Expected release date:
# **Late 2017**

^ So, first things first.

---

# Stage 1 & 2

---

# Stage 1

^ Source stability for Swift 3 code
^ ABI stability for the std lib
^ ... but "Reliability of the compiler, better error messages, faster compile times & scaling better to large projects *OVER* ABI for Swift 4"

---

# Strings

^ We know strings, right?

---

# 🤔

^ Right?

---

# No

^ Strings will change dramatically in Swift 4

---

# Strings in Swift 4
## Re-evaluate the API[^1]

- **How** to use internationalization API's correctly[^2]
- Better **unicode** support
- No more **`.characters`** for most operations
- Supporting `Range` **in favor of** `NSRange`
- Improved string **interpolation & formatting**
- ~~Regex~~

[^1]: https://github.com/apple/swift/blob/master/docs/StringManifesto.md

[^2]: Localization & internationalization itself are planned for Swift 5

^ Regex: "In the future, support for regular expression literals in the compiler could allow for compile time syntax checking and optimization." 🎉

---

# 🎉

---

# 😕

---

## [fit] What about source stability?

---

# SE-0141[^3] to the rescue

```swift
@available(swift 4, *)
extension Collection {
  func index(offset: IndexDistance) -> Index {
    return index(startIndex, offsetBy: offset)
  }
  func offset(of i: Index) -> IndexDistance {
    return distance(from: startIndex, to: i)
  }
}
```

[^3]: https://github.com/apple/swift-evolution/blob/master/proposals/0141-available-by-swift-version.md

---

# 🎉

---

# Stage 2
### "Some time in Spring 2017"

^ ... so that's between the end of March and end of June.

---

# [fit] Swift-evolution[^4]

[^4]: https://apple.github.io/swift-evolution/

^ Pretty much the resource for Stage 2.
^ Has some awesome filtering options as well.

---

# What is upon us?[^5]

- Enforce calling **super**
- **Multi-line** string literals
- User-provided warning diagnostics **at compile time**
- The **pipeline** (`|>`) operator
- Increased Objective-C & Swift **interoperability**
- Much more once Stage 2 starts...

[^5]: https://github.com/apple/swift-evolution/pulls?utf8=✓&q=label%3A%22out%20of%20scope%20for%20current%20release%22

^ In no particular order

---

# And of course...

- **Swift Package Manager** improvements[^6]
- Swift on the **server**[^7]
- ???

[^6]: https://lists.swift.org/pipermail/swift-evolution-announce/2017-January/000307.html

[^7]: https://github.com/swift-server

^ Introduce Swift Weekly Brief @ "???"

---

# *WORLD* **DOMINATION**

^ And as Chris Lattner said in the ATP podcast... "Obviously, I care a lot about Swift and I really want it to get to its goal of world domination."

^ He said it more casually, though

---

## **@basthomas**
## @swiftlybrief[^8]

[^8]: https://swiftweekly.github.io