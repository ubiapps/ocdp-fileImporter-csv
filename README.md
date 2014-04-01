ocdp-fileImporter-csv
=====================

Adapter for importing CSV files into OCDP

Introduction
---

This module provides the ability to import CSV files into the UbiApps Open City Data Platform.

Files are imported from disk and stored in the given mongodb collection.

Installation
---

Clone this repository into a sub-folder of your OCDP Data Access and Service Toolkit installation, and re-start the platform. The CSV importer will automatically be loaded and available for use when importing documents.


Usage
---

The adapter will automatically be picked up and made available via the OCDP web UI. If you want to programmatically use the adapter see the example below.

```sh
var filePath = "/path/to/csv/file";
var coll = <mongodb collection>;
var importer = require("ocdp-fileImporter-csv");
importer.import(coll, filePath, function(err, dataSet) {
    if (err) {
        // Error occurred.

    } else {
        // Import succeeded.
        
    }
});

```

Related
---

For details of how to write an OCDP adapter, see the [ocdp adapter how-to].

[ocdp adapter how-to]:http://github.com/TobyEalden/ocdp-adapters
