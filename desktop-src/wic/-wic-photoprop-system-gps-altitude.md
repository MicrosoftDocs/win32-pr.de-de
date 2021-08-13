---
description: Die Richtlinie für Fotometadaten für die System.GPS.Altitude-Eigenschaft.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: System.GPS.Altitude Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a9209bfb0bbc1a4c6f95ce4a995d32d3f532c293dd2295c335eea61c22df89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442000"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>System.GPS.Altitude Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.GPS.Altitude-Eigenschaft.](../properties/props-system-gps-altitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ \_ GPS-Höhe

### <a name="description"></a>Beschreibung

Die Höhe wird als absoluter Wert angegeben, auf den in Metern verwiesen wird.

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert kann durch Schreiben in System.GPS.Altitude.Numerator und System.GPS.Altitude.Denominator geschrieben werden. Sie kann nicht direkt geschrieben werden. Die Schreibpfade in den folgenden Tabellen geben an, wo der Wert gespeichert werden kann, wenn er generiert wird, nicht, wenn er direkt geschrieben wird. Wenn der Wert gelesen wird, werden Werte aus verschiedenen Schemas abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |     |
|-------|---------------------------|-----|
| 1     | /ifd/gps/{ushort=6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Altitude](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
