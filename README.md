# \<etools-datepicker\>

Polymer datepicker element 

## Usage
```html
<etools-datepicker pretty-date="{{prettyDate}}"
    json-date="{{jsonDate}}"
    min-date="[[currentDate]]" 
    max-date="[[currentDatePlus14days]]"
    format="LL"
    open="true",
    is-disabled="false"></etools-datepicker>
```

You can combine the element attributes as you need.
Available attributes:
* prettyDate: String, selected date with format applied
* jsonDate: String, JSON date format
* minDate: Date, min date
* maxDate: Date, max date
* isDisabled: Boolean, disabled state
* open: Boolean, if true then calendar will be open by default

## Styling

The button that opens the calendar is just an iron-icon. You can use iron-icon style variables and mixins to style your
datepicker button.

You can use defined variables and mixins to change element style.

Custom property | Description | Default
----------------|-------------|----------
`--etools-datepicker-primary-color` | Date picker primary color | `#333333`
`--etools-datepicker-secondary-color` | Date picker primary color | `#737373`
`--etools-datepicker-heading-bg-color` | Heading background color | `#4a90e2`
`--etools-datepicker-heading-date-color` | Heading date color | `#ffffff`
`--etools-datepicker-heading-year-color` | Heading year color | `#c5cae9`
`--etools-datepicker-calendar-bg-color` | Calendar background color | `#ffffff`
`--etools-datepicker-disabled-color` | Disabled color | `#d1d1d1`
`--etools-datepicker-btns-text-color` | Calendar dialog buttons text color  | `#d1d1d1`
`--etools-datepicker-btn` | Calendar dialog buttons mixin  | `{}`


## Install
```bash
$ bower install --save etools-datepicker
```

## Preview element locally
Install needed dependencies by running: `$ bower install`.
Make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `$ polymer serve` to serve your element application locally.

## Running Tests

```
$ polymer test
```
