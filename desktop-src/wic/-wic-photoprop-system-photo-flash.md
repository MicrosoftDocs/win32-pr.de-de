---
description: Die Richtlinie für Fotometadaten für die System.Photo.Flash-Eigenschaft.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: System.Photo.Flash-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880072"
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



| Order | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:flash |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                 | Datenträgerformat |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                 | Datenträgerformat |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:flash |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
