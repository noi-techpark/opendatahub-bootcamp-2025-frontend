# Welcome to the Open Data Hub Bootcamp 2025!
This repo will guide you through the challenge 1, in which you will implement a frontend which visualizes Webcams.

The goal of this bootcamp is to foster our community around the Open Data Hub, to get to know each other, the technology, but also for you to just learn stuff and make friends. This is not a competition, so don't be afraid to make mistakes and try out new stuff. Our Open Data Hub team is there to help and support you.

You will also have an opportunity to present the results to the public at our upcoming event, the Open Data Hub Day

# The challenge
Your challenge will be to implement a visualization of Webcam data from the Open Data Hub Content Api.

# Tech stack
You are free to use whatever programming language best fits your group. The frontend should be usable on a web page.

# Dataset
For this challenge you will use the WebcamInfo dataset, which is part of the Open Data Hub's tourism domain.  
You can explore it using the
- [API](https://tourism.api.opendatahub.com/v1/WebcamInfo)
- [Swagger](https://tourism.api.opendatahub.com/swagger/index.html#/WebcamInfo)
- [databrowser](https://databrowser.opendatahub.com/dataset-overview/ac3db7eb-f125-4c24-add5-2e4392961e16) 

The data is available as Open Data. So no Token / Authentication is needed to retrieve the data.
The available webcams are from different sources.
The data quality differs, Open Data Hub tries to map all available fields of the providers in the Opendatahub Webcam Datamodel.
Some providers offers static images, 360° views with their custom webcam video players etc... 
The goal is to show the static images where available.

a list of the various data providers is available with this request
[Webcam Providers](https://tourism.api.opendatahub.com/v1/Distinct?type=webcam&fields=Source&getasarray=true)


This is a real world example of a Webcam of the provider Feratel:
https://tourism.api.opendatahub.com/v1/WebcamInfo/FERATEL_84109A42-B103-47EA-A2CC-23CE9AD37D7F_6202
```json
{
"Id": "FERATEL_84109A42-B103-47EA-A2CC-23CE9AD37D7F_6202",
"Self": "https://tourism.api.opendatahub.com/v1/WebcamInfo/FERATEL_84109A42-B103-47EA-A2CC-23CE9AD37D7F_6202",
"Areas": [],
"_Meta": {
"Id": "FERATEL_84109A42-B103-47EA-A2CC-23CE9AD37D7F_6202",
"Type": "webcam",
"Source": "feratel",
"Reduced": false,
"LastUpdate": "2025-04-07T00:10:33.7820108+00:00",
"UpdateInfo": {
"UpdatedBy": "feratel.webcam.import",
"UpdateSource": "http://tourism.importer.opendatahub.com/FERATEL/Wecam",
"UpdateHistory": [
{
"UpdatedBy": "feratel.webcam.import",
"LastUpdate": "2025-04-07T00:10:33.7820108+00:00",
"UpdateSource": "http://tourism.importer.opendatahub.com/FERATEL/Wecam"
}
]
}
},
"Active": true,
"Detail": {
"de": {
"Title": "3 Zinnen Racing Arena",
"Header": null,
"BaseText": null,
"Keywords": [
"Toblach (3Zinnen Dolomites)",
"Südtirol",
"Italien",
"trentino",
"pustertal",
"drei zinnen",
"3 zinnen",
"bozen",
"dolomiten",
"dolomiti superski",
"südtirol",
"alto adige",
"suedtirol"
],
"Language": "de",
"MetaDesc": null,
"AuthorTip": null,
"IntroText": null,
"MetaTitle": null,
"SubHeader": null,
"SafetyInfo": null,
"ParkingInfo": null,
"GetThereText": null,
"EquipmentInfo": null,
"AdditionalText": null,
"PublicTransportationInfo": null
}
},
"Source": "feratel",
"AreaIds": null,
"GpsInfo": [
{
"Gpstype": "position",
"Altitude": 1245,
"Latitude": 46.727645,
"Longitude": 12.202379,
"AltitudeUnitofMeasure": "m"
}
],
"Mapping": {
"feratel": {
"panid": "6202",
"link_id": "84109A42-B103-47EA-A2CC-23CE9AD37D7F"
}
},
"ODHTags": [],
"SmgTags": null,
"WebcamId": "6202",
"GpsPoints": {
"position": {
"Gpstype": "position",
"Altitude": 1245,
"Latitude": 46.727645,
"Longitude": 12.202379,
"AltitudeUnitofMeasure": "m"
}
},
"OdhActive": true,
"Shortname": "3 Zinnen Racing Arena",
"SmgActive": true,
"Streamurl": null,
"Webcamurl": "http://webtv.feratel.com/webtv/?design=v5&pg=CDB9645D-E67B-44D2-9FC9-E1539FF9A6B7&cam=6202",
"LastChange": "2025-04-05T00:10:33.7503195+00:00",
"Previewurl": null,
"VideoItems": null,
"Webcamname": {
"de": "3 Zinnen Racing Arena"
},
"FirstImport": "2023-11-28T16:42:24.9076512+00:00",
"HasLanguage": null,
"LicenseInfo": {
"Author": "",
"License": "",
"ClosedData": false,
"LicenseHolder": "https://www.feratel.com/"
},
"PublishedOn": [],
"ContactInfos": {},
"ImageGallery": [
{
"Width": null,
"Height": null,
"License": null,
"ValidTo": null,
"ImageUrl": "http://wtvthmb.feratel.com/thumbnails/6202.jpeg?t=38&dcsdesign=WTP_opendatahubsuedtirol&design=v5",
"CopyRight": null,
"ImageDesc": {},
"ImageName": "MediaPlayer Thumbnails 38",
"ImageTags": null,
"ValidFrom": null,
"ImageTitle": {},
"ImageSource": "feratel",
"IsInGallery": true,
"ImageAltText": {},
"ListPosition": 0,
"LicenseHolder": null
},
{
"Width": null,
"Height": null,
"License": null,
"ValidTo": null,
"ImageUrl": "http://wtvthmb.feratel.com/thumbnails/6202.jpeg?dcsdesign=WTP_opendatahubsuedtirol&design=v5",
"CopyRight": null,
"ImageDesc": {},
"ImageName": "MediaPlayer Thumbnails",
"ImageTags": null,
"ValidFrom": null,
"ImageTitle": {},
"ImageSource": "feratel",
"IsInGallery": true,
"ImageAltText": {},
"ListPosition": null,
"LicenseHolder": null
},
{
"Width": null,
"Height": null,
"License": null,
"ValidTo": null,
"ImageUrl": "http://wtvthmb.feratel.com/thumbnails/6202.jpeg?t=36&dcsdesign=WTP_opendatahubsuedtirol&design=v5",
"CopyRight": null,
"ImageDesc": {},
"ImageName": "MediaPlayer Thumbnails 36",
"ImageTags": null,
"ValidFrom": null,
"ImageTitle": {},
"ImageSource": "feratel",
"IsInGallery": true,
"ImageAltText": {},
"ListPosition": null,
"LicenseHolder": null
}
],
"ListPosition": null,
"WebCamProperties": {
"HasVR": null,
"TourCam": null,
"HtmlEmbed": null,
"StreamUrl": null,
"WebcamUrl": "http://webtv.feratel.com/webtv/?design=v5&pg=CDB9645D-E67B-44D2-9FC9-E1539FF9A6B7&cam=6202",
"PreviewUrl": null,
"ViewerType": null,
"ZeroDirection": null,
"ViewAngleDegree": null
},
"WebcamAssignedOn": null
}
```

There are a lot of fields available. Inspect the data of various providers and identify the right fields to display a webcam.  
Reduce the json size by using field selectors, removing null data, remove data that is not usable etc....


### More information
You can find more information on the API format here:  
[Swagger Ninja API](https://tourism.api.opendatahub.com)  
[Content Api Wiki](hhttps://github.com/noi-techpark/opendatahub-docs/wiki/Content-API)  
[Open Data Hub documentation](https://opendatahub.readthedocs.io/)  
