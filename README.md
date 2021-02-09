h1. #a11yEngineer - Web App Acceptance Criteria

h2. Header
- Full information: https://a11yengineer.com/thing/header/

h3. Success Criteria
- Description: Discoverable by screen reader as header or banner landmark
- Role: Identifies itself as a header or banner landmark
- Relationships: Typically contains site title and primary navigation
- State: n/a
- Focus: Can be targeted with a skip link, but isn't focusable
- Action: n/a



h2. Navigation Menu
- Full information: https://a11yengineer.com/thing/navigation/

h3. Navigation Container
- Description: Can have a heading if there are multiple navigation elements
- Role: Discoverable by screen reader as navigation landmark
- Relationships: If using a heading, aria-labelledby="headingId"
- State: n/a
- Focus: Can be targeted with a skip link, but isn't focusable
- Action: n/a

h3. Links go somewhere
- Description: Inner text describes purpose
- Role: Identifies itself as a link
- Relationships: href="url" makes a link focusable
- State: visited
- Focus: All links and dropdowns visibly focused with the tab key / swipe
- Action: enter

h3. Buttons do something
- Description: Inner text describes purpose
- Role: Identifies itself as a button
- Relationships: aria-controls="popup-id",  has-popup="true"
- State: aria-expanded="true/false"
- Focus: Visibly focused with the tab key / swipe
- Action: space, enter



h2. Headings
- Full information: https://a11yengineer.com/thing/headings/

h3. Headings (h1, h2, h3)
- Description: Inner text describes the heading
- Role: Should describe itself as a heading and its level
- Relationships: Headings should logically nest with a singular h1 and each major section staring with an h2 with h3 nested beneath.
- State: n/a
- Focus: Headings generally should not be focusable
- Action: n/a



h2. Button
- Full information: https://a11yengineer.com/thing/button/

h3. Success Criteria
- Description: Purpose is clear
- Role: Identifies itself as a button
- Relationships: Uses aria-haspopup for modal, listbox, or menus
- State: Express its state (pressed, expanded, disabled)
- Focus: Visibly focusable with tab key / swipe
- Action: Enter, spacebar / double tap

h3. Keyboard & Screenreader Support
- Tab / swipe, Focuses the button
- Enter / double tap, Activates the button
- Space / double tap, Activates the button


h2. Link
- Full information: https://a11yengineer.com/thing/link/

h3. Success Criteria
- Description: Purpose is clear
- Role: Identifies itself as a link
- Relationships: Has a valid href pointing to a uri
- State: n/a
- Focus: Is visibly focusable with tab / swipe
- Action: Enter key / double tap

h3. Keyboard & Screenreader Support
- Tab / swipe, Focuses the link
- Enter / double tap, Activates the link


h2. Modal Dialog
- Full information: https://a11yengineer.com/thing/modal/

h3. Success Criteria
- Description: Dialog is described by a title
- Role: Identifies as a dialog or modal
- Relationships: n/a
- State: n/a
- Focus: When open, focus is trapped inside dialog, focus returns to launch button on close
- Action: Escape key closes, enter/space activates close button

h3. Keyboard & Screenreader Support
- Escape, Closes the modal window
- Tab & shift-tab / swipe, Moves focus inside the modal window
h3. Keyboard & Screenreader Support
- Tab, Moves focus to next focusable element inside the dialog.  When focus is on the last focusable element in the dialog, moves focus to the first focusable element in the dialog.
- Shift + Tab, Moves focus to previous focusable element inside the dialog.  When focus is on the first focusable element in the dialog, moves focus to the last focusable element in the dialog.
- Escape, Closes the dialog.


h2. Tooltips
- Full information: https://a11yengineer.com/thing/tooltip/

h3. Don't use tooltips
- Description: Impossible to define
- Role: Poorly supported
- Relationships: None
- State: Unclear
- Focus: Unclear
- Action: Undefined



h2. Image: jpg, gif, png, svg
- Full information: https://a11yengineer.com/thing/image/

h3. JPG, GIF, or PNG
- Description: The alt="" attribute must describe the content of the image
- Role: Identifies itself as an image or graphic
- Relationships: n/a
- State: n/a
- Focus: n/a
- Action: n/a

h3. Linked SVG
- Description: The alt="" attribute must describe the content of the image
- Role: Identifies itself as an image or graphic - (Use role="image")
- Relationships: n/a
- State: n/a
- Focus: n/a
- Action: n/a

h3. Inline SVG
- Description: The title element of the SVG must describe the content of the image
- Role: Identifies itself as an image or graphic - (Use role="image")
- Relationships: n/a
- State: n/a
- Focus: n/a
- Action: n/a



h2. Icon
- Full information: https://a11yengineer.com/thing/icon/

h3. If the icon should be read by the screen reader:
- Description: Internal text can describe the icon, or aria=label="" can be used to provide a better description in the context
- Role: identifies as an image with role="image"
- Relationships: none
- State: none
- Focus: none
- Action: none

