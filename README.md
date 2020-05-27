# Auto Translate JSON

Adds a menu item to JSON files to allow them to be automatically translates into other languages using Google Translate.

## How it works

![demo](images/demo.gif)

When localizing an application, if you have a folder called something like `translations`, `languages`, or `i18n` that contains JSON files for each language, you can use this extension to right click on your primary language file and automatically create additional translations. It uses the Google Translate API to perform the translations, and you must have your own API key to make the calls.

Just create empty files with the locale names as filenames and this extension will generate their translations. For example, if you want French, create a file `fr.json`.

## Features

- Option to keep existing translations, to cut down on data processing when adding new terms
- Option to keep extra translations, if one language has additional items

## Requirements

Since translation services are not free, you must provide your own Google API key. Luckily they give a decent amount of translations for free. Go here to set up your account and request a key:

<https://console.developers.google.com/apis/library/translate.googleapis.com>

## Extension Settings

This extension contributes the following settings:

- `auto-translate-json.sourceLocale`: A failsafe to prevent processing the wrong file. Defaults to "en" for english. You can change this to any valid two letter locale code you wish to use.
- `auto-translate-json.googleApiKey`: Enter your Google API key in this setting.

## Limitations

- all files need to be in the same folder. This does not support structures where each language is in it's own subfolder.
- this does not (yet) support nested terms.

## Release Notes

### 1.0.0

Initial release of auto-translate-json