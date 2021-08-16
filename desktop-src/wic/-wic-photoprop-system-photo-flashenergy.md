---
description: Die Richtlinie für Fotometadaten für die System.Photo.FlashStopp-Eigenschaft.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: System.Photo.Flash Speicher-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faebdcd32eaae346a44de9d1fa19f6954cb9d74ee9d79a09645216660845d16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204929"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>System.Photo.Flash Speicher-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.FlashStopp-Eigenschaft.](../properties/props-system-photo-flashenergy.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashKey

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41483} |             |
| 2     | /xmp/exif:Flash Led         |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41483} |             |
| 2     | /xmp/exif:Flash Led         |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41483} |
| 2     | /xmp/exif:flash blink         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=41483}  |             |
| 2     | /ifd/xmp/exif:Flash Led |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=41483}  |             |
| 2     | /ifd/xmp/exif:Flash Led |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=41483}  |
| 2     | /ifd/xmp/exif:flash blink |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.FlashStopp](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
