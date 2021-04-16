---
description: Die fotometadatenrichtlinie für die System. GPS. Differential-Eigenschaft.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: System. GPS. differenzielle fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348578"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>System. GPS. differenzielle fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Differential](../properties/props-system-gps-differential.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ -GPS- \_ differenziell

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ UI1, VT \_ UI2 und VT \_ UI4 werden alle akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /XMP/EXIF: gpsdifferential | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /XMP/EXIF: gpsdifferential | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 30} |
| 2     | /XMP/EXIF: gpsdifferential |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 30}          | ushort      |
| 2     | /IFD/XMP/EXIF: gpsdifferential | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 30}          | ushort      |
| 2     | /IFD/XMP/EXIF: gpsdifferential | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 30}          |
| 2     | /IFD/XMP/EXIF: gpsdifferential |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
