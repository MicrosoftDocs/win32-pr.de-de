---
description: Die fotometadatenrichtlinie für die System. Photo. DateTaken-Eigenschaft.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: System. Photo. DateTaken-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366225"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>System. Photo. DateTaken-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto, \_ DateTaken

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ FILETIME

### <a name="input-type"></a>Eingabetyp

Datetime

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                  | Datenträger Format |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date erstellt | Unicode     |
| 3     | /XMP/XMP: kreatedate                   | Unicode     |
| 4     | /App1/IFD/EXIF/{ushort = 36868}         | ascii       |
| 5     | /app13/IRB/8bimiptc/IPTC/Date erstellt | Unicode     |
| 6     | /XMP/EXIF: DateTimeOriginal            | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                  | Datenträger Format |
|-------|---------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         | ascii       |
| 2     | /app13/IRB/8bimiptc/IPTC/Date erstellt | Unicode     |
| 3     | /XMP/XMP: kreatedate                   | Unicode     |
| 4     | /App1/IFD/EXIF/{ushort = 36868}         | ascii       |
| 5     | /XMP/EXIF: DateTimeOriginal            | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                  |
|-------|---------------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 36867}         |
| 2     | /App1/IFD/EXIF/{ushort = 37521}         |
| 3     | /App1/IFD/EXIF/{ushort = 36868}         |
| 4     | /App1/IFD/EXIF/{ushort = 37522}         |
| 5     | /XMP/EXIF: DateTimeOriginal            |
| 6     | /XMP/XMP: kreatedate                   |
| 7     | /app13/IRB/8bimiptc/IPTC/Date erstellt |
| 8     | /app13/IRB/8bimiptc/IPTC/Time erstellt |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date erstellt              | Unicode     |
| 3     | /IFD/XMP/XMP: kreatedate             | Unicode     |
| 4     | /IFD/EXIF/{ushort = 36868}            | ascii       |
| 5     | /IFD/IPTC/Date erstellt              | Unicode     |
| 6     | /IFD/IRB/8bimiptc/IPTC/Date erstellt | Unicode     |
| 7     | /IFD/XMP/EXIF: DateTimeOriginal      | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 36867}            | ascii       |
| 2     | /IFD/IPTC/Date erstellt              | Unicode     |
| 3     | /IFD/XMP/XMP: kreatedate             | Unicode     |
| 4     | /IFD/EXIF/{ushort = 36868}            | ascii       |
| 5     | /IFD/IRB/8bimiptc/IPTC/Date erstellt | Unicode     |
| 6     | /IFD/XMP/EXIF: DateTimeOriginal      | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{ushort = 36867}            |
| 2     | /IFD/EXIF/{ushort = 37521}            |
| 3     | /IFD/EXIF/{ushort = 36868}            |
| 4     | /IFD/EXIF/{ushort = 37522}            |
| 5     | /IFD/XMP/EXIF: DateTimeOriginal      |
| 6     | /IFD/XMP/XMP: kreatedate             |
| 7     | /IFD/IPTC/Date erstellt              |
| 8     | /IFD/IPTC/Time erstellt              |
| 9     | /IFD/IRB/8bimiptc/IPTC/Date erstellt |
| 10    | /IFD/IRB/8bimiptc/IPTC/Time erstellt |



 

### <a name="png-policy"></a>PNG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /\[\*\]Text/Erstellungszeit | ascii       |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 2     | /\[\*\]Text/Erstellungszeit | ascii       |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 3     | /\[\*\]Text/Erstellungszeit |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
