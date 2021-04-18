---
description: Die fotometadatenrichtlinie für die System. GPS. Longitude-Eigenschaft.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: System. GPS. Längengrade Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351062"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a>System. GPS. Längengrade Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. GPS. Longitude](../properties/props-system-gps-longitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Längengrad

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Sie können diesen Wert schreiben, indem Sie in System. GPS. in "System. GPS................. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |             |
| 2     | /XMP/EXIF: gpslängen Grad   |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |             |
| 2     | /XMP/EXIF: gpslängen Grad   |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 4} |
| 2     | /XMP/EXIF: gpslängen Grad   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /IFD/XMP/EXIF: gpslängen Grad |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 4}        |             |
| 2     | /IFD/XMP/EXIF: gpslängen Grad |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 4}        |
| 2     | /IFD/XMP/EXIF: gpslängen Grad |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Längengrad](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
