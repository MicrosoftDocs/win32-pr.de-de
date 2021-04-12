---
description: Die fotometadatenrichtlinie für die System. Image. ImageID-Eigenschaft.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: System. Image. ImageID-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529270"
---
# <a name="systemimageimageid-photo-metadata-policy"></a>System. Image. ImageID-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. ImageID](../properties/props-system-image-imageid.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Image- \_ ImageID

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /XMP/EXIF: imageuniqueid       | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} | ascii       |
| 2     | /XMP/EXIF: imageuniqueid       | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 42016} |
| 2     | /XMP/EXIF: imageuniqueid       |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{ushort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: imageuniqueid | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
|       | /IFD/EXIF/{ushort = 42016}    | ascii       |
|       | /IFD/XMP/EXIF: imageuniqueid | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        |
|-------|-----------------------------|
|       | /IFD/EXIF/{ushort = 42016}    |
|       | /IFD/XMP/EXIF: imageuniqueid |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. ImageID](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
