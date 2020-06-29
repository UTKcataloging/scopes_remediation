**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>

<identifier type="pid">{{cells["PID"].value}}</identifier>
<identifier type="local">{{cells["identifier"].value}}</identifier>

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells['name.0'].value), '', '<name'+ if(isBlank(cells['name.0_URI'].value), '', ' authority="naf" valueURI="' + cells['name.0_URI'].value + '"') + '><namePart>' + cells['name.0'].value + '</namePart>' + if(isBlank(cells['name.0_role'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name.0_role_URI'].value + '">' + cells['name.0_role'].value + '</roleTerm></role>') + '</name>')}}

{{if(isBlank(cells['name.1'].value), '', '<name'+ if(isBlank(cells['name.1_URI'].value), '', ' authority="naf" valueURI="' + cells['name.1_URI'].value + '"') + '><namePart>' + cells['name.1'].value + '</namePart>' + if(isBlank(cells['name.1_role'].value), '', '<role><roleTerm authority="marcrelator" valueURI="' + cells['name.1_role_URI'].value + '">' + cells['name.1_role'].value + '</roleTerm></role>') + '</name>')}}

<originInfo> {{if(isBlank(cells["date"].value),'','<dateCreated>' + cells['date'].value + '</dateCreated>')}}{{if(isBlank(cells["date_edtf"].value),'','<dateCreated encoding="edtf">' + cells['date_edtf'].value + '</dateCreated>')}}</originInfo>

<language><languageTerm authority="iso639-2b" type="text">English</languageTerm></language>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells['extent'].value}}</extent></physicalDescription>

{{if(isBlank(cells['subject.0geographic'].value), '', '<subject' + if(isBlank(cells['subject.0geographic_URI'].value), '>', ' authority="naf" valueURI="' + cells['subject.0geographic_URI'].value + '">') + '<geographic>' + cells['subject.0geographic'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject.0topic'].value), '', '<subject' + if(isBlank(cells['subject.0topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.0topic_URI'].value + '">') + '<topic>' + cells['subject.0topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.1topic'].value), '', '<subject' + if(isBlank(cells['subject.1topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject.1topic_URI'].value + '">') + '<topic>' + cells['subject.1topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject.0name'].value), '', '<subject'+ if(isBlank(cells['subject.0name_URI'].value), '', ' valueURI="' + cells['subject.0name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.0name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.1name'].value), '', '<subject'+ if(isBlank(cells['subject.1name_URI'].value), '', ' valueURI="' + cells['subject.1name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.1name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.2name'].value), '', '<subject'+ if(isBlank(cells['subject.2name_URI'].value), '', ' valueURI="' + cells['subject.2name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.2name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject.3name'].value), '', '<subject'+ if(isBlank(cells['subject.3name_URI'].value), '', ' valueURI="' + cells['subject.3name_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject.3name'].value + '</namePart></name></subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<relatedItem displayLabel="{{cells['relatedItem_label'].value}}" type="host"><titleInfo><title>{{cells['relatedItem'].value}}</title></titleInfo><identifier>{{cells['relatedItem_identifier'].value}}</identifier></relatedItem>

<location><physicalLocation valueURI="{{cells['physicalLocation_URI'].value}}">{{cells['physicalLocation'].value}}</physicalLocation><shelfLocator>{{cells['physicalLocation.1'].value}}</shelfLocator></location>

<recordInfo><recordContentSource valueURI="{{cells['source_URI'].value}}">{{cells['source'].value}}</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['accessCondition_URI'].value}}">{{cells['accessCondition'].value}}</accessCondition>

</mods>
```



**Suffix:**

```
</modsCollection>
```