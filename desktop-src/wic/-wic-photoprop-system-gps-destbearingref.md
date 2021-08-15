---
description: Die Richtlinie für Fotometadaten für die System.GPS.DestBearingRef-Eigenschaft.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: System.GPS.DestBearingRef-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ee4b984d0a759769b80be76b53499690673c7ec630c759aa0371b53ea9368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087851"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>System.GPS.DestBearingRef-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.DestBearingRef-Eigenschaft.](../properties/props-system-gps-destbearingref.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestBearingRef

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



| Auftrag | Pfad                        | Datenträgerformat |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                        | Datenträgerformat |
|-------|-----------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=23}   | ascii       |
| 2     | /xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /app1/ifd/gps/{ushort=23}   |
| 2     | /xmp/exif:gpsdestbearingref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                            | Datenträgerformat |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                            | Datenträgerformat |
|-------|---------------------------------|-------------|
| 1     | /ifd/gps/{ushort=23}            | ascii       |
| 2     | /ifd/xmp/exif:GPSDestBearingRef | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| order | path                            |
|-------|---------------------------------|
| 1     | /ifd/gps/{ushort=23}            |
| 2     | /ifd/xmp/exif:gpsdestbearingref |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DestBearingRef](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
