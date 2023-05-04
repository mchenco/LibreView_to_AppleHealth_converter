# Export blood glucose data from LibreView to Apple Health
Converts a CSV export of blood sugar levels from [LibreView](https://libreview.com) into a format that can be imported into the Apple Health app **with an iOS shortcut**

yay more quantified self data

## Forked updates
- import/export .csv locally in Downloads folder
- different timestamp format
- [Apple Health shortcut](https://www.icloud.com/shortcuts/6de3f2e4be294032810d5840ce710863) to import data (free) instead of Health CSV Importer
  - Watch out for units of measure, I had to export in mmol/L and input into Apple Health in mg/dL so I multiplied by `18.0182` in the shortcut but you can do the math

This is just a tweaked fork from [https://github.com/shrugalic](https://github.com/shrugalic/LibreView_to_AppleHealth_converter) and [u/Blue_Matter](https://www.reddit.com/r/shortcuts/comments/9jszwn/import_weight_data_into_health_app_from_csv/)! See original repo for more detailed instructions.

## TL;DR
1. Export LibreView data into `Downloads` folder
2. Download [conversion script](./convert_LV_export.py)
3. Run `python3 convert_LV_export.py` 
4. See outputted CSV in `Downloads` folder
5. Airdrop to Files app on iPhone
6. [Add shortcut](https://www.icloud.com/shortcuts/6de3f2e4be294032810d5840ce710863) and run