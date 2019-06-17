# Open Refine Template for University Catalogs

## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="filename">{{cells['filename'].value}}</identifier>
<titleInfo><title>{{cells["title"].value}}</title></titleInfo> 
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['creator'].value), '', '<name' + if(isBlank(cells['creator_URI'].value), '', ' authority="naf" valueURI="' + cells['creator_URI'].value +'"') + '><namePart>' + cells['creator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>')}}
<originInfo>
{{if(isBlank(cells['coverage'].value), '', '<dateOther>' + cells['coverage'].value + '</dateOther>')}}
{{if(isBlank(cells['dateIssued'].value), '','<dateIssued keyDate="yes" encoding="edtf">' + cells['dateIssued'].value + '</dateIssued>')}}
</originInfo>
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026614">online catalogs</form><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026685">records (documents)</form><digitalOrigin>reformatted digital</digitalOrigin><internetMediaType>application/pdf</internetMediaType></physicalDescription>
{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
<subject authority="lcsh" valueURI="http://id.loc.gov/authorities/subjects/sh85041065"><topic>Education, Higher</topic></subject>
<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>University Course Catalogs</title></titleInfo></relatedItem>
<recordInfo><languageOfCataloging><languageTerm authority="iso639-2b" type="text">English</languageTerm></languageOfCataloging><recordOrigin>Created and edited in general conformance to MODS Guidelines (Version 3.5).</recordOrigin><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>
```

#### Suffix

```
</modsCollection>
```