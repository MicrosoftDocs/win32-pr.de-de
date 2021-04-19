---
description: Die fotometadatenrichtlinie für die System. Image. ColorSpace-Eigenschaft.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: System. Image. ColorSpace-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356197"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>System. Image. ColorSpace-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. ColorSpace](../properties/props-system-image-colorspace.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Image \_ Color Space

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /XMP/EXIF: colorspace          | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /XMP/EXIF: colorspace          | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 40961} |
| 2     | /XMP/EXIF: colorspace          |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /IFD/XMP/EXIF: colorspace | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 40961} | ushort      |
| 2     | /IFD/XMP/EXIF: colorspace | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 40961} |
| 2     | /IFD/XMP/EXIF: colorspace |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
