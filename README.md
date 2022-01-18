[![npm version](https://badge.fury.io/js/flatpickr-predefined.svg)](https://www.npmjs.com/package/flatpickr-predefined)
# flatpickr-predefined
Flatpickr plugin to show predefined options. Original script belongs to @patrick-vandy &amp; @austince

## Getting Started
Install the package with npm (or yarn) and require or import in into your project.
When you initialise a flatpickr include the plugin and set extra config fields to your liking.

## Example
``` js
flatpickr('.datepicker', {
    mode: 'range',
    plugins: myFlatpickrPlugins,
    ranges: {
        'Today': [new Date(), new Date()],
        "Yesterday": [moment().subtract(1, "days").toDate(), moment().subtract(1, "days").toDate()],
        'Last 30 Days': [moment().subtract(29, 'days').toDate(), new Date()],
        'This Month': [moment().startOf('month').toDate(), moment().endOf('month').toDate()],
        'Last Month': [
            moment().subtract(1, 'month').startOf('month').toDate(),
            moment().subtract(1, 'month').endOf('month').toDate()
        ],
        'Year to Date': [
            moment().startOf('year').toDate(),
            new Date()
        ],
        'Last Year': [
            moment().subtract(1, 'year').startOf('year').toDate(),
            moment().subtract(1, 'year').endOf('year').toDate()
        ]
    },
    rangesOnly: true, // only show the ranges menu unless the custom range button is selected
    rangesAllowCustom: true, // adds a Custom Range button to show the calendar if `rangesOnly` is true
    rangesCustomLabel: 'Custom Range' // customize the label for the custom range button
});
```
