Configuration
=============

.. code-block:: yaml

    # Default configuration for "MewesKTwigSpreadsheetBundle"
    mewes_k_twig_spreadsheet:

        # Disabling formula calculations can improve the performance but the resulting documents
        # won't immediately show formula results in external programs.
        pre_calculate_formulas: true
        cache:

            # Using a bitmap cache is necessary, PhpSpreadsheet supports only local files.
            bitmap:               '"%kernel.cache_dir%/spreadsheet/bitmap"'

            # Using XML caching can improve memory consumption by writing data to disk.
            # Works only for .xlsx and .ods documents.
            xml:                  false # Example: "%kernel.cache_dir%/spreadsheet/xml"
