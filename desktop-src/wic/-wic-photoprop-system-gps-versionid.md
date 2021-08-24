---
description: Die Fotometadatenrichtlinie für die System.GPS.VersionID-Eigenschaft.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: System.GPS.VersionID–Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857ecb6b172dafa2a771d9e81f8b570a89f458c79b7630a2f231ce84dbec4f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706360"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>System.GPS.VersionID–Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.VersionID-Eigenschaft.](../properties/props-system-gps-versionid.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ VersionID

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ UI

### <a name="input-type"></a>Eingabetyp

Buffer

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort=0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
