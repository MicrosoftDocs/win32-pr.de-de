---
description: Die Fotometadatenrichtlinie für die System.Image.ColorSpace-Eigenschaft.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: System.Image.ColorSpace-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710420"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>System.Image.ColorSpace-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Image.ColorSpace-Eigenschaft.](../properties/props-system-image-colorspace.md)

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ ColorSpace

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Image.ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
