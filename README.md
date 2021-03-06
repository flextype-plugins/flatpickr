<h1 align="center">Flatpickr Plugin for <a href="https://flextype.org/">Flextype</a></h1>

<p align="center">
<a href="https://github.com/flextype-plugins/flatpickr/releases"><img alt="Version" src="https://img.shields.io/github/release/flextype-plugins/flatpickr.svg?label=version&color=black"></a> <a href="https://github.com/flextype-plugins/flatpickr"><img src="https://img.shields.io/badge/license-MIT-blue.svg?color=black" alt="License"></a> <a href="https://github.com/flextype-plugins/flatpickr"><img src="https://img.shields.io/github/downloads/flextype-plugins/flatpickr/total.svg?color=black" alt="Total downloads"></a> <a href="https://github.com/flextype/flextype"><img src="https://img.shields.io/badge/Flextype-0.9.16-green.svg?color=black" alt="Flextype"></a> <a href=""><img src="https://img.shields.io/discord/423097982498635778.svg?logo=discord&color=black&label=Discord%20Chat" alt="Discord"></a>
</p>

Lightweight and powerful datetime picker plugin for Flextype.

## Dependencies

The following dependencies need to be downloaded and installed for Flatpickr Plugin.

| Item | Version | Download |
|---|---|---|
| [flextype](https://github.com/flextype/flextype) | 0.9.16 | [download](https://github.com/flextype/flextype/releases) |
| [twig](https://github.com/flextype-plugins/twig) | >=2.0.0 | [download](https://github.com/flextype-plugins/twig/releases) |
| [blueprints](https://github.com/flextype-plugins/blueprints) | >=1.0.0 | [download](https://github.com/flextype-plugins/blueprints/releases) |

## Installation

1. Download & Install all required dependencies.
2. Create new folder `/project/plugins/flatpickr`
3. Download Flatpickr Plugin and unzip plugin content to the folder `/project/plugins/flatpickr`

## Documentation

### Settings

```yaml
# enabled: true or false to disable the plugin
enabled: true

# Plugin priority
priority: 41

# Place to load
assetsLoadOnAdmin: true
assetsLoadOnSite: false

# Blocks
blocks:
  InputFlatpickr:
    properties:
      id: flatpickr
      name: flatpickr
      
      # Flatpicker options
      options:

        # Allows the user to enter a date directly input the input field. By default, direct entry is disabled.
        allowInput: false

        # Allow preloading of invalid date
        allowInvalidPreload: false

        # Exactly the same as date format, but for the altInput field
        altFormat: "F j, Y"

        # Show the user a readable date (as per altFormat), but return something totally different to the server.
        altInput: false

        # This class will be added to the input element created by the altInput option.  
        # Note that altInput already inherits classes from the original input.
        altInputClass: ""

        # Whether to enable animations, such as month transitions
        animate: true

        # Defines how the date will be formatted in the aria-label for calendar days, using the same tokens as dateFormat. 
        # If you change this, you should choose a value that will make sense if a screen reader reads it out loud.
        ariaDateFormat: "F j, Y"

        # Whether the default time should be auto-filled when the input is empty and gains or loses focus. 
        autoFillDefaultTime: true

        # Whether clicking on the input should open the picker.
        # Set it to false if you only want to open the calendar programmatically
        clickOpens: true

        # Whether calendar should close after date selection
        closeOnSelect: true
        
        # If "mode" is "multiple", this string will be used to join
        # selected dates together for the date input value.
        conjunction: null
  
        # A string of characters which are used to define how the date will be displayed in the input box.
        # See https://chmln.github.io/flatpickr/formatting
        dateFormat: "d-m-Y H:i"

        # The initial selected date(s).
        defaultDate: null

        # Initial value of the hour element, when no date is selected 
        defaultHour: 12

        # Initial value of the minute element, when no date is selected 
        defaultMinute: 0

        # Initial value of the seconds element, when no date is selected 
        defaultSeconds: 0

        # Set this to true to always use the non-native picker on mobile devices.
        # By default, Flatpickr utilizes native datetime widgets unless certain options (e.g. disable) are used.
        disableMobile: false

        # Disables all dates except these specified. 
        # See https://chmln.github.io/flatpickr/examples/#disabling-all-dates-except-select-few 
        #enable: []
                
        # Disables certain dates, preventing them from being selected.
        # See https://chmln.github.io/flatpickr/examples/#disabling-specific-dates
        #disable: []

        # Enables seconds selection in the time picker.
        enableSeconds: false

        # Enables the time picker
        enableTime: true

        # Adjusts the step for the hour input (incl. scrolling)
        hourIncrement: 1

        # By default, clicking anywhere outside of calendar/input will close the calendar.
        # Clicking on elements specified in this option will not close the calendar
        ignoredFocusElements: []

        # Displays the calendar inline
        inline: false

        # The locale, either as a string (e.g. "ru", "en") or as an object.
        # See https://chmln.github.io/flatpickr/localization/ 
        locale: "default"

        # Adjusts the step for the minute input (incl. scrolling)
        minuteIncrement: 5

        # Date selection mode, defaults to "single"
        # variants: single, multiple, or range
        mode: "single"

        # How the month selector in the calendar should be shown
        # variants: dropdown, static
        monthSelectorType: "static"

        # HTML for the right arrow icon, used to switch months.
        nextArrow: "<svg version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' viewBox='0 0 17 17'><g></g><path d='M13.207 8.472l-7.854 7.854-0.707-0.707 7.146-7.146-7.146-7.148 0.707-0.707 7.854 7.854z' /></svg>"

        # Hides the day selection in calendar.
        # Use it along with "enableTime" to create a time picker.
        noCalendar: false

        # A custom datestring parser
        parseDate: false

        # Plugins. 
        # See https://chmln.github.io/flatpickr/plugins/ 
        # plugins: []

        # How the calendar should be positioned with regards to the input.
        # variants: auto, above, below, auto left, auto center, above right, below left, below center, below right
        position: "auto"
          
        # The element off of which the calendar will be positioned.
        # Defaults to the date input
        positionElement: null

        # HTML for the left arrow icon, used to switch months.
        prevArrow: "<svg version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' viewBox='0 0 17 17'><g></g><path d='M5.207 8.471l7.146 7.147-0.707 0.707-7.853-7.854 7.854-7.853 0.707 0.707-7.147 7.146z' /></svg>"

        # Whether to display the current month name in shorthand mode, e.g. "Sep" instead "September"
        shorthandCurrentMonth: false

        # Creates a wrapper to position the calendar. Use this if the input is inside a scrollable element
        static: false

        # Sets the number of months to show 
        showMonths: 1

        # Displays time picker in 24 hour mode without AM/PM selection when enabled.
        time_24hr: false

        # Display week numbers left of the calendar.
        weekNumbers: false

        # See https://chmln.github.io/flatpickr/examples/#flatpickr-external-elements
        wrap: false
         
    template: plugins/flatpickr/blocks/InputFlatpickr/block.html
```

## LICENSE
[The MIT License (MIT)](https://github.com/flextype-plugins/flatpickr/blob/master/LICENSE.txt)
Copyright (c) 2021 [Sergey Romanenko](https://github.com/Awilum)
