# NEX GDDP Data Extension Specification

- **Title:** NEX GDDP
- **Identifier:** <https://stac-extensions.github.io/nexgddp/v1.0.0/schema.json>
- **Field Name Prefix:** nexgddp
- **Scope:** Item, Collection
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @dchandan

This document explains the provides an extension to describe the NEX GDDP data. Specifically, it describes the data stored on the [Marble network](https://marbleclimate.com).

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Fields

The fields in the table below can be used in these parts of STAC documents:

- [ ] Catalogs
- [x] Collections
- [x] Item Properties (incl. Summaries in Collections)
- [ ] Assets (for both Collections and Items, incl. Item Asset Definitions in Collections)
- [ ] Links

| Field Name           | Type                      | Description                                  |
| -------------------- | ------------------------- | -------------------------------------------- |
| nexgddp:license | string | **REQUIRED**. Data license |
| nexgddp:version      | string | **REQUIRED**. Data version |
| nexgddp:calendar      | string | **REQUIRED**. Calendar of the data |
| nexgddp:frequency      | string | **REQUIRED**. Temporal frequency of the data |
| nexgddp:source_id      | string | **REQUIRED**. Source ID of the CMIP6 model |
| nexgddp:Conventions      | string | **REQUIRED**. Data CF convention |
| nexgddp:institution      | string | **REQUIRED**. Name of the institution which produced the CMIP6 model |
| nexgddp:variable_id      | string | **REQUIRED**. Variable ID of the CMIP6 variable |
| nexgddp:cmip_version      | string | **REQUIRED**. Generation of the CMIP project |
| nexgddp:experiment_id      | string | **REQUIRED**. Experiment ID of the CMIP6 experiment |
| nexgddp:variant_label      | string | **REQUIRED**. String representation of the experiment variant |
| nexgddp:institution_id | string | **REQUIRED**. ID of the institution that created this model |

### Additional Field Information

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
