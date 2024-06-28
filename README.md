# THEODO Analysis

<p>
  <a href="https://www.bam.tech">
  <img  alt="logo" src="https://raw.githubusercontent.com/bamlab/theodo_analysis/main/doc/logo_bam.png" width="200"/>
  </a>
  </br>
  <p>Lint and dcm rules for Dart and Flutter used internally at <a href="https://www.bam.tech">Theodo Apps</a> ❤️💙💛.</p>
  <b>Note:</b> This package was heavily inspired by <a href="https://github.com/VeryGoodOpenSource/very_good_analysis">very_good_analysis</a>.
</p>

---

## 🧑‍💻 Usage

To use the lints, add as a dev dependency in your `pubspec.yaml`:

```yaml
dart pub add dev:theodo_analysis
# or
flutter pub add dev:theodo_analysis
```

Then, add an include in `analysis_options.yaml`:

```yaml
include: package:theodo_analysis/theodo_analysis.yaml
```
**Optional**: enable DCM.
This packages also include a subset of [dcm](https://dcm.dev) rules. Since dcm needs an API key to start. You can skip this part. Also, we consider it as a great tool, and we recommend it's usage.

First instal dcm:
```bash
$ brew tap CQLabs/dcm
$ brew install dcm
```
Then, [activate the license](https://dcm.dev/docs/getting-started/#activating-the-license):
```bash
dcm activate --license-key=YOUR_KEY
```

## ⚙️ Customize rules

To add or suppress a specific rules, you can edit the `analysis_options.yaml` file.

Suppression: 
```yaml
include: package:theodo_analysis/theodo_analysis.yaml
linter:
  rules:
    public_member_api_docs: false
dart_code_metrics:
  rules:
    - member-ordering: false
```
Addition:
```yaml
include: package:theodo_analysis/theodo_analysis.yaml
linter:
  rules:
    - no_leading_underscores_for_local_identifiers
dart_code_metrics:
  rules:
    - avoid-inferrable-type-arguments
```
> The list of all available dart rule can be found [here](https://dart.dev/tools/linter-rules/all).
> And the list of all available dcm rules can be found [here](https://dcm.dev/docs/rules/).

You can also disable it for specific files or folder. By default, theodo_analysis will not be applied to generated files.
```yaml
include: package:theodo_analysis/theodo_analysis.yaml
analyzer:
  exclude:
    - "**/*.g.dart"
    - "**/*.freezed.dart"
    - "**/*.graphql.dart"
dart_code_metrics:
  rules-exclude:
    - "**/*.g.dart"
    - "**/*.freezed.dart"
    - "**/*.graphql.dart"
```
## 👉 About Theodo Apps

We are a 130 people company developing and designing universal applications with [React Native](https://www.bam.tech/expertise/react-native) and [Flutter](https://www.bam.tech/expertise/flutter) using the Lean & Agile methodology. To get more information on the solutions that would suit your needs, feel free to get in touch by [email](mailto://contact@bam.tech) or through or [contact form](https://www.bam.tech/contact)!

We will always answer you with pleasure 😁