h3. If the icon should not be read by the screen reader
- Description: aria-hidden="true" should prevent the icon from being read
- Role: none
- Relationships: none
- State: none
- Focus: none
- Action: none



h2. Video or Audio Media
- Full information: https://a11yengineer.com/thing/video-or-audio/

h3. Video Player
- Description: Content is described by a heading or aria-label="media title"
- Role: none
- Relationships: none
- State: none
- Focus: All controls should be visibly focusable with the keyboard
- Action: Tab / swipe,  spacebar / double tap and arrow keys should operate controls

h3. Background video or animation
- Description: Content is described by aria-label="media title"
- Role: none
- Relationships: none
- State: none
- Focus: All controls should be visibly focusable with the keyboard
- Action: Pause, Play or hide controls operated by tab and spacebar



h2. Maps, charts, figures
- Full information: https://a11yengineer.com/thing/maps-charts-figures/

h3. Mapbox Map
- Description: Label the map with a heading or aria-label
- Role: Infoboxes should use role="status" to update the screen reader.
- Relationships: aria-labelledby="heading-id" can be used instead of aria-label
- State: none
- Focus: Map controls should be focusable with tab key
- Action: tab key / swipe should focus control buttons, enter / spacebar / double tap should activate

h3. Embedded map (like Google Maps)
- Description: Label the map in a heading, iFrame should include title attribute
- Role: none
- Relationships: aria-labelledby="heading-id" can be used
- State: none
- Focus: Map controls should be focusable with tab key
- Action: tab key should focus control buttons, enter or spacebar should activate

h3. Figures
- Description: Label the figure in a heading
- Role: Wrap chart/map in a <figure> element
- Relationships: Wrap the source in <cite>
- State: none
- Focus: none
- Action: none

h3. Simple image chart
- Description: Label the chart in a heading, img should have alt attribute
- Role: Wrap chart in a <figure> element with a <cite> of the source.
- Relationships: aria-labelledby="heading-id" can be used, longdesc can be used to point to a long description file
- State: none
- Focus: none
- Action: none



h2. Animations
- Full information: https://a11yengineer.com/thing/animations/

h3. If part of core functionality
- Description: The content should be described with inner text or aria-label
- Role: Identifies itself as an image or figure
- Relationships: none
- State: May need to be disabled by prefers-reduced-motion settings
- Focus: none
- Action: none



h2. Checkbox
- Full information: https://a11yengineer.com/thing/checkbox/

h3. Success Criteria
- Description: Label describes the input
- Role: Identifies  as a checkbox
- Relationships: for="input-id" is required in the label
- State: checked/unchecked/disabled
- Focus: Visibly focusable with tab / swipe
- Action: Check/uncheck with spacebar / double tap

h3. Keyboard & Screenreader Support
- Tab / swipe, Moves keyboard focus to the checkbox.
- Space / double tap, Toggles checkbox between checked and unchecked states.


h2. Radio Inputs
- Full information: https://a11yengineer.com/thing/radio-inputs/

h3. Success Criteria
- Description: Label describes its purpose
- Role: Identifies as a radio button
- Relationships: for="input-id" is required in the label
- State: checked/unchecked (selected/unselected), disabled
- Focus: Visibly focusable with tab key / swipe
- Action: Select with spacebar  / double tap and arrow keys

h3. Keyboard & Screenreader Support
- Tab  / swipe, Moves focus to the checked radio input in the group.  If a radio button is not checked, focus moves to the first radio button in the group.
- Space  / double tap, If the radio button with focus is not checked, changes the state to checked.  Otherwise, does nothing.  Note: The state where a radio is not checked only occurs on page load.
- Right arrow / swipe, Moves focus to and checks the next radio button in the group.  If focus is on the last radio button, moves focus to the first radio button.  The state of the previously checked radio button is changed to unchecked.
- Down arrow / swipe, Moves focus to and checks the next radio button in the group.  If focus is on the last radio button, moves focus to the first radio button.  The state of the previously checked radio button is changed to unchecked.
- Left arrow / swipe, Moves focus to and checks the previous radio button in the group.  If focus is on the first radio button, moves focus to and checks the last radio button.  The state of the previously checked radio button is changed to unchecked.
- Up arrow / swipe, Moves focus to and checks the previous radio button in the group.  If focus is on the first radio button, moves focus to and checks the last radio button.  The state of the previously checked radio button is changed to unchecked.


h2. Toggle Switch
- Full information: https://a11yengineer.com/thing/toggle-switch/

h3. Success Criteria
- Description: Label describes its purpose
- Role: Identifies  as a switch or checkbox
- Relationships: for="input-id" is required in the label
- State: on/off
- Focus: Visibly focusable with tab key
- Action: Check/uncheck with spacebar  / double tap

