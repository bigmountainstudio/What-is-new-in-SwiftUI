# What's New In SwiftUI for iOS Cheat Sheet - WWDC22
By [Big Mountain Studio](https://www.bigmountainstudio.com/)

A list of everything new in SwiftUI after WWDC 2022.

# Working with Data
## Environment Values
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

# SwiftUI Views
## New Controls
* [AnyLayout](https://developer.apple.com/documentation/swiftui/anylayout/) - A view that can represent a container view such as a VStack, HStack, grids, etc.
* [Gauge](https://developer.apple.com/documentation/swiftui/gauge) - A view that shows a value within a range. This can be circular or straight.
* [Grid](https://developer.apple.com/documentation/swiftui/grid) - A container view that arranges other views in a two dimensional layout with the use of the [GridRow](https://developer.apple.com/documentation/swiftui/gridrow).
* [LabeledContent](https://developer.apple.com/documentation/swiftui/labeledcontent/) - A container for attaching a label to a value-bearing view. This way it can layout appropriately depending on where it's used. For example, if in a Form, the label will be leading and the content portion will be trailing and gray.
* [Layout](https://developer.apple.com/documentation/swiftui/gridrow) - Not exactly a new control but rather a new protocol that you can conform to so you can create your own custom layout container control.
* [MultiDatePicker](https://developer.apple.com/documentation/swiftui/multidatepicker) - A control for picking multiple dates.
* [NavigationStack](https://developer.apple.com/documentation/swiftui/navigationstack) - A view that displays a root view and enables you to present additional views over the root view. To navigate, use a NavigationLink in combination with the [navigationDestination](https://developer.apple.com/documentation/swiftui/view/navigationdestination(for:destination:)) modifier. You can also specify a [NavigationPath](https://developer.apple.com/documentation/swiftui/navigationpath) to create or manage your stack of views.
* [NavigationSplitView](https://developer.apple.com/documentation/swiftui/navigationsplitview) - A container that presents 2 or 3 views in columns. (sidebar, content, detail)
* [RenameButton](https://developer.apple.com/documentation/swiftui/renamebutton) - A button that triggers a standard rename action. Used with the renameAction modifier.
* [ShareLink](https://developer.apple.com/documentation/swiftui/sharelink) - A view that controls a sharing presentation.
* [Table](https://developer.apple.com/documentation/swiftui/table) - A container that presents rows of data arranged in one or more columns, optionally providing the ability to select one or more members, sort data, and style it.
* [ViewThatFits](https://developer.apple.com/documentation/swiftui/viewthatfits) - A container view that adapts to the available space by providing the first child view that fits.


## Updated Controls
### NavigationLink
* Works in combination with the [navigationDestination](https://developer.apple.com/documentation/swiftui/view/navigationdestination(for:destination:)) modifier. NavigationLinks have values and if there is a navigationDestination modifier that matches the NavigationLink's value type, then it is used and navigates to the view the navigationDestination specifies.

### Stepper
* You can provide a [format](https://developer.apple.com/documentation/foundation/parseableformatstyle) parameter to handle conversions for number, percent, dateTime, iso8601 date format and now URL format.

### Toggle
* You can bind a Toggle to an array of values.
* Multiple Text views within will be arranged hierarchically. (Second line less prominent than first line.)


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
* [scrollIndicators(:axes:)](https://developer.apple.com/documentation/swiftui/view/scrollindicators(_:axes:)) - Sets the visibility of scroll indicators within this view.
* [widgetAccentable](https://developer.apple.com/documentation/swiftui/view/widgetaccentable(_:)) - Adds view and all subviews to the accented group.
* [widgetLabel](https://developer.apple.com/documentation/swiftui/view/widgetlabel(_:)-7wguh) - Returns a text label that displays additional content outside the accessory family widget’s main SwiftUI view.

## Text and Symbol Modifiers
Many of the modifiers that were just for Text can now be applied to any view and all Text within will adopt the modifier.

* [bold(isActive:)](https://developer.apple.com/documentation/swiftui/view/bold(_:)) - Applies bold to views when isActive is true.
* [fontWeight](https://developer.apple.com/documentation/swiftui/view/fontweight(_:)) - Can now be applied to views (not just Text).
* [italic(isActive:)](https://developer.apple.com/documentation/swiftui/view/italic(_:)) - Applies italics to views when isActive is true.
* [strikethrough(:pattern:color:)](https://developer.apple.com/documentation/swiftui/view/strikethrough(_:pattern:color:)) - Can now be applied to views (not just Text).
* [underline(:pattern:color:)](https://developer.apple.com/documentation/swiftui/view/underline(_:pattern:color:)) - Can now be applied to views (not just Text).
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
* [navigationTitle(title:Binding)](https://developer.apple.com/documentation/swiftui/view/navigationtitle(_:)-7onr8) - Allows navigation title editing.
* [navigationTitle(:actions:)](https://developer.apple.com/documentation/swiftui/view/navigationtitle(_:actions:)-1jl6s) - Configures the navigation title with associated actions and a title.
* [navigationDocument](https://developer.apple.com/documentation/swiftui/view/navigationdocument(_:)-66zro) - Configures the view’s document for purposes of navigaiton.
* [navigationDestination](https://developer.apple.com/documentation/swiftui/view/navigationdestination(for:destination:)) - Associates a destination view with a presented data type for use within a navigation stack.

## Toolbar Modifiers
* [toolbar(:in:)](https://developer.apple.com/documentation/swiftui/view/toolbar(_:in:)) - Specifies the visibility of a bar managed by SwiftUI. (Place it automatically, bottom, navigation bar, tab bar or window toolbar.)
* [toolbarBackground](https://developer.apple.com/documentation/swiftui/view/toolbarbackground(_:in:)-1k7vw) - Customize the background style.
* [toolbarColorScheme](https://developer.apple.com/documentation/swiftui/view/toolbarcolorscheme(_:in:)) - Specifies the preferred color scheme (light or dark) of a bar.
* [toolbarRole](https://developer.apple.com/documentation/swiftui/view/toolbarrole(_:)) - Configures the semantic role (automatic, browser, editor, navigationStack) for the content populating the toolbar.

## Context Menu
* [contextMenu(menuItems:preview:)](https://developer.apple.com/documentation/swiftui/view/contextmenu(menuitems:preview:)) - Adds a context menu with a preview to a view.

## Style Modifiers
* [gaugeStyle](https://developer.apple.com/documentation/swiftui/view/gaugestyle(_:)) - Sets the style for gauges within this view. (New for iOS)
* [tableStyle](https://developer.apple.com/documentation/swiftui/view/tablestyle(_:)) - Sets the style for tables within this view. (New for iOS)
* [disclosureGroupStyle](https://developer.apple.com/documentation/swiftui/view/disclosuregroupstyle(_:)) - Sets the style for disclosure groups within this view.
* [navigationSplitViewStyle](https://developer.apple.com/documentation/swiftui/view/navigationsplitviewstyle(_:)) - Sets the style for navigation split views within this view.

## Grid Modifiers
* [gridCellColumns](https://developer.apple.com/documentation/swiftui/view/gridcellcolumns(_:)) - Tells a view that acts as a cell in a grid to span the specified number of rows.
* [gridCellAnchor](https://developer.apple.com/documentation/swiftui/view/gridcellanchor(_:)) - Custom alignment anchor for a view that acts as a grid cell. (top, topLeading, topTrailing, bottom, etc.)
* [gridCellUnsizedAxes](https://developer.apple.com/documentation/swiftui/view/gridcellunsizedaxes(_:)) - Asks grid layouts not to offer the view extra size in the specified axes (horizontal or vertical).
* [gridColumnAlignment](https://developer.apple.com/documentation/swiftui/view/gridcolumnalignment(_:)) - Overrides the default horizontal alignment of the grid column that the view appears in. 

## Input and Event Modifiers
* [SpatialTapGesture](https://developer.apple.com/documentation/swiftui/spatialtapgesture) - A gesture that recognizes one or more taps and reports their location.
* [onTapGesture(count:coordinateSpace:perform:)](https://developer.apple.com/documentation/swiftui/view/ontapgesture(count:coordinatespace:perform:)) - Adds a tap gesture within the specified coordinate space. The onTapGesture isn't new. But specifying the coordinate space is.
* [defersSystemGestures](https://developer.apple.com/documentation/swiftui/view/deferssystemgestures(on:)) - Sets the screen edge from which you want your gesture to take precedence over the system gesture.
* [defaultFocus](https://developer.apple.com/documentation/swiftui/view/defaultfocus(_:_:priority:)) - Default focus is evaluated by assigning a value to a given focus state binding.

## Searchable
There are over a dozen new searchable modifiers that can be used now. Rather than go through them all, I think it would be better to just list out some of the new parameters:
* **scope**: A binding for the active scope of the search field.
* **scopes**: A view builder representing the scopes of the search field which will be used to populate a Picker.
* **token**: A view builder that creates a view given an element in tokens.
* **tokens**: A collection of tokens to display and edit in the search field.
* **suggestedTokens**: A collection of tokens to display as suggestions.
* [SearchSuggestionsPlacement](https://developer.apple.com/documentation/swiftui/searchsuggestionsplacement) - A structure that defines ways in which search suggestions may be placed. (automatic, content, menu)

## Presentation Modifiers
* [presentationDetents](https://developer.apple.com/documentation/swiftui/view/presentationdetents(_:)) - Sets the available detents for the enclosing sheet. (medium, large, custom, fraction, height)
* [presentationDragIndicator](https://developer.apple.com/documentation/swiftui/view/presentationdragindicator(_:)) - Sets the visibility of the drag indicator on top of a sheet.
* [offerCodeRedemption](https://developer.apple.com/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:)) - Sheet that enables users to redeem subscription offer codes.

## State Modifiers
* [backgroundPreferenceValue](https://developer.apple.com/documentation/swiftui/view/backgroundpreferencevalue(_:alignment:_:)) - Reads the specified preference value from the view, using it to produce a second view that is applied as the background of the original view.
* [overlayPreferenceValue](https://developer.apple.com/documentation/swiftui/view/overlaypreferencevalue(_:alignment:_:)) - Reads the specified preference value from the view, using it to produce a second view that is applied as an overlay to the original view.

## Text Input & Output
### TextField
* The TextField can now overflow horizontally or vertically by specifying an [axis](https://developer.apple.com/documentation/swiftui/textfield/init(_:text:axis:)-7n1bm).
* A lienLimit modifier with one or a range of values can be added to specify how much the TextField can grow. Beyond that a scroll indicator will appear.
### TextEditor
* [findNavigator](https://developer.apple.com/documentation/swiftui/view/findnavigator(ispresented:)) - Programmatically presents the find and replace interface for text editor views.
* [findDisabled](https://developer.apple.com/documentation/swiftui/view/finddisabled(_:)) - Prevents find and replace operations in a text editor.
* [replaceDisabled](https://developer.apple.com/documentation/swiftui/view/replacedisabled(_:)) - Prevents replace operations in a text editor.

### Font
* [system(size:weight:design:)](https://developer.apple.com/documentation/swiftui/font/system(size:weight:design:)-697b2) - While the signature looks the same, the weight and design are now optional instead of required.

## Images
The Image initializer now has a new parameter called [variableValue](https://developer.apple.com/documentation/swiftui/image/init(_:variablevalue:bundle:)) that the rendered image can use to customize its appearance. If the symbols does not support it, this has no effect.
* [ImageRenderer](https://developer.apple.com/documentation/swiftui/imagerenderer) - An object that creates images from SwiftUI views. So you can compose a SwiftUI view and then generate an image or PDF from it.

# Animations
* [contentTransition](https://developer.apple.com/documentation/swiftui/view/contenttransition(_:)) - Modifies the view to use a given transition as its method of animating changes to the contents of its views.

# Charts
* More research needed here...
