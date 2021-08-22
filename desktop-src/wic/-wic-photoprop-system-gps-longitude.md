---
description: Die Fotometadatenrichtlinie für die System.GPS.Longitude-Eigenschaft.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: System.GPS.Longitude Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff05dd8ada6e10bbd3109187d34b220ff352ae984f92bd68281c56d3c1a29a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087188"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>System.GPS.Longitude Photo Metadata Policy

Die Fotometadatenrichtlinie für die [System.GPS.Longitude-Eigenschaft.](../properties/props-system-gps-longitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ \_ GPS-Längengrad

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert kann durch Schreiben in System.GPS.LongitudeNumerator und System.GPS.LongitudeDenominator geschrieben werden. Er kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=4} |             |
| 2     | /xmp/exif:GPSLongitude   |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=4} |
| 2     | /xmp/exif:gpslongitude   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=4}        |             |
| 2     | /ifd/xmp/exif:GPSLongitude |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort=4}        |
| 2     | /ifd/xmp/exif:gpslongitude |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Longitude](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
