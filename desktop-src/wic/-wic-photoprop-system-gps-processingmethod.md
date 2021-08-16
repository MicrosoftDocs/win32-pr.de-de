---
description: Die Richtlinie für Fotometadaten für die System.GPS.ProcessingMethod-Eigenschaft.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: System.GPS.ProcessingMethod-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800515d3a7870fa2dc9b5a6ec8c19178889482fa820f66d7d98e8e3ff09870f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931740"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>System.GPS.ProcessingMethod-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.ProcessingMethod-Eigenschaft.](../properties/props-system-gps-processingmethod.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/gps/{ushort=27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                              | Datenträgerformat |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                              | Datenträgerformat |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | Unicode     |
| 2     | /ifd/gps/{ushort=27}              |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /ifd/gps/{ushort=27}              |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
