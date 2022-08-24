# Style Guidelines
  - [Use lowerCamelCase](#use-lowercamelcase)
  - [Use singular tense](#use-singular-tense)
  - [Provide all translations](#provide-all-translations)

## Use lowerCamelCase
Use lower camel case for all names.

yes:
```
title
associatedResource{}
pointOfContact[]
```

no:
```
Title
AssociatedResource{}
pointofContact[]
```

## Use singular tense
Use singular tense for all names.

yes: `dataDictionary[]`

no: `dataDictionaries[]`

## Provide all translations

Provide "[__FGDC CSDGM__](https://www.fgdc.gov/metadata/csdgm-standard)", "__DCAT__" ([Data Catalog Vocabulary](https://www.w3.org/TR/vocab-dcat-2/)) and "[__sbJSON__]" (https://my.usgs.gov/confluence/display/sciencebase/ScienceBase ??) translations when an ISO translation is provided. If no translation is available indicate ```"no translation"```.

yes:
```
"translation": {
  "ISO 19115-1": ["CI_ResponsibleParty > partyIdentifier"],
  "FGDC CSDGM": ["no translation"]
  "DCAT": ["no translation"],
  "sbJSON": ["no translation"]
}
```

yes:
```
"translation": {
  "ISO 19115-2": ["MD_Keywords > thesaurusName > CI_Citation"],
  "FGDC CSDGM": [
    "idinfo>keywords>theme>themekt",
    "idinfo>keywords>place>placekt",
    "idinfo>keywords>temporal>tempkt"
  ],
  "DCAT": ["no translation"],
  "sbJSON": ["tags > scheme"]
}
```

no:
```
"translation": {
  "ISO 19115-1": ["CI_ResponsibleParty > partyIdentifier"]
}
```

no:
```
"translation": {
  "ISO 19115-1": ["CI_ResponsibleParty > partyIdentifier"],
  "FGDC CSDGM": ["no translation"]
}
```


