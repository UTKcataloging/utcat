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
{{if(isBlank(cells['author'].value), '', '<name' + if(isBlank(cells['author_URI'].value), '', ' authority="naf" valueURI="' + cells['author_URI'].value +'"') + '><namePart>' + cells['author'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['author2'].value), '', '<name' + if(isBlank(cells['author2_URI'].value), '', ' authority="naf" valueURI="' + cells['author2_URI'].value +'"') + '><namePart>' + cells['author2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['author3'].value), '', '<name' + if(isBlank(cells['author3_URI'].value), '', ' authority="naf" valueURI="' + cells['author3_URI'].value +'"') + '><namePart>' + cells['author3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['date_text'].value), '', '<originInfo><dateCreated>' + cells['date_text'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_edtf'].value + '</dateCreated></originInfo>')}}
{{if(isBlank(cells['date_text_2'].value), '', '<originInfo><dateCreated>' + cells['date_text_2'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_2'].value + '</dateCreated></originInfo>')}}
{{if(isBlank(cells['date_text_3'].value), '', '<originInfo><dateCreated>' + cells['date_text_3'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_3'].value + '</dateCreated></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_aat_URI'].value}}">{{cells['form_aat'].value}}</form>
{{if(isBlank(cells['form_aat_2'].value), '', '<form authority="aat" valueURI="' + cells['form_aat_2_URI'].value + '">' + cells['form_aat_2'].value + '</form>')}}
{{if(isBlank(cells['extent'].value), '', '<extent>' + cells['extent'].value + '</extent>')}}
<digitalOrigin>reformatted digital</digitalOrigin></physicalDescription>
{{if(isBlank(cells['subject_lcsh'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_URI'].value + '"><topic>' + cells['subject_lcsh'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_2_URI'].value + '"><topic>' + cells['subject_lcsh_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_3_URI'].value + '"><topic>' + cells['subject_lcsh_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_4_URI'].value + '"><topic>' + cells['subject_lcsh_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_URI'].value + '"') + '><namePart>' + cells['subject_naf'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf_2'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_2_URI'].value + '"') + '><namePart>' + cells['subject_naf_2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf_3'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_3_URI'].value + '"') + '><namePart>' + cells['subject_naf_3'].value + '</namePart></name></subject>')}}
<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>University of Tennessee President's Papers, 1867-1954</title></titleInfo><identifier>{{cells['archival_identifier'].value}}</identifier></relatedItem>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation authority="naf" valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><languageOfCataloging><languageTerm authority="iso639-2b" type="text">English</languageTerm></languageOfCataloging><recordOrigin>Created and edited in general conformance to MODS Guidelines (Version 3.5).</recordOrigin><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>
```

#### Suffix

```
</modsCollection>
```