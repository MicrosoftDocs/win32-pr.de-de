---
description: Die Fotometadatenrichtlinie für die System.Photo.FocalLength-Eigenschaft.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: System.Photo.FocalLength-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbfb1c0a5a8d88993a42ecc1d29e70f3f3d5911d3c0451cbeeaf0ace040460d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667367"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>System.Photo.FocalLength-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.FocalLength-Eigenschaft.](../properties/props-system-photo-focallength.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FocalLength

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird aus System.Photo.FocalLengthNumerator und System.Photo.FocalLengthDenominator generiert. Er kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37386} |
| 2     | /xmp/exif:focallength         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=37386}  |
| 2     | /ifd/xmp/exif:focallength |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
