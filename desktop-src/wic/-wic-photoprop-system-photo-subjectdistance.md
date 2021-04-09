---
description: Die fotometadatenrichtlinie für die System. Photo. subjetdistance-Eigenschaft.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: System. Photo. subjetdistance-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867328"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a>System. Photo. subjetdistance-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. subjetdistance](../properties/props-system-photo-subjectdistance.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto ( \_ subjetdistance)

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. subjetdistancenenumerator" und "System. Photo. subjetdistancenenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37382} |             |
| 2     | /XMP/EXIF: subjetdistance     |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37382} |             |
| 2     | /XMP/EXIF: subjetdistance     |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37382} |
| 2     | /XMP/EXIF: subjetdistance     |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37382}      |             |
| 2     | /IFD/XMP/EXIF: subjetdistance |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37382}      |             |
| 2     | /IFD/XMP/EXIF: subjetdistance |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{ushort = 37382}      |
| 2     | /IFD/XMP/EXIF: subjetdistance |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. subjetdistance](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
