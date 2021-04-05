<p align="center">
  <img src='https://cloud.githubusercontent.com/assets/126989/22546798/6cf18938-e936-11e6-933f-da756b9ee7b8.png' alt='Cavy logo' />
</p>

# Cavy

[![npm version](https://badge.fury.io/js/cavy.svg)](https://badge.fury.io/js/cavy) [![CircleCI](https://circleci.com/gh/pixielabs/cavy.svg?style=svg)](https://circleci.com/gh/pixielabs/cavy)

**Cavy** is a cross-platform, integration test framework for React Native, by
[Pixie Labs](http://pixielabs.io).

Cavy tests allow you to programmatically interact with deeply nested components
within your application. Write your tests in pure JavaScript and run them on
both Android and iOS.

Cavy tests look like this:
```js
export default function(spec) {
  spec.describe('A list of the employees', function() {
    spec.it('can be filtered by search input', async function() {
      await spec.exists('EmployeeList.JimCavy');
      await spec.fillIn('SearchBar.TextInput', 'Amy');
      await spec.press('Button.FilterSubmit');
      await spec.notExists('EmployeeList.JimCavy');
      await spec.exists('EmployeeList.AmyTaylor');
    });
  });
}
```

## 📋 Requirements
- React Native >= 0.59
- React >= 16.8.0

## 👶 Getting started
Get set up with Cavy by following our
[installation guide](https://cavy.app/docs/getting-started/installing).

You might also want to
[check out some articles and watch talks about Cavy](https://cavy.app/media) to
find out a bit more before you write code.

If you need some inspiration, head over to Cavy's
[sample app](/sample-app/CavyDirectory), follow the instructions in the README,
and see Cavy in action.

## 📘 Documentation
Full documentation and guides for Cavy can be found on our
[website](https://cavy.app).

## 🗺️ Development roadmap
Take a look at our public
[Pivotal Tracker](https://www.pivotaltracker.com/n/projects/2447582) to see what
we're currently working on, and what features we plan to add to Cavy next.

## 💯 Contributing
When making changes to Cavy, it's useful to have the
[CavyTester](https://github.com/pixielabs/cavy-tester) app running in
development for regression testing.

Follow the instructions it's own README on how to get the tester app running
against a local version of the Cavy library.

Here you'll also find instructions on adding new test cases to ensure
your functionality is fully tested. Please do this :)

Before contributing, please read the [code of conduct](CODE_OF_CONDUCT.md).

- Check out the latest master to make sure the feature hasn't been implemented
  or the bug hasn't been fixed yet.
- Check out the issue tracker to make sure someone already hasn't requested it
  and/or contributed it.
- Fork the project.
- Start a feature/bugfix branch.
- Commit and push until you are happy with your contribution.
- Remember to
  [submit a PR to DefinitelyTyped](https://github.com/DefinitelyTyped/DefinitelyTyped/tree/master/types/cavy)
  to update the type definitions if you've changed a function's inputs or outputs.
- Remember to submit a PR to update
  [the documentation](https://github.com/pixielabs/cavy-app) if you've changed
  how something works.
- Please try not to mess with the package.json, version, or history. If you
  want to have your own version, or is otherwise necessary, that is fine, but
  please isolate to its own commit so we can cherry-pick around it..
