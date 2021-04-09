---
description: Die fotometadatenrichtlinie für die System. Photo. Program Mode-Eigenschaft.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: System. Photo. Program Mode-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960364"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a>System. Photo. Program Mode-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Program Mode](../properties/props-system-photo-programmode.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Programmmodus

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI4

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} | ushort      |
| 2     | /XMP/EXIF: ExposureProgram     | Unicode     |
| 3     | /XMP/EXIF: Programm Mode         | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} | ushort      |
| 2     | /XMP/EXIF: ExposureProgram     | Unicode     |
| 3     | /XMP/EXIF: Programm Mode         | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 34850} |
| 2     | /XMP/EXIF: ExposureProgram     |
| 3     | /XMP/EXIF: Programm Mode         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34850}      | ushort      |
| 2     | /IFD/XMP/EXIF: ExposureProgram | Unicode     |
| 3     | /IFD/XMP/EXIF: Programm Mode     | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34850}      | ushort      |
| 2     | /IFD/XMP/EXIF: ExposureProgram | Unicode     |
| 3     | /IFD/XMP/EXIF: Programm Mode     | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{ushort = 34850}      |
| 2     | /IFD/XMP/EXIF: ExposureProgram |
| 3     | /IFD/XMP/EXIF: Programm Mode     |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Program Mode](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
