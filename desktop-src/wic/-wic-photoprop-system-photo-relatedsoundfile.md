---
description: Die Fotometadatenrichtlinie für die System.Photo.RelatedSoundFile-Eigenschaft.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: System.Photo.RelatedSoundFile-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aae80ad39b8d3dab271aacf4815836e8b386c150ec80be63a83a4ab5937635e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549430"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>System.Photo.RelatedSoundFile-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.RelatedSoundFile-Eigenschaft.](../properties/props-system-photo-relatedsoundfile.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ RelatedSoundFile

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
