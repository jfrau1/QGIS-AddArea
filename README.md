# AddArea — QGIS Plugin

A QGIS plugin that calculates ellipsoidal area in hectares for all features in the active polygon layer and writes the result to a field named `Area_ha`.

## Features

- Calculates accurate **ellipsoidal area** (not planar) using the project's CRS and ellipsoid settings
- Writes results to an `Area_ha` field (created automatically if it doesn't exist)
- Handles **invalid geometries** automatically — attempts repair before skipping
- Works with layers already in edit mode — will not auto-commit in that case
- Reports a summary in the QGIS message bar (features processed, geometries repaired, features skipped)

## Requirements

- QGIS 3.0 or later

## Installation

### Manual install

1. Download or clone this repository
2. Copy the `addarea` folder into your QGIS plugins directory:
   - **Windows:** `C:\Users\<you>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins`
   - **Mac:** `~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins`
   - **Linux:** `~/.local/share/QGIS/QGIS3/profiles/default/python/plugins`
3. Restart QGIS
4. Go to **Plugins → Manage and Install Plugins**, find **AddArea**, and enable it

## Usage

1. Load a polygon layer in QGIS and make it the active layer
2. Click the **AddArea** button in the toolbar, or go to **Vector → AddArea → AddArea**
3. The plugin will add or update the `Area_ha` field with ellipsoidal area in hectares
4. A summary message will appear in the message bar

## License

This plugin is free software licensed under the [GNU General Public License v2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html).

## Author

Jackson Frauenfelder — [j.frauenfelder@me.com](mailto:j.frauenfelder@me.com)

## Issues

Please report bugs or feature requests on the [GitHub Issues](https://github.com/jfrau1/QGIS-AddArea/issues) page.
