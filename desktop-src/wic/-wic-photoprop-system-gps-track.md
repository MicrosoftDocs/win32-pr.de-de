---
description: Die Richtlinie für Fotometadaten für die System.GPS.Track-Eigenschaft.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: System.GPS.Track-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89aee05d0c55e78fe4e55d7eacd8a8d0992fcb8d9f56312164c652cbc0bd81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205531"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>System.GPS.Track-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.Track-Eigenschaft.](../properties/props-system-gps-track.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ Track

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.GPS.TrackNumerator und System.GPS.TrackDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=15} |             |
| 2     | /xmp/exif:GPSTrack        |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=15} |
| 2     | /xmp/exif:gpstrack        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /ifd/gps/{ushort=15}   |             |
| 2     | /ifd/xmp/exif:GPSTrack |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /ifd/gps/{ushort=15}   |
| 2     | /ifd/xmp/exif:gpstrack |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
