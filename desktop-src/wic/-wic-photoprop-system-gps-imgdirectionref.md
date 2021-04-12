---
description: Die fotometadatenrichtlinie für die System. GPS. imgdirectionref-Eigenschaft.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: System. GPS. imgdirectionref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218031"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a>System. GPS. imgdirectionref-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. imgdirectionref](../properties/props-system-gps-imgdirectionref.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

pkey \_ GPS. Imgdirectionref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /XMP/EXIF: gpsimgdirectionref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    | ascii       |
| 2     | /XMP/EXIF: gpsimgdirectionref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 16}    |
| 2     | /XMP/EXIF: gpsimgdirectionref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /IFD/XMP/EXIF: gpsimgdirectionref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 16}             | ascii       |
| 2     | /IFD/XMP/EXIF: gpsimgdirectionref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 16}             |
| 2     | /IFD/XMP/EXIF: gpsimgdirectionref |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. imgdirectionref](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
