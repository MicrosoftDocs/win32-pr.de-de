---
description: Die Richtlinie für Fotometadaten für die System.Photo.Flash-Eigenschaft.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: System.Photo.Flash-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba32a7b4dfcde564f6b0c0c9e175aa56786e1324080264c7c928398fe97e6a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811730"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>System.Photo.Flash-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.Flash-Eigenschaft.](../properties/props-system-photo-exposuretime.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI1 (wenn das Quellschema XMP war) oder VT \_ UI2 (wenn das Quellschema EXIF war)

\\lang1036

### <a name="input-type"></a>Eingabetyp

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ <xmpstruct> exif:flash |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                 | Datenträgerformat |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                 | Datenträgerformat |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ <xmpstruct> exif:flash |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
