# What Is New In SwiftUI - WWDC22 - iOS
By [Big Mountain Studio](https://www.bigmountainstudio.com/)

A list of everything new and deprecated for SwiftUI after WWDC 2022.
(Note: I don't list things that have been updated.)

# Working with Data
## Environment Values
### New
* [accessibilityQuickActionsEnabled](https://developer.apple.com/documentation/swiftui/environmentvalues/accessibilityquickactionsenabled) - Shows quick action bar.
* [renameAction](https://developer.apple.com/documentation/swiftui/environmentvalues/rename) - Activates standard rename action.
* [menuOrder](https://developer.apple.com/documentation/swiftui/environmentvalues/menuorder) - The preferred order of items for menus.
* [searchSuggestionsPlacement](https://developer.apple.com/documentation/swiftui/environmentvalues/searchsuggestionsplacement) - The current placement of search suggestions.
* [isScrollEnabled](https://developer.apple.com/documentation/swiftui/environmentvalues/isscrollenabled) - Can or can't scroll.
* [horizontalScrollIndicatorVisibility](https://developer.apple.com/documentation/swiftui/environmentvalues/horizontalscrollindicatorvisibility) - Can or can't see horizontal scroll indicators.
* [verticalScrollIndicatorVisibility](https://developer.apple.com/documentation/swiftui/environmentvalues/verticalscrollindicatorvisibility) - Can or can't see vertical scroll indicators.
* [scrollDismissesKeyboardMode](https://developer.apple.com/documentation/swiftui/environmentvalues/scrolldismisseskeyboardmode) - Dismiss keyboard when scrolling, never, automatically based on context or allow user to choose.
* [supportsMultipleWindows](https://developer.apple.com/documentation/swiftui/environmentvalues/supportsmultiplewindows) - Check if platform allows multiple windows.
* [displayStoreKitMessage](https://developer.apple.com/documentation/swiftui/environmentvalues/displaystorekitmessage) - Tells StoreKit to display an App Store message
* [requestReview](https://developer.apple.com/documentation/swiftui/environmentvalues/requestreview) - Ask user to review your app.
* [autocorrectionDisabled](https://developer.apple.com/documentation/swiftui/environmentvalues/autocorrectiondisabled) - Allow auto-correct or not.
* [backgroundStyle](https://developer.apple.com/documentation/swiftui/environmentvalues/backgroundstyle) - Overrides the default system background style.
* [contentTransition](https://developer.apple.com/documentation/swiftui/environmentvalues/contenttransition) - Method of animating the contents of views.
* [contentTransitionAddsDrawingGroup](https://developer.apple.com/documentation/swiftui/environmentvalues/contenttransitionaddsdrawinggroup) - Transition with GPU-acceleration or not.
* [showsWidgetLabel](https://developer.apple.com/documentation/swiftui/environmentvalues/showswidgetlabel) - Tells you if you can or can't display an accessory label.
### Deprecated
* disableAutocorrection
* sizeCategory
* presentationMode

# SwiftUI Views
## Accessibility Modifiers
* [accessibilityActions](https://developer.apple.com/documentation/swiftui/view/accessibilityactions(_:)) - Adds multiple accessibility actions to the view.
* [accessibilityQuickAction](https://developer.apple.com/documentation/swiftui/view/accessibilityquickaction(style:content:)) - Adds a quick action to be shown by the system when active.
* [AccessibilityQuickActionStyle](https://developer.apple.com/documentation/swiftui/accessibilityquickactionstyle) - Presentation style of an accessibility quick action. (Outline, Prompt)
## Appearance Modifiers
* [backgroundStyle](https://developer.apple.com/documentation/swiftui/view/backgroundstyle(_:)) - Sets the specified style to render backgrounds within the view.
* [tint(ShapeStyle](https://developer.apple.com/documentation/swiftui/view/tint(_:)-93mfq) - Sets the tint within this view.
* [scrollDisabled](https://developer.apple.com/documentation/swiftui/view/scrolldisabled(_:)) - Disables or enables scrolling in scrollable views.
* [menuOrder](https://developer.apple.com/documentation/swiftui/view/menuorder(_:)) - The preferred order of items for menus. (Fixed, Priority)
* [persistentSystemOverlays](https://developer.apple.com/documentation/swiftui/view/persistentsystemoverlays(_:)) - Preferred visibility of the non-transient system views overlaying the app.
* [scrollIndicators(_:axes:)](https://developer.apple.com/documentation/swiftui/view/scrollindicators(_:axes:)) - Sets the visibility of scroll indicators within this view.
* [widgetAccentable](https://developer.apple.com/documentation/swiftui/view/widgetaccentable(_:)) - Adds view and all subviews to the accented group.
* [widgetLabel](https://developer.apple.com/documentation/swiftui/view/widgetlabel(_:)-7wguh) - Returns a text label that displays additional content outside the accessory family widget’s main SwiftUI view.
## Text and Symbol Modifiers
Many of the modifiers that were just for Text can now be applied to any view and all Text within will adopt the modifier.

* [bold(isActive:)](https://developer.apple.com/documentation/swiftui/view/bold(_:)) - Applies bold to views when isActive is true.
* [fontWeight](https://developer.apple.com/documentation/swiftui/view/fontweight(_:)) - Can now be applied to views (not just Text).
* [italic(isActive:)](https://developer.apple.com/documentation/swiftui/view/italic(_:)) - Applies italics to views when isActive is true.
* [strikethrough(_:pattern:color:)](https://developer.apple.com/documentation/swiftui/view/strikethrough(_:pattern:color:)) - Can now be applied to views (not just Text).
* [underline(_:pattern:color:)](https://developer.apple.com/documentation/swiftui/view/underline(_:pattern:color:)) - Can now be applied to views (not just Text).
* [baselineOffset](https://developer.apple.com/documentation/swiftui/view/baselineoffset(_:)) - Vertical offset that can now be applied to views (not just Text).
* [kerning](https://developer.apple.com/documentation/swiftui/view/kerning(_:)) - Spacing between characters that can now be applied to views (not just Text).
* [tracking](https://developer.apple.com/documentation/swiftui/view/tracking(_:)) - Spacing between all characters that can now be applied to views (not just Text).
* [lineLimit](https://developer.apple.com/documentation/swiftui/view/linelimit(_:)-7ufty) - Line limit can now be applied to Text AND a vertical TextField.
* [autocorrectionDisabled](https://developer.apple.com/documentation/swiftui/view/autocorrectiondisabled(_:)) - Used to be disableAutoCorrection on TextField. Can be applied to any view now.
* [scrollDismissesKeyboard](https://developer.apple.com/documentation/swiftui/view/scrolldismisseskeyboard(_:)) - Dismiss keyboard when scrolling, never, automatically based on context or allow user to choose.
* [findNavigator(isPresented:)](https://developer.apple.com/documentation/swiftui/view/findnavigator(ispresented:)) - Presents the find and replace interface for TextEditor views.
* [findDisabled](https://developer.apple.com/documentation/swiftui/view/finddisabled(_:)) - Prevents find and replace operations in a TextEditor.
* [replaceDisabled](https://developer.apple.com/documentation/swiftui/view/replacedisabled(_:)) - Prevents replace operations in a TextEditor.
## Navigation Modifiers

## Toolbar Modifiers

## Other Auxilary View Modifiers

# Animations Mastery


# Charts
