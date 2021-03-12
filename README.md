# Overview #

This component monitors all drives, or specific drives, for files. The file filter is user-configurable. If found, it will alert.

The intent is to use to scan for files you don't expect or want to find on endpoints, such as AVHDX on HyperV in most instances, PSTs on fileservers, etc.

# Usage #

Set the Drive variable to "all" to scan ALL drives, including network drives.

To scan only specific drives use individual letters comma separated, such as "c,d". DO NOT use spaces, DO NOT include the colon and backslash.

Set the filter variable to a PowerShell compatible filter. Separate multiple filters by commas WITHOUT spaces, such as "*.hrl,*.avdh*"

# Output #
The standard output will output what drives were scanned for what files, and if any were found. If the component alerts the full paths
will be outputted to the diagnostic area. I.e., it should be sent your PSA in the ticket description field.