---
description: Die fotometadatenrichtlinie für die System. GPS. imgdirection-Eigenschaft.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: System. GPS. imgdirection-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349664"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a>System. GPS. imgdirection-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. imgdirection](../properties/props-system-gps-imgdirection.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ imgdirection

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert kann durch Schreiben in System. GPS. imgdirectionnumerator und System. GPS. imgdirectionnenner geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 17} |             |
| 2     | /XMP/EXIF: gpsimgdirection |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 17} |             |
| 2     | /XMP/EXIF: gpsimgdirection |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 17} |
| 2     | /XMP/EXIF: gpsimgdirection |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 17}          |             |
| 2     | /IFD/XMP/EXIF: gpsimgdirection |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 17}          |             |
| 2     | /IFD/XMP/EXIF: gpsimgdirection |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 17}          |
| 2     | /IFD/XMP/EXIF: gpsimgdirection |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. imgdirection](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
