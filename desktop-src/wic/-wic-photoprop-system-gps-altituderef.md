---
description: Die Richtlinie für Fotometadaten für die System.GPS.AltitudeRef-Eigenschaft.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: System.GPS.AltitudeRef-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca49213754f605dcf6df40dfa3ff00e2b7aeaf765008037c23da21e35ab9ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710697"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a>System.GPS.AltitudeRef-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.AltitudeRef-Eigenschaft.](../properties/props-system-gps-altituderef.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AltitudeRef

### <a name="description"></a>BESCHREIBUNG

Gibt die Höhe an, die als Referenzhöhe verwendet wird. Der Wert 0 gibt an, dass die Höhe oberhalb des Seeniveaus liegt. Der Wert 1 gibt eine Höhe unterhalb des Seeniveaus an.

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI1

### <a name="input-type"></a>Eingabetyp

Byte.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=5} | byte        |
| 2     | /xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=5} |
| 2     | /xmp/exif:gpsaltituderef |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=5}          | byte        |
| 2     | /ifd/xmp/exif:GPSAltitudeRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=5}          |
| 2     | /ifd/xmp/exif:gpsaltituderef |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
