# Style Guidelines
## Use lowerCamelCase for all names

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
PointofContact[]
```

## Use singular case for all names

yes: `dataDictionary[]`

no: `dataDictionaries[]`

## Provide all translations

Provide "[FGDC CSDGM](https://www.fgdc.gov/metadata/csdgm-standard)" and "DCAT" ([Data Catalog Vocabulary](https://www.w3.org/TR/vocab-dcat-2/)) translations when an ISO translation is provided. If no translation is available indicate "no translation".

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

yes:
```
"translation": {
  "ISO 19115-1": ["CI_ResponsibleParty > partyIdentifier"],
  "FGDC CSDGM": ["no translation"]
  "DCAT": ["no translation"]
}
```
yes:
```
"translation": {
  "ISO 19115-2": ["MD_Keywords > thesaurusName > CI_Citation"],
  "FGDC CSDGM": ["idinfo>keywords>theme>themekt",
    "idinfo>keywords>place>placekt",
    "idinfo>keywords>temporal>tempkt"
  ],
  "DCAT": ["no translation"]
}
```         
