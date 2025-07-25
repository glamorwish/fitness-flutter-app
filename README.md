# Flexify

Get fit with Flexify. Easily track your gym progression with offline records and seamless graphs.

<p float="left">
    <a href="https://github.com/brandonp2412/Flexify/releases/latest"><img alt="GitHub Release" src="https://img.shields.io/github/v/release/brandonp2412/flexify?style=for-the-badge&logoColor=d3bcfd&labelColor=d3bcfd&color=151218"></a>
    <a href="#"><img alt="Release downloads" src="https://img.shields.io/github/downloads/brandonp2412/Flexify/total.svg?style=for-the-badge&logoColor=d3bcfd&labelColor=d3bcfd&color=151218"></a>
    <a href="#"><img alt="GitHub repo size" src="https://img.shields.io/github/repo-size/brandonp2412/flexify?style=for-the-badge&logoColor=d3bcfd&labelColor=d3bcfd&color=151218"></a>
</p>


<a href='https://play.google.com/store/apps/details?id=com.presley.flexify'><img alt='Get it on Google Play' height="75" src='https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png'/></a><a href="https://f-droid.org/packages/com.presley.flexify"><img src="https://fdroid.gitlab.io/artwork/badge/get-it-on.png" alt="Get it on F-Droid" height="75"></a>

<a href="https://apps.microsoft.com/detail/Flexify/9P13THVK7F69?mode=direct"><img src="https://get.microsoft.com/images/en-us%20dark.svg" height="75"/></a>
<a href="https://apps.apple.com/us/app/flexify/id6503730178?itsct=apps_box_badge&amp;itscg=30200"><img src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&amp;releaseDate=1717977600" alt="Download on the App Store" height="75"></a>

## Screenshots

<p float="left">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/1_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/2_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/3_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/4_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/5_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/6_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/7_en-US.png" height="600">
    <img src="fastlane/metadata/android/en-US/images/phoneScreenshots/8_en-US.png" height="600">
</p>

## Migration from [Massive](https://github.com/brandonp2412/Massive)

Gym sets and plans can be imported into Flexify.

<p float="left">
    <img src="docs/export-massive.png" height="600">
    <img src="docs/import-flexify.png" height="600">
</p>

## Donations

If you would like to support this project:
- Bitcoin `bc1qzlte8featxzf7xvtp3rjv7qqtwkgpup8hu85gp`
- Monero (XMR) `85tmLfWKbpd8nxQnUY878DDuFjmfcoCFXPWR7XYKLHBSbDZV8wxgoKYUtHtq1kHWJg4m14sdBXhYuUSbxEDA29d19XuREL5`
- [GitHub sponsor](https://github.com/sponsors/brandonp2412)

## Getting Started

To get started with Flexify, follow these steps:

1. **Clone the Repository**: Clone the Flexify repository to your local machine using Git:

   ```bash
   git clone --recursive https://github.com/brandonp2412/Flexify flexify
   ```

2. **Install Dependencies**: Navigate to the project directory and install the necessary dependencies:

   ```bash
   cd flexify
   flutter pub get
   ```

3. **Run the App**: Launch the Flexify app on your preferred device or emulator:

   ```bash
   flutter run
   ```
   
## Migrations

If you edit any of the models in the `lib/database` directory you probably need to create migrations. E.g. assume the version starts at `1`.

1. Bump the `schemaVersion`
`lib/database/database.dart`
```dart
  int get schemaVersion => 2;
```

2. Run database migrations
```sh
./scripts/migrate.sh
```

3. Add the migration step
`lib/database/database.dart`
```dart
from1To2: (Migrator m, Schema2 schema) async {
  await m.addColumn(schema.myTable, schema.myTable.myColumn);
},
```


## Contributing

Contributions to Flexify are welcomed and encouraged! Whether you want to report a bug, suggest a feature, or submit a pull request, please feel free to contribute. For major changes, please open an issue first to discuss the proposed changes.

## License

Flexify is licensed under the [MIT License](LICENSE.md).

