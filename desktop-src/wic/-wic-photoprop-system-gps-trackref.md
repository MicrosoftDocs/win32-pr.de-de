---
description: Die Fotometadatenrichtlinie für die System.GPS.TrackRef-Eigenschaft.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: System.GPS.TrackRef-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a523f801b8e82fc4191b54bf0bb5fee659ab4f5b09c326d5d1adf14c713f13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087178"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>System.GPS.TrackRef-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.TrackRef-Eigenschaft.](../properties/props-system-gps-trackref.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ TrackRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=14} | ascii       |
| 2     | /xmp/exif:GPSTrackRef     | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=14} |
| 2     | /xmp/exif:gpstrackref     |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=14}      | ascii       |
| 2     | /ifd/xmp/exif:GPSTrackRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=14}      |
| 2     | /ifd/xmp/exif:gpstrackref |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.TrackRef](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
