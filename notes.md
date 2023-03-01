1. SwiftUI’s introduction in 2019 created another opportunity for a paradigm shift in the industry. After years of using UIKit and AppKit to create user interfaces, SwiftUI presented a fresh, new way to create UI for your apps. In many ways, SwiftUI is much simpler and powerful than its predecessors, and even more, it is cross-platform over the Apple ecosystem.

2. One of the most important things, though, is SwiftUI’s declarative nature. For years, developers have worked with imperative programming models, dealing with state- management problems and complex code. But now, you have in your hands a declarative, straightforward way to build amazing user interfaces. And don’t worry; if you loved working with UIKit or AppKit, rest assured that you can integrate those frameworks with your SwiftUI code.

3. The `@main` attribute means this struct contains the entry point for the app. The App protocol takes care of generating the static main function that actually runs. When the app starts, it displays this instance of ContentView, which is defined in the `ContentView` file

`````
@main
struct AppName: App {
  var body: some Scene {
    WindowGroup {
      ContentView()
    }
} }
`````

* Whats a Scene?
* Whats a Window group?

4. The `padding()` modifier adds `10` points padding around the text. 

5. Canvas and Minimap: To get the full SwiftUI experience, you need at least Xcode 11 and macOS 10.15. Then you’ll be able to preview your app’s views in the canvas, alongside the code editor. Also available is a minimap of your code: It doesn’t appear in my screenshots because I unchecked it in Editor Options.

6. Modifiers: Instead of setting attributes or properties of UIKit objects, you can call modifier methods for foreground color, font, padding and a lot more.

7. Container views: If you’ve previously used stack views, you’ll find it pretty easy to create this app’s UI in SwiftUI, using HStack and VStack container views. There are other container views, including ZStack and Group. You’ll learn about them in Chapter 7: “Introducing Stacks & Containers”.

8. For the value property, you use @Binding instead of @State, because the ColorSlider view doesn’t own this data. It receives an initial value from its parent view and mutates it.

9. Every @State property is a source of truth, and views depend on state, not on a sequence of events.

10. What's a primitive view? Atomic Default View Elements, like Text and Color, that are used as the smallest building blocks for custom views.

11. What's a modifier? A modifier is a method that creates a new view from the existing view. You can chain modifiers like a pipeline to customize any view.

12. Is it costly to create new Views? No. SwiftUI collapses the modified view into an efficient data structure, so you get all the  creation and collapsation convenience with no visible performance hit.

13. How to duplciate a content preview?
    1. Click Duplicate preview or 
    2. Add a Group in `ContentPreview` and change `.previewDevice("iPhone X")` where desidered.

14. 

##### View Primitives

13. What are the type of Stacks and how to configure each?

14. What's SafeArea and how to ignore it?

15. Whats the defauld applied padding()? 10 points.

16. Does the order of modifiers matter? 
When you apply more than one modifier to a view, sometimes the order matters.
Modifiers like padding and frame change the view’s layout or position. Modifiers like background or border fill or wrap a view. Normally, you want to set up a view’s layout and position before you fill or wrap it.

17. What does Capsule means?

18. What is GeometryReader and how does it work?

18. What is GeometryProxy and how does it work?

19. How to read value form text in test env?
Set `.accessibility(identifier: <id>)`
This method sets the accessibilityIdentifer for the resulting UI element. Despite the name, VoiceOver doesn’t read the accessibilityIdentifer attribute; this simply provides a way to give a UI element a constant label for testing.

20. How to retrieve UI elements in a UI Test? acessing app properties, such as `app.buttons[:]`

21. How to launch an app in test env?
```
Import XCTest

final class TestClass: XCTestCase {
    func test<Name>() {
        let app = XCUIApplication()
        app.launch()
    }
}
```

22. How to add a DragGesture to a View? 
````
let dragGesture = DragGesture()
.gesture(dragGesture)
````

23. How to test a drag gesture in a test?
`````
<XCUIElement>.swipe<Up, Down, Left, Right>
`````

24. 

##### Random

x. What are EnvironmentValues? https://developer.apple.com/documentation/swiftui/environmentvalues

x. What's neumorphism? Neumorphism is the new skeumorphism. It’s easy to implement with color sets and the SwiftUI shadow modifier.

x. What's Catalyst?

x. How to add breakpoints with keyboard? `CMD + \`

x. What's XCTest and what capabilities does it contain? 

x. Why tests that don't assert anything are considered green? Because non-failing tests are considered passing tests.

