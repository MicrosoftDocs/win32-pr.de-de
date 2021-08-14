---
description: Die Fotometadatenrichtlinie für die System.GPS.ImgDirection-Eigenschaft.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: System.GPS.ImgDirection-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43544458c4b6a64df1d396426ebbe487d80324d24dd10c2f8f6f0e548d9eca99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710670"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>System.GPS.ImgDirection-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.ImgDirection-Eigenschaft.](../properties/props-system-gps-imgdirection.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ImgDirection

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert kann durch Schreiben in System.GPS.ImgDirectionNumerator und System.GPS.ImgDirectionDenominator geschrieben werden. Er kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=17} |             |
| 2     | /xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=17} |
| 2     | /xmp/exif:gpsimgdirection |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=17}          |             |
| 2     | /ifd/xmp/exif:GPSImgDirection |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=17}          |
| 2     | /ifd/xmp/exif:gpsimgdirection |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
