---
description: Die fotometadatenrichtlinie für die System. Photo. Schärding-Eigenschaft.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: System. Photo. Schärding-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362395"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>System. Photo. Schärding-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Schärding](../properties/props-system-photo-sharpness.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Schärfe

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
| 1     | /App1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /XMP/EXIF: Schärfe           | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /XMP/EXIF: Schärfe           | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41994} |
| 2     | /XMP/EXIF: Schärfe           |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: Schärfe  | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/EXIF: Schärfe  | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41994} |
| 2     | /IFD/XMP/EXIF: Schärfe  |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Schärding](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
