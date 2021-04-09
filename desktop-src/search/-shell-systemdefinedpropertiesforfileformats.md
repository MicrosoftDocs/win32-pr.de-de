---
description: Microsoft Windows bietet eine Reihe von Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined Eigenschaften für benutzerdefinierte Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128517"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>System-Defined Eigenschaften für benutzerdefinierte Dateiformate

Microsoft Windows bietet eine Reihe von Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können. Wenn Sie ein benutzerdefiniertes Dateiformat erstellen, sollten Sie beliebig viele System definierte Eigenschaften unterstützen. Vor dem Erstellen eines benutzerdefinierten Eigenschaften Handler sollten Sie die vom System bereitgestellten Handler überprüfen, um festzustellen, ob Sie einen verwenden können, anstatt einen eigenen zu schreiben.

In der folgenden Tabelle werden die Dateiformate kategorisiert und anschließend die wichtigsten Systemeigenschaften aufgelistet, die ihr Dateiformat unterstützen sollte. Um eine gute Benutzer Leistung zu gewährleisten, sollten Sie alle Eigenschaften der Priorität 1 und 2 für die Kategorie des Datei Formats unterstützen.

-   [Kommunikation](#communications)
-   [Kontakte](#contacts)
-   [Dokumente](#documents)
-   [Allgemein](#generic)
-   [Musizieren](#music)
-   [Bilder](#pictures)
-   [Videos](#videos)
-   [Zugehörige Themen](#related-topics)

## <a name="communications"></a>Kommunikation



| Name            | Eigenschaft                               | Priorität |
|-----------------|----------------------------------------|----------|
| Empfangenes Datum   | System. Message. DateReceived            | 1        |
| Aus Namen      | System. Message. FromName                | 1        |
| Hat Anlagen | System. Message. hasattachments          | 1        |
| Mailbox         | System. Communication. storeddisplayname | 1        |
| Name            | System. filename                        | 1        |
| Subject         | System. Subject                         | 1        |
| In Namen        | System. Message. ToName                  | 1        |
| Category        | System. Category                        | 2        |
| type            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Kontakte



| Name             | Eigenschaft                           | Priorität |
|------------------|------------------------------------|----------|
| Kontoname     | System. Communication. Accountname   | 1        |
| Telefon (geschäftlich)   | System. Contact. businesstelephone   | 1        |
| Company          | System. Company                     | 1        |
| E-Mail-Adresse    | System. Contact. primaryemailaddress | 1        |
| Wichtigkeit       | System. importancetext              | 1        |
| Mobiltelefon     | System. Contact. Mobiletelefon     | 1        |
| Geschäftliche Adresse | System. Contact. BusinessAddress     | 2        |
| Geschäftfax     | System. Contact. businessfaxnummer   | 2        |
| Category         | System. Category                    | 2        |
| Privatadresse     | System. Contact. HomeAddress         | 2        |
| Telefon (privat)       | System. Contact. homeTelephone       | 2        |
| Titel            | System.Title                       | 2        |



 

## <a name="documents"></a>Dokumente



| Name      | Eigenschaft             | Priorität |
|-----------|----------------------|----------|
| Authors   | System.Author        | 1        |
| Volltext | System. Fulltext      | 1        |
| `Tags`      | System.Keywords      | 1        |
| type      | System.PerceivedType | 1        |
| Category  | System. Category      | 2        |
| Titel     | System.Title         | 2        |



 

## <a name="generic"></a>Allgemein



| Name     | Eigenschaft             | Priorität |
|----------|----------------------|----------|
| Authors  | System.Author        | 1        |
| Titel    | System.Title         | 1        |
| type     | System.PerceivedType | 1        |
| Category | System. Category      | 2        |
| `Tags`     | System.Keywords      | 2        |



 

## <a name="music"></a>Musik



| Name         | Eigenschaft                     | Priorität |
|--------------|------------------------------|----------|
| \#           | System. Music. tracknumber     | 1        |
| Aufzunehmen        | System. Music. albumtitle      | 1        |
| Künstler      | System. Music. Artist          | 1        |
| Genre        | System. Music. Genre           | 1        |
| Rating       | System. Rating                | 1        |
| Titel        | System.Title                 | 1        |
| Album-Künstlerin | System. Music. albumartist     | 2        |
| Bitrate     | System. Audio. encodingbitrate | 2        |
| Chor   | System. Music. Conductor       | 2        |
| Länge       | System. Media. Duration        | 2        |
| Protected    | System. DRM. IsProtected       | 2        |
| Jahr         | System. Media. Year            | 2        |



 

## <a name="pictures"></a>Bilder



| Name          | Eigenschaft                        | Priorität |
|---------------|---------------------------------|----------|
| Import Datum | System. dateimportiert             | 1        |
| Datum der Erstellung    | System. Photo. DateTaken          | 1        |
| Rating        | System. Rating                   | 1        |
| `Tags`          | System.Keywords                 | 1        |
| type          | System.PerceivedType            | 1        |
| Authors       | System.Author                   | 2        |
| Kamerahersteller  | System. Photo. cameramanufakturer | 2        |
| Kameramodell  | System. Photo. CameraModel        | 2        |
| Kommentare      | System. Comment                  | 2        |
| Dimensionen    | System. Image. Dimensions         | 2        |



 

## <a name="videos"></a>Videos



| Name         | Eigenschaft                 | Priorität |
|--------------|--------------------------|----------|
| Länge       | System. Media. Duration    | 1        |
| Rating       | System. Rating            | 1        |
| `Tags`         | System.Keywords          | 1        |
| type         | System.PerceivedType     | 1        |
| Rahmenhöhe | System. Video. frameheight | 2        |
| Rahmenbreite  | System. Video. framewidth  | 2        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Entwickeln von Eigenschaften Handlern für Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Eigenschaften System](../properties/building-property-handlers.md)
</dt> <dt>

[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
