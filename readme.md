# Laravel-elixir-codeception standalone

**[Jeffrey Way's](https://github.com/JeffreyWay/laravel-elixir-codeception) laravel-elixir-codeception** module made compatible with laravel-elixir > 6.0.

It uses the legacy laravel-elixir code to momic original behavior.

## Installation

    npm install laravel-elixir-codeception-standalone

## Usage

This is a simple Codeception wrapper around Laravel Elixir. Add it to your Elixir-enhanced Gulpfile, like so:

```
var elixir = require('laravel-elixir');

require('laravel-elixir-codeception-standalone');

elixir(function(mix) {
   mix.codeception();
});
```

This will scan your `./tests/` directory, as well as any PHP classes in your 'app' folder for changes, and trigger your Codeception suite.

---

You may pass two arguments to the `codeception()` method.

### baseDir

Defaulting to './tests', this argument specifies the root directory to search for Codeception-specific tests.

### options

If you need to pass any Codeception-specific options, then you may pass an object as the second argument, like so:

```
mix.codeception(null, { flags: '--report' });
```

Or, maybe you only want to trigger your "functional" suite.

```
mix.codeception(null, { testSuite: 'functional' });
```

