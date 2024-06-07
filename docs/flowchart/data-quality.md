Spark Error Flowchart: Note this uses mermaid.js which may take awhile to load.

```mermaid
flowchart LR
DataNotExpected("Data is not as expected")
 
DataNotExpected("Data is not as expected") --> DataQualityIssue("Data Quality Issue")
DataQualityIssue("Data Quality Issue") --> NullValues("I have null values in columns that should not have null values")

{%
  include-markdown "./shared.md"
  end="OHNOES[Contact support]"
  comments=false
%}
```