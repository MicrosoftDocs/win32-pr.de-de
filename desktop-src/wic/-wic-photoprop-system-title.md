---
description: Die Richtlinie für Fotometadaten für die System.Title-Eigenschaft.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: System.Title Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa43b31595928fa3c2c936de8710131c20f17b1a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880684"
---
# <a name="systemtitle-photo-metadata-policy"></a>System.Title Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.Title-Eigenschaft.](../properties/props-system-title.md)

### <a name="pkey"></a>PKEY

\_PKEY-Titel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

Entweder VT \_ LPWSTR oder VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                | Datenträgerformat    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | \_Unicode-Bytes |
| 2     | /xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 3     | /xmp/dc:title                       | Unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | Unicode        |
| 5     | /app1/ifd/{ushort=270}              | ascii          |
| 6     | /app13/irb/8bimiptc/iptc/caption    |                |
| 7     | /xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |
| 8     | /xmp/dc:description                 | Unicode        |
| 9     | /app13/irb/8bimiptc/iptc/caption    |                |
| 10    | /xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                | Datenträgerformat    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40091}            | \_Unicode-Bytes |
| 2     | /xmp/dc:title                       | Unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 4     | /app1/ifd/exif/{ushort=37510}       | Unicode        |
| 5     | /xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |
| 6     | /app1/ifd/{ushort=270}              | ascii          |
| 7     | /app13/irb/8bimiptc/iptc/caption    |                |
| 8     | /xmp/dc:description                 | Unicode        |
| 9     | /xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=40091}            |
| 2     | /xmp/dc:title                       |
| 3     | /app1/ifd/exif/{ushort=37510}       |
| 4     | /xmp/ &lt; xmpalt &gt; exif:UserComment |
| 5     | /app1/ifd/{ushort=270}              |
| 6     | /app13/irb/8bimiptc/iptc/caption    |
| 7     | /xmp/dc:description                 |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                    | Datenträgerformat    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40091}                     | \_Unicodebytes |
| 2     | /ifd/xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 3     | /ifd/xmp/dc:title                       | Unicode        |
| 4     | /ifd/exif/{ushort=37510}                | Unicode        |
| 5     | /ifd/{ushort=270}                       | ascii          |
| 6     | /ifd/iptc/caption                       |                |
| 7     | /ifd/xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |
| 8     | /ifd/xmp/dc:description                 | Unicode        |
| 9     | /ifd/iptc/caption                       |                |
| 10    | /ifd/irb/8bimiptc/iptc/caption          |                |
| 11    | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                    | Datenträgerformat    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40091}                     | \_Unicodebytes |
| 2     | /ifd/xmp/dc:title                       | Unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; dc:title         | Unicode        |
| 4     | /ifd/exif/{ushort=37510}                | Unicode        |
| 5     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |
| 6     | /ifd/{ushort=270}                       | ascii          |
| 7     | /ifd/iptc/caption                       |                |
| 8     | /ifd/irb/8bimiptc/iptc/caption          |                |
| 9     | /ifd/xmp/dc:description                 | Unicode        |
| 10    | /ifd/xmp/ &lt; xmpalt &gt; dc:description   | Unicode        |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort=40091}                     |
| 2     | /ifd/xmp/dc:title                       |
| 3     | /ifd/exif/{ushort=37510}                |
| 4     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment |
| 5     | /ifd/{ushort=270}                       |
| 6     | /ifd/iptc/caption                       |
| 7     | /ifd/irb/8bimiptc/iptc/caption          |
| 8     | /ifd/xmp/dc:description                 |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Title](../properties/props-system-title.md)
</dt> </dl>

 

 
