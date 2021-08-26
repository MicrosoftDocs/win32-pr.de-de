---
description: Die Richtlinie für Fotometadaten für die System.Photo.EXIFVersion-Eigenschaft.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: System.Photo.EXIFVersion-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eee0fdac7ba8e86321d4a055cb6c37c4e9c7bad3f5bcfced548cc2485b3347c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882030"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>System.Photo.EXIFVersion-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.EXIFVersion-Eigenschaft.](../properties/props-system-photo-exifversion.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ EXIFVersion

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

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | \_Exif-Version |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat   |
|-------|-------------------------------|---------------|
| 1     | /app1/ifd/exif/{ushort=36864} | \_Exif-Version |
| 2     | /xmp/exif:ExifVersion         | Unicode       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | \_Exif-Version |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat   |
|-------|---------------------------|---------------|
| 1     | /ifd/exif/{ushort=36864}  | \_Exif-Version |
| 2     | /ifd/xmp/exif:ExifVersion | Unicode       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
