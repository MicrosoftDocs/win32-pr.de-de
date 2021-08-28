---
description: Die Richtlinie für Fotometadaten für die System.Photo.DateTaken-Eigenschaft.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: System.Photo.DateTaken-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691476c704d3fdbc4ff5e01467031f2b41884ccb16be537904484a9d01c8fa18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087076"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a>System.Photo.DateTaken-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.DateTaken-Eigenschaft.](../properties/props-system-photo-datetaken.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DateTaken

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ FILETIME

### <a name="input-type"></a>Eingabetyp

Datetime

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                  | Datenträgerformat |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | Unicode     |
| 3     | /xmp/xmp:CreateDate                   | Unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /app13/irb/8bimiptc/iptc/date created | Unicode     |
| 6     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                  | Datenträgerformat |
|-------|---------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=36867}         | ascii       |
| 2     | /app13/irb/8bimiptc/iptc/date created | Unicode     |
| 3     | /xmp/xmp:CreateDate                   | Unicode     |
| 4     | /app1/ifd/exif/{ushort=36868}         | ascii       |
| 5     | /xmp/exif:DateTimeOriginal            | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                  |
|-------|---------------------------------------|
| 1     | /app1/ifd/exif/{ushort=36867}         |
| 2     | /app1/ifd/exif/{ushort=37521}         |
| 3     | /app1/ifd/exif/{ushort=36868}         |
| 4     | /app1/ifd/exif/{ushort=37522}         |
| 5     | /xmp/exif:DateTimeOriginal            |
| 6     | /xmp/xmp:CreateDate                   |
| 7     | /app13/irb/8bimiptc/iptc/date created |
| 8     | /app13/irb/8bimiptc/iptc/time created |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                | Datenträgerformat |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | Unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | Unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/iptc/date created              | Unicode     |
| 6     | /ifd/irb/8bimiptc/iptc/date created | Unicode     |
| 7     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                | Datenträgerformat |
|-------|-------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=36867}            | ascii       |
| 2     | /ifd/iptc/date created              | Unicode     |
| 3     | /ifd/xmp/xmp:CreateDate             | Unicode     |
| 4     | /ifd/exif/{ushort=36868}            | ascii       |
| 5     | /ifd/irb/8bimiptc/iptc/date created | Unicode     |
| 6     | /ifd/xmp/exif:DateTimeOriginal      | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /ifd/exif/{ushort=36867}            |
| 2     | /ifd/exif/{ushort=37521}            |
| 3     | /ifd/exif/{ushort=36868}            |
| 4     | /ifd/exif/{ushort=37522}            |
| 5     | /ifd/xmp/exif:DateTimeOriginal      |
| 6     | /ifd/xmp/xmp:CreateDate             |
| 7     | /ifd/iptc/date created              |
| 8     | /ifd/iptc/time created              |
| 9     | /ifd/irb/8bimiptc/iptc/date created |
| 10    | /ifd/irb/8bimiptc/iptc/time created |



 

### <a name="png-policy"></a>PNG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /\[\*\]tEXt/Erstellungszeit | ascii       |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 2     | /\[\*\]tEXt/Erstellungszeit | ascii       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 3     | /\[\*\]tEXt/Erstellungszeit |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.DateTaken](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
