---
description: Die fotometadatenrichtlinie für die System. GPS. versionID-Eigenschaft.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: System. GPS. versionID Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362266"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>System. GPS. versionID Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. versionID](../properties/props-system-gps-versionid.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ versionID

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ UI

### <a name="input-type"></a>Eingabetyp

Buffer

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |             |
| 2     | /XMP/EXIF: gpsversionid   | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |             |
| 2     | /XMP/EXIF: gpsversionid   | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 0} |
| 2     | /XMP/EXIF: gpsversionid   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 0}        |             |
| 2     | /IFD/XMP/EXIF: gpsversionid | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 0}        |             |
| 2     | /IFD/XMP/EXIF: gpsversionid | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 0}        |
| 2     | /IFD/XMP/EXIF: gpsversionid |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. versionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
