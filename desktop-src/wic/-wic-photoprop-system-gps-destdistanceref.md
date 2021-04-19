---
description: Die fotometadatenrichtlinie für die System. GPS. destdistanceref-Eigenschaft.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: System. GPS. destdistanceref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349665"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a>System. GPS. destdistanceref-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destdistanceref](../properties/props-system-gps-destdistanceref.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ destdistanceref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR oder VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /XMP/EXIF: gpsdestdistanceref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    | ascii       |
| 2     | /XMP/EXIF: gpsdestdistanceref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 25}    |
| 2     | /XMP/EXIF: gpsdestdistanceref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /IFD/XMP/EXIF: gpsdestdistanceref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 25}             | ascii       |
| 2     | /IFD/XMP/EXIF: gpsdestdistanceref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 25}             |
| 2     | /IFD/XMP/EXIF: gpsdestdistanceref |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destdistanceref](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
