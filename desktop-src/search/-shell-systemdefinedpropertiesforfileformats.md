---
description: Microsoft Windows stellt eine Reihe von Systemeigenschaften zur Verfügung, die Sie für Ihre Dateiformate verwenden können.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: System-Defined eigenschaften für benutzerdefinierte Dateiformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28dcf137d10fffb3cc192acf66b1279b83fd079b6b81cf963dfed8a78408388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944500"
---
# <a name="system-defined-properties-for-custom-file-formats"></a>System-Defined eigenschaften für benutzerdefinierte Dateiformate

Microsoft Windows stellt eine Reihe von Systemeigenschaften zur Verfügung, die Sie für Ihre Dateiformate verwenden können. Wenn Sie ein benutzerdefiniertes Dateiformat erstellen, sollten Sie so viele systemdefinierte Eigenschaften wie möglich unterstützen. Bevor Sie einen benutzerdefinierten Eigenschaftenhandler erstellen, sollten Sie die vom System bereitgestellten Handler überprüfen, um zu überprüfen, ob Sie einen handler verwenden können, anstatt einen eigenen zu schreiben.

Die folgende Tabelle kategorisiert Dateiformate und listet dann die wichtigsten Systemeigenschaften auf, die Ihr Dateiformat unterstützen sollte. Um eine gute Benutzererfahrung zu bieten, sollten Sie alle Eigenschaften der Priorität 1 und 2 für Ihre Kategorie des Dateiformats unterstützen.

-   [Kommunikation](#communications)
-   [Kontakte](#contacts)
-   [Dokumente](#documents)
-   [Allgemein](#generic)
-   [Musik](#music)
-   [Bilder](#pictures)
-   [Videos](#videos)
-   [Zugehörige Themen](#related-topics)

## <a name="communications"></a>Kommunikation



| Name            | Eigenschaft                               | Priorität |
|-----------------|----------------------------------------|----------|
| Empfangenes Datum   | System.Message.DateReceived            | 1        |
| Aus Namen      | System.Message.FromName                | 1        |
| Verfügt über Anlagen | System.Message.HasAttachments          | 1        |
| Mailbox         | System.Communication.storeddisplayname | 1        |
| Name            | System.FileName                        | 1        |
| Gegenstand         | System.Subject                         | 1        |
| An Namen        | System.Message.ToName                  | 1        |
| Kategorie        | System.Category                        | 2        |
| type            | System.PerceivedType                   | 2        |



 

## <a name="contacts"></a>Kontakte



| Name             | Eigenschaft                           | Priorität |
|------------------|------------------------------------|----------|
| Kontoname     | System.Communication.AccountName   | 1        |
| Telefon (geschäftlich)   | System.Contact.BusinessTelephone   | 1        |
| Company          | System.Company                     | 1        |
| E-Mail-Adresse    | System.Contact.PrimaryEmailAddress | 1        |
| Wichtigkeit       | System.ImportanceText              | 1        |
| Mobiltelefon     | System.Contact.MobileTelephone     | 1        |
| Geschäftsadresse | System.Contact.BusinessAddress     | 2        |
| Geschäftsfax     | System.Contact.BusinessFaxNumber   | 2        |
| Kategorie         | System.Category                    | 2        |
| Home-Adresse     | System.Contact.HomeAddress         | 2        |
| Telefon (privat)       | System.Contact.HomeTelephone       | 2        |
| Titel            | System.Title                       | 2        |



 

## <a name="documents"></a>Dokumente



| Name      | Eigenschaft             | Priorität |
|-----------|----------------------|----------|
| Authors   | System.Author        | 1        |
| Volltext | System.FullText      | 1        |
| `Tags`      | System.Keywords      | 1        |
| type      | System.PerceivedType | 1        |
| Kategorie  | System.Category      | 2        |
| Titel     | System.Title         | 2        |



 

## <a name="generic"></a>Allgemein



| Name     | Eigenschaft             | Priorität |
|----------|----------------------|----------|
| Authors  | System.Author        | 1        |
| Titel    | System.Title         | 1        |
| type     | System.PerceivedType | 1        |
| Kategorie | System.Category      | 2        |
| `Tags`     | System.Keywords      | 2        |



 

## <a name="music"></a>Musik



| Name         | Eigenschaft                     | Priorität |
|--------------|------------------------------|----------|
| \#           | System. Musik. TrackNumber     | 1        |
| Album        | System. Musik. AlbumTitle      | 1        |
| Künstler      | System. Musik. Künstler          | 1        |
| Genre        | System. Musik. Genre           | 1        |
| Rating       | System.Rating                | 1        |
| Titel        | System.Title                 | 1        |
| Albumartist | System. Musik. AlbumArtist     | 2        |
| Bitrate     | System.Audio.EncodingBitrate | 2        |
| Leiter   | System. Musik. Dirigent       | 2        |
| Länge       | System.Media.Duration        | 2        |
| Protected    | System.DRM.IsProtected       | 2        |
| Jahr         | System.Media.Year            | 2        |



 

## <a name="pictures"></a>Bilder



| Name          | Eigenschaft                        | Priorität |
|---------------|---------------------------------|----------|
| Importiertes Datum | System.DateImported             | 1        |
| Datum der Erstellung    | System.Photo.DateTaken          | 1        |
| Rating        | System.Rating                   | 1        |
| `Tags`          | System.Keywords                 | 1        |
| type          | System.PerceivedType            | 1        |
| Authors       | System.Author                   | 2        |
| Kameraersteller  | System.Photo.CameraManufacturer | 2        |
| Kameramodell  | System.Photo.CameraModel        | 2        |
| Kommentare      | System.Comment                  | 2        |
| Dimensionen    | System.Image.Dimensions         | 2        |



 

## <a name="videos"></a>Videos



| Name         | Eigenschaft                 | Priorität |
|--------------|--------------------------|----------|
| Länge       | System.Media.Duration    | 1        |
| Rating       | System.Rating            | 1        |
| `Tags`         | System.Keywords          | 1        |
| type         | System.PerceivedType     | 1        |
| Framehöhe | System.Video.FrameHeight | 2        |
| Rahmenbreite  | System.Video.FrameWidth  | 2        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Entwickeln von Eigenschaftenhandlern für die Windows Suche](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Eigenschaftensystem](../properties/building-property-handlers.md)
</dt> <dt>

[Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 
