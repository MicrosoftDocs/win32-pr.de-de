---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Energy-Eigenschaft.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: System. Photo. Flash Energy-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050438"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a>System. Photo. Flash Energy-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Flash Energy](../properties/props-system-photo-flashenergy.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo \_ Flash Energy

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /XMP/EXIF: Flash Energy         |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |             |
| 2     | /XMP/EXIF: Flash Energy         |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41483} |
| 2     | /XMP/EXIF: Flash Energy         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |             |
| 2     | /IFD/XMP/EXIF: Flash Energy |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |             |
| 2     | /IFD/XMP/EXIF: Flash Energy |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 41483}  |
| 2     | /IFD/XMP/EXIF: Flash Energy |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Flash Energy](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
