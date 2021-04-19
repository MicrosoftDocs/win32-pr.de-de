---
description: Die fotometadatenrichtlinie für die System. GPS. Track-Eigenschaft.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: System. GPS. Track Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369876"
---
# <a name="systemgpstrack-photo-metadata-policy"></a>System. GPS. Track Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. GPS. Track](../properties/props-system-gps-track.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Track

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. GPS. tracknumerator" und "System. GPS. tracknenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |             |
| 2     | /XMP/EXIF: gpstrack        |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |             |
| 2     | /XMP/EXIF: gpstrack        |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 15} |
| 2     | /XMP/EXIF: gpstrack        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 15}   |             |
| 2     | /IFD/XMP/EXIF: gpstrack |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 15}   |             |
| 2     | /IFD/XMP/EXIF: gpstrack |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /IFD/GPS/{ushort = 15}   |
| 2     | /IFD/XMP/EXIF: gpstrack |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Track](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
