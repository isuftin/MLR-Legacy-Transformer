# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Updated
- isuftin@usgs.gov - Updated the version constraint for pyca/cryptography due to
CVE https://nvd.nist.gov/vuln/detail/CVE-2018-10903

### Added
- Dockerfile Healthcheck

### Removed
- Dockerfile
- Dockerfile-DOI
- gunicorn_config.py

## [0.5.0] - 2017-11-20
### Added
- GET endpoint /version to show the current version and artifact name
- Authentication for /transformer/decimal_location and transformer/station_ix endpoints
- HTTPS Support

## [0.4.0] - 2017-11-01
### Change
- Trim whitespace from coordinateDatumCode before using it as a key to determine what projection to use.

## [0.3.0] - 2017-10-18
### Change
- Handle bad latitude/longitude values including out of range values by return null values for decimalLatitude and decimalLongitude.

## 0.2.0 - 2017-10-04
### Add
- POST endpoint /transformer/decimal_location takes a json object containing string latitude, longitude, and coordinateDatumCode and returns
decimalLatitude and decimalLongitude. Values will be null if invalid latitude, longitude, or coordinateDatumCode
- POST endpoint /transformer/station_ix takes a json object containing string station name and responds with stationIx.
- Swagger documention endpoint /api

[Unreleased]: https://github.com/USGS-CIDA/MLR-Legacy-Transformer/compare/MLR-Legacy-Transformer-0.5.0...master
[0.5.0]: https://github.com/USGS-CIDA/MLR-Legacy-Transformer/compare/MLR-Legacy-Transformer-0.4.0...MLR-Legacy-Transformer-0.5.0
[0.4.0]: https://github.com/USGS-CIDA/MLR-Legacy-Transformer/compare/MLR-Legacy-Transformer-0.3.0...MLR-Legacy-Transformer-0.4.0
[0.3.0]: https://github.com/USGS-CIDA/MLR-Legacy-Transformer/compare/MLR-Legacy-Transformer-0.2.0...MLR-Legacy-Transformer-0.3.0
