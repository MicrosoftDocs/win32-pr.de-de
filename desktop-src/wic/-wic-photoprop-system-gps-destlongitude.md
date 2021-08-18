---
description: Die Richtlinie für Fotometadaten für die System.GPS.DestLongitude-Eigenschaft.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: System.GPS.DestLongitude-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 917c65dbd580b00cf25603e04050386383967e3a70c1896405346652667ef5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087841"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>System.GPS.DestLongitude-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.DestLongitude-Eigenschaft.](../properties/props-system-gps-destlongitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.GPS.DestLongitudeNumerator und System.GPS.DestLongitudeDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /app1/ifd/gps/{ushort=22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/gps/{ushort=22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/gps/{ushort=22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
