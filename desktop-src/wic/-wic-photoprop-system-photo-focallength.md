---
description: Die fotometadatenrichtlinie für die System. Photo. focalLength-Eigenschaft.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: System. Photo. focalLength-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364071"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>System. Photo. focalLength-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. focalLength](../properties/props-system-photo-focallength.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo \_ focalLength

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von System. Photo. focallengthnumerator und System. Photo. focallengthnenner generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /XMP/EXIF: focalLength         |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |             |
| 2     | /XMP/EXIF: focalLength         |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37386} |
| 2     | /XMP/EXIF: focalLength         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |             |
| 2     | /IFD/XMP/EXIF: focalLength |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |             |
| 2     | /IFD/XMP/EXIF: focalLength |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 37386}  |
| 2     | /IFD/XMP/EXIF: focalLength |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. focalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
