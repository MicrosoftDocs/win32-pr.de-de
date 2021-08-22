---
description: Die Fotometadatenrichtlinie für die System.GPS.DestDistanceRef-Eigenschaft.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: System.GPS.DestDistanceRef-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d7973a3be36f9a7624ed8679f364c898d69b622de067bdd2595f3b919a964f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964979"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>System.GPS.DestDistanceRef-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.DestDistanceRef-Eigenschaft.](../properties/props-system-gps-destdistanceref.md)

### <a name="pkey"></a>PKEY

PKEY \_ DestDistanceRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR oder VT \_ LPSTR werden akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                         | Datenträgerformat |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=25}    | ascii       |
| 2     | /xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=25}    |
| 2     | /xmp/exif:gpsdestdistanceref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=25}             | ascii       |
| 2     | /ifd/xmp/exif:GPSDestDistanceRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=25}             |
| 2     | /ifd/xmp/exif:gpsdestdistanceref |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
