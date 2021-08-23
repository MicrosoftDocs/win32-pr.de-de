---
description: Die Fotometadatenrichtlinie für die System.Photo.PeopleNames-Eigenschaft.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: System.Photo.PeopleNames-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4118cc8242d6dfe8a91d0bcd2b6039095fdf180037f51205d3541b9aefa2cc0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087049"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a>System.Photo.PeopleNames-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.PeopleNames-Eigenschaft.](../properties/props-system-photo-peoplenames.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PeopleNames

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

StringMulti

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                                           | Datenträgerformat |
|-------|----------------------------------------------------------------|-------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Schreibpfade

Diese Eigenschaft kann nicht mithilfe der Metadatenrichtlinie geschrieben werden.

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /xmp/ <xmpstruct> MP:RegionInfo |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                                               | Datenträgerformat |
|-------|--------------------------------------------------------------------|-------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo/ <xmpbag> MPRI:Regions | ushort      |



 

### <a name="write-paths"></a>Schreibpfade

Diese Eigenschaft kann nicht mithilfe der Metadatenrichtlinie geschrieben werden.

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /ifd/xmp/ <xmpstruct> MP:RegionInfo |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.ProgramMode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