h3. Keyboard & Screenreader Support
- Tab / swipe, Moves keyboard focus to the checkbox.
- Space / double tap, Toggles checkbox between checked and unchecked states.


h2. Date Picker Input
- Full information: https://a11yengineer.com/thing/date-picker/

h3. Success Criteria
- Description: Label describes the input
- Role: Identify it as a date picker
- Relationships: for="input-id" is required in the label
- State: valid/invalid = selected/unselected
- Focus: Be visibly focusable with tab key / swipe
- Action: Enter and spacebar keys / double tap

h3. Keyboard & Screenreader Support
- Tab / swipe, Moves focus to the date picket input and between parts of the date / the date string
- Space / double tap, If the date picker is [type="text"] is will replace the text value with a space, if the input is [type="date"] is will open the calendar month widget.
- Right arrow, When focus is on the input with [type="date"] Moves focus between parts of the date (day/month/year). If the input is [type="text"] moves the cursor inside of the date string
- Down arrow, When focus is on the input with [type="date"] decrements the current value. If the input is [type="text"] moves the cursor to the end of the string.
- Left arrow, When focus is on the input with [type="date"] Moves focus between parts of the date (day/month/year). If the input is [type="text"] moves the cursor inside of the date string
- Up arrow, When focus is on the input with [type="date"] increments the current value. If the input is [type="text"] moves the cursor to the start of the string.


h2. Date Picker Dialog
- Full information: https://a11yengineer.com/thing/date-picker-dialog/

h3. Launch date picker button
- Description: Inner text describes button
- Role: Identify itself as a button
- Relationships: none
- State: none
- Focus: Visibly focusable with tab / swipe
- Action: Enter, space / double tap

h3. Date Picker Dialog
- Description: aria-labelledby="month-year-heading-id"
- Role: identify itself as a dialog or modal,  aria-modal="true"
- Relationships: none
- State: aria-live="polite" for dialog,  aria-live="polite" for month/year heading
- Focus: none
- Action: none

h3. Calendar Navigation Buttons
- Description: Inner text describes its purpose
- Role: Identifies itself as a button
- Relationships: none
- State: none
- Focus: Visibly focusable with tab
- Action: Enter / space / double tap

h3. Date Grid Table
- Description: aria-labelledby="month-year-heading-id"
- Role: May identifies itself as table or grid.
- Relationships: none
- State: none
- Focus: none
- Action: Arrow keys, Home, End, Page up, Page down

h3. Date Picker Buttons
- Description: Inner text describes its purpose
- Role: Identifies itself as a button
- Relationships: none
- State: aria-selected="true"
- Focus: Visibly focusable with tab
- Action: Enter / space / double tap



h2. Text Fields
- Full information: https://a11yengineer.com/thing/text-fields/

h3. Success Criteria
- Description: Label describes input
- Role: Identifies itself as a text input
- Relationships: for="input-id" is required in the label
- State: required, disabled
- Focus: Visibly focusable with tab key / swipe
- Action: Standard text editing keys

h3. Keyboard & Screenreader Support
- Standard single line text editing keys, Keys used for cursor movement and text manipulation, such as Delete and Shift + Right Arrow.  An HTML input with type="text" is used for the textbox so the browser will provide platform-specific editing keys.


h2. Progress Bar
- Full information: https://a11yengineer.com/thing/progress-bar/

h3. Success Criteria
- Description: Inner text describes the value
- Role: Identifies itself as a progress bar
- Relationships: none
- State: value and max properties,  indeterminate, determinate
- Focus: Typically not focusable
- Action: none



h2. Credit Card Input
- Full information: https://a11yengineer.com/thing/credit-card-input/

h3. Credit Card Number Input
- Description: Label describes input
- Role: type="text", use inputmode="numeric",    pattern="[0-9]*"
- Relationships: for="input-id" is required in the label
- State: required
- Focus: Visibly focusable with the tab key / swipe
- Action: Standard single line text editing keys

h3. Expiration Date (Month/Year)
- Description: Label describes input
- Role: type="text", inputmode="numeric",    pattern="[0-9]*"
- Relationships: for="input-id" is required in the label
- State: required
- Focus: Visibly focusable with the tab key
- Action: Standard single line text editing keys



h2. Telephone Input
- Full information: https://a11yengineer.com/thing/telephone/

h3. Telephone input
- Description: Label describes input
- Role: type="text", inputmode="numeric" to utilize mobile number pad
- Relationships: for="input-id" is required in the label
- State: none
- Focus: Visibly focusable with the tab key / swipe
- Action: Standard single line text editing keys



h2. Footer
- Full information: https://a11yengineer.com/thing/footer/

h3. Success Criteria
- Description: n/a
- Role: Identifies itself as footer or role="contentinfo"
- Relationships: Should be included in skip links
- State: none
- Focus: none
- Action: none

