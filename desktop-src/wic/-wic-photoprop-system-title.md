---
description: Die fotometadatenrichtlinie für die System. Title-Eigenschaft.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: System. Title-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356948"
---
# <a name="systemtitle-photo-metadata-policy"></a>System. Title-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Title](../properties/props-system-title.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Titel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Entweder VT \_ LPWSTR oder VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                | Datenträger Format    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40091}            | Unicode- \_ Bytes |
| 2     | /XMP/ <xmpalt> DC: Title         | Unicode        |
| 3     | /XMP/DC: Title                       | Unicode        |
| 4     | /App1/IFD/EXIF/{ushort = 37510}       | Unicode        |
| 5     | /App1/IFD/{ushort = 270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /XMP/ <xmpalt> DC: Beschreibung   | Unicode        |
| 8     | /XMP/DC: Beschreibung                 | Unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                | Datenträger Format    |
|-------|-------------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 40091}            | Unicode- \_ Bytes |
| 2     | /XMP/DC: Title                       | Unicode        |
| 3     | /XMP/ <xmpalt> DC: Title         | Unicode        |
| 4     | /App1/IFD/EXIF/{ushort = 37510}       | Unicode        |
| 5     | /XMP/ <xmpalt> EXIF: UserComment | Unicode        |
| 6     | /App1/IFD/{ushort = 270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /XMP/DC: Beschreibung                 | Unicode        |
| 9     | /XMP/ <xmpalt> DC: Beschreibung   | Unicode        |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{ushort = 40091}            |
| 2     | /XMP/DC: Title                       |
| 3     | /App1/IFD/EXIF/{ushort = 37510}       |
| 4     | /XMP/ <xmpalt> EXIF: UserComment |
| 5     | /App1/IFD/{ushort = 270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /XMP/DC: Beschreibung                 |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                    | Datenträger Format    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | Unicode- \_ Bytes |
| 2     | /IFD/XMP/ <xmpalt> DC: Title         | Unicode        |
| 3     | /IFD/XMP/DC: Title                       | Unicode        |
| 4     | /IFD/EXIF/{ushort = 37510}                | Unicode        |
| 5     | /IFD/{ushort = 270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /IFD/XMP/ <xmpalt> DC: Beschreibung   | Unicode        |
| 8     | /IFD/XMP/DC: Beschreibung                 | Unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                    | Datenträger Format    |
|-------|-----------------------------------------|----------------|
| 1     | /IFD/{ushort = 40091}                     | Unicode- \_ Bytes |
| 2     | /IFD/XMP/DC: Title                       | Unicode        |
| 3     | /IFD/XMP/ <xmpalt> DC: Title         | Unicode        |
| 4     | /IFD/EXIF/{ushort = 37510}                | Unicode        |
| 5     | /IFD/XMP/ <xmpalt> EXIF: UserComment | Unicode        |
| 6     | /IFD/{ushort = 270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /IFD/XMP/DC: Beschreibung                 | Unicode        |
| 10    | /IFD/XMP/ <xmpalt> DC: Beschreibung   | Unicode        |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{ushort = 40091}                     |
| 2     | /IFD/XMP/DC: Title                       |
| 3     | /IFD/EXIF/{ushort = 37510}                |
| 4     | /IFD/XMP/ <xmpalt> EXIF: UserComment |
| 5     | /IFD/{ushort = 270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /IFD/XMP/DC: Beschreibung                 |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
