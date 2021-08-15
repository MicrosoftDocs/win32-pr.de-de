---
description: Die Fotometadatenrichtlinie für die System.GPS.SpeedRef-Eigenschaft.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: System.GPS.SpeedRef-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c7b60a0c8decaf5ecc30f9017a0aadc61bb9fe4814240fb7ab2e022d6a2873f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549490"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>System.GPS.SpeedRef-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.SpeedRef-Eigenschaft.](../properties/props-system-gps-speedref.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ SpeedRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      |         |
|-------|---------------------------|---------|
| 1     | /ifd/gps/{ushort=12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
