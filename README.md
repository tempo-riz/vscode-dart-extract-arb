## Features

<img src="https://github.com/tempo-riz/vscode-dart-extract-arb/blob/89a7d4447b51616abc8526a9bea253b1b978506f/assets/demo.gif?raw=true" width="1200"/>

## This extension adds a single code action : 

### `Extract String to ARB`

Extract selected text, prompt for a key, add it to the ARB file, and translate it with DeepL for other ARB files.


## Quick Setup

You should already have a l10n.yaml file in your project. If not, create one.
it uses flutter's official options for internationalization. see [here](https://docs.flutter.dev/ui/accessibility-and-internationalization/internationalization#configuring-the-l10n-yaml-file)

This plugins extends existing options with the following options:

### Options with default values
```yaml
# l10n.yaml (plugin specific options)
translate: true                             # Enable translation 
key-prefix: AppLocalizations.of(context).   # Key prefix for translation
import-line: ""                             # Import line if needed
auto-name-key: false                        # Generate key name based on text
generate : true                             # auto run flutter gen-l10n
```

For the translation feature to work, you need to add your Deepl API key in vscode settings.json file:

`"flutter.deeplApiKey": "your-key",`   

You can get a free one [here](https://www.deepl.com/en/pro#developer)

And that's it! You're ready to go 🚀

## Links

Download the extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=zealousFoundry.flutter-extract-to-arb) or the [Open VSX Registry](https://open-vsx.org/extension/ZealousFoundry/flutter-extract-to-arb)


If you want to add a feature or file a bug, please open an issue/PR on the [GitHub repository](https://github.com/tempo-riz/vscode-dart-extract-arb)
