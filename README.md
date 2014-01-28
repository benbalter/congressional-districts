# US Congressional Districts

*Historic and current US Congressional districts as GeoJSON, versioned within Git*

## Usage

### Viewing a district's history

1. Select a state from the list above
2. Select a district
3. You will see the district boundaries for the 113th congress
4. Click history
5. Select a congress to compare changes in that district boundaries to the previous congress, if any

### As an API

Files in this repository follow a predictable file structure and can be treated as a RESTful API.

Each district's geoJSON for the current year can be retrieved via `ben.balter.com/congressional-districts/#{STATE}/#{DISTRICT}.geojson` where `STATE` is the two character state postal code, and `DISTRICT` is the two digit congressional district number with leading `0`s.

## Data

All data obtained from [US Census Datasets](http://www.census.gov/geo/maps-data/data/cbf/cbf_cds.html), although I don't guarantee their accuracy.

## Building

`script/build` will download all the relevant datasets (if not already downloaded), unzip, convert from ESRI Shapefile to the open GeoJSON format, break into files/folders by state/district, and commit, amending the git history to reflect the day the congress took session.

## License

MIT
