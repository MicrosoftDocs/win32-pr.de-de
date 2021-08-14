---
description: Die Richtlinie für Fotometadaten für die System.GPS.Satellites-Eigenschaft.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: System.GPS.Satellites-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65bdc244324df513b5029c682e9c2cb355da58f2c95d13910fe093ce2521c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964839"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>System.GPS.Satellites-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.Satellites-Eigenschaft.](../properties/props-system-gps-satellites.md)

### <a name="pkey"></a>PKEY

\_ \_ PKEY-GPS-Satelliten

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=8} | ascii       |
| 2     | /xmp/exif:GPSSatellites  | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=8} |
| 2     | /xmp/exif:gpssatellites  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                        | Datenträgerformat |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                        | Datenträgerformat |
|-------|-----------------------------|-------------|
| 1     | /ifd/gps/{ushort=8}         | ascii       |
| 2     | /ifd/xmp/exif:GPSSatellites | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /ifd/gps/{ushort=8}         |
| 2     | /ifd/xmp/exif:gpssatellites |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Satellites](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
