---
description: Die fotometadatenrichtlinie für die System. GPS. processingmethod-Eigenschaft.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: System. GPS. processingmethod-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359582"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>System. GPS. processingmethod-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. processingmethod](../properties/props-system-gps-processingmethod.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ processingmethod

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |             |
| 2     | /XMP/EXIF: gpsprocessingmethod | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |             |
| 2     | /XMP/EXIF: gpsprocessingmethod | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 27}     |
| 2     | /XMP/EXIF: gpsprocessingmethod |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                              | Datenträger Format |
|-------|-----------------------------------|-------------|
| 1     | /IFD/XMP/EXIF: gpsprocessingmethod | Unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                              | Datenträger Format |
|-------|-----------------------------------|-------------|
| 1     | /IFD/XMP/EXIF: gpsprocessingmethod | Unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                              |
|-------|-----------------------------------|
| 1     | /IFD/XMP/EXIF: gpsprocessingmethod |
| 2     | /IFD/GPS/{ushort = 27}              |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. processingmethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
