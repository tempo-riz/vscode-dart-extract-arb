Download the extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=zealousFoundry.flutter-extract-to-arb) or the [Open VSX Registry](https://open-vsx.org/extension/ZealousFoundry/flutter-extract-to-arb)

[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/zealousFoundry.flutter-extract-to-arb?label=Version)](https://marketplace.visualstudio.com/items?itemName=zealousFoundry.flutter-extract-to-arb)
[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/zealousFoundry.flutter-extract-to-arb?label=VS%20Marketplace%20Downloads)](https://marketplace.visualstudio.com/items?itemName=zealousFoundry.flutter-extract-to-arb)
[![Open VSX Downloads](https://img.shields.io/open-vsx/dt/zealousfoundry/flutter-extract-to-arb?label=Open%20VSX%20Downloads)](https://open-vsx.org/extension/ZealousFoundry/flutter-extract-to-arb)




<a href="https://ko-fi.com/M4M71BK1YJ">
<img src="https://github.com/tempo-riz/vscode-dart-extract-arb/blob/8561538ea208f424c5e3473a2fefee5ba9820bf8/assets/ko-fi.png?raw=true" height="40"/>
</a>

## Features

<img src="https://github.com/tempo-riz/vscode-dart-extract-arb/blob/89a7d4447b51616abc8526a9bea253b1b978506f/assets/demo.gif?raw=true" width="1200"/>

## This extension adds a single code action : 

### `Extract String to ARB`

Extract selected text, prompt for a key or infer from text, update ARB files with DeepL translations, generate dart code, and replace hardcoded strings with the generated key.

## Quick Setup

You should already have a l10n.yaml file in your project. If not, create one.
it uses flutter's official options for internationalization. see [here](https://docs.flutter.dev/ui/accessibility-and-internationalization/internationalization#configuring-the-l10n-yaml-file)

This extension extends existing options with the following options:

### Options with default values
```yaml
# l10n.yaml (extension specific options)

# Enable translation 
translate: true              

# Auto run flutter gen-l10n               
generate : true       

# Key prefix for translation             
key-prefix: AppLocalizations.of(context)!.  

# Generate key name 
# "ask" : prompt with pre-filled text | true : infer from text | false : prompt  
auto-name-key: true       

# Language to use for key name                  
key-name-language: en       

# Import line if needed                
import-line: ""                             
```

For the translation feature to work, you need to add your Deepl API key in vscode settings.json file:

`"flutter.deeplApiKey": "your-key",`   

You can get a free one [here](https://www.deepl.com/en/pro#developer)

And that's it! You're ready to go 🚀

## Links

Download the extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=zealousFoundry.flutter-extract-to-arb) or the [Open VSX Registry](https://open-vsx.org/extension/ZealousFoundry/flutter-extract-to-arb)


If you want to add a feature or file a bug, please open an issue/PR on the [GitHub repository](https://github.com/tempo-riz/vscode-dart-extract-arb)

## Pro tips
You can define an extension getter to access your translations more concisely:
```dart
extension ContextExt on BuildContext {
  AppLocalizations get t => AppLocalizations.of(this);
}

// then instead of this
Text(AppLocalizations.of(context).yourKey)

// use it like this:
Text(context.t.yourKey)
```
Don't forget to update the `key-prefix` & `import-line` options in l10n.yaml ;)

## Changelog
You can find it [here](https://github.com/tempo-riz/vscode-dart-extract-arb/blob/main/CHANGELOG.md)

I try to follow Semantic Versioning:
- Major: Breaking changes
- Minor: New features, but backward-compatible
- Patch: Bug fixes

## Support

If you'd like to support this project, consider contributing [here](https://github.com/sponsors/tempo-riz). Thank you! :)