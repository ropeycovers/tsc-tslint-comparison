# tsc-tslint-comparison

Compares agressive rule settings for tsc compiler warnings
and tslint to identify gaps for developers
that use default tsc warning settings and hope that tslint will pick
up any other important issues.

## Install Developer Dependencies

```npm install```

## Run the Comparison

```npm run compare```

## Run Individually

```npm run tsc```

or

```npm run tslint```

## Rules

The configuration of each includes agressive rule settings.

This helps to find out what tsc *could* catch with agressive settings
that tslint will *not* catch with agressive settings.

There are two compromises in the agressive settings:

### tslint no-inferrable-types disabled

Reason: ['no-inferrable-types' and 'typedef' rules conflict #711](https://github.com/palantir/tslint/issues/711).

### tslint no-unused-variable enabled

Reason: It is deprecated (recommended to use
tsc compiler warning options instead) but we want to see it
for this comparison.

### Rule Settings

See (./tsconfig.json) and (./tslint.json)
