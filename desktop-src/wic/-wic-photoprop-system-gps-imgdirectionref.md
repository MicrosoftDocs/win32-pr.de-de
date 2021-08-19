---
description: Die Fotometadatenrichtlinie für die System.GPS.ImgDirectionRef-Eigenschaft.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: System.GPS.ImgDirectionRef-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e735f91133d4ec473537f063e30d2d48f801a99f8f6bc80fa228b98a9bd95437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667897"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>System.GPS.ImgDirectionRef-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.ImgDirectionRef-Eigenschaft.](../properties/props-system-gps-imgdirectionref.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS. ImgDirectionRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=16}    | ascii       |
| 2     | /xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=16}    |
| 2     | /xmp/exif:gpsimgdirectionref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=16}             | ascii       |
| 2     | /ifd/xmp/exif:GPSImgDirectionRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=16}             |
| 2     | /ifd/xmp/exif:gpsimgdirectionref |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
