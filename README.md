# \<etools-datepicker\>

Polymer datepicker element.
It also contains a button element (etools-datepicker-button) that creates and appends the datepicker to body tag to avoid dialog backdrop overlap entire content.

## Usage
```html
<etools-datepicker pretty-date="{{prettyDate}}"
    json-date="{{jsonDate}}"
    min-date="[[currentDate]]"
    max-date="[[currentDatePlus14days]]"
    format="LL"
    open="true",
    is-disabled="false"></etools-datepicker>

<etools-datepicker-button pretty-date="{{prettyD}}"
  format="DD/MM/YYYY"></etools-datepicker-button>

<etools-datepicker-button pretty-date="{{prettyD}}"
  format="DD/MM/YYYY" no-init></etools-datepicker-button>

<etools-datepicker-button pretty-date="{{prettyD}}"
format="DD/MM/YYYY" no-init show-clear-btn></etools-datepicker-button>
```

You can combine the element properties as you need.
Available properties:
* prettyDate: String, selected date with format applied
* jsonDate: String, JSON date format
* date: Date, selected date
* minDate: Date, min date
* maxDate: Date, max date
* isDisabled: Boolean, disabled state
* open: Boolean, if true then calendar will be open by default
* noInit: Boolean, default: false; if is set: `true` then the datepicker will not be initialized with a default date;
it works on both etools-datepicker and etools-datepicker-button elements
* showClearBtn: Boolean, default: false, if true the clear button will be visible and it can be used to empty the selected date.
* fireDateHasChanged: Boolean, default: false

### Events fired by etools-datepicker

* date-selected - when date is selected
* dismiss - when the datepicker modal is closed (click on cancel or clear buttons)
* date-has-changed - fired when date is changed only by the etools-datepicker-button
and only if `fireDateHasChanged` property is set to true


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


Datepicker button element style variables and mixins:

Custom property | Description | Default
----------------|-------------|----------
`--etools-datepicker-btn` | Mixin applyed to datepicker button | `{}`
`--etools-datepicker-btn-width` | Button width | `24px`
`--etools-datepicker-btn-height` | Button height | `24px`

## Install
```bash
$ bower install --save etools-datepicker
```

## Linting the code

Innstall local npm packages (run `npm install`)
Then just run the linting task

```bash
$ npm run lint
```
You should also use polylint. If you don't have Polylint installed run `npm install -g polylint`.
Then just run the linter on each file you wish to check like so

```bash
$ polylint -i filename.html
```
At the moment polylint crashes if it encounters a missing import. If that happens, temporarily comment out such imports and run the command again.

## Preview element locally
Install needed dependencies by running: `$ bower install`.
Make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `$ polymer serve` to serve your element application locally.

## Running Tests

```
$ polymer test
```
