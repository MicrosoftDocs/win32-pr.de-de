---
description: Die fotometadatenrichtlinie für die System. Photo. Flash-Eigenschaft.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: System. Photo. Flash-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373146"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>System. Photo. Flash-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Flash](../properties/props-system-photo-exposuretime.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo \_ Flash

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI1 (wenn das Quell Schema XMP war) oder VT \_ UI2 (wenn das Quell Schema EXIF war)

\\lang1036

### <a name="input-type"></a>Eingabetyp

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    | ushort      |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37385}    |
| 2     | /XMP/ <xmpstruct> EXIF: Flash |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                 | Datenträger Format |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                 | Datenträger Format |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37385}             | ushort      |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{ushort = 37385}             |
| 2     | /IFD/XMP/ <xmpstruct> EXIF: Flash |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
