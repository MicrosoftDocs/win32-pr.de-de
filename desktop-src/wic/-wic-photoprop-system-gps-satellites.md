---
description: Die fotometadatenrichtlinie für die System. GPS. Satellites-Eigenschaft.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: System. GPS. Satellites-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368790"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a>System. GPS. Satellites-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Satellites](../properties/props-system-gps-satellites.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Satelliten

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

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /XMP/EXIF: gpssatellites  | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 8} | ascii       |
| 2     | /XMP/EXIF: gpssatellites  | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 8} |
| 2     | /XMP/EXIF: gpssatellites  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /IFD/XMP/EXIF: gpssatellites | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 8}         | ascii       |
| 2     | /IFD/XMP/EXIF: gpssatellites | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /IFD/GPS/{ushort = 8}         |
| 2     | /IFD/XMP/EXIF: gpssatellites |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Satelliten](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
