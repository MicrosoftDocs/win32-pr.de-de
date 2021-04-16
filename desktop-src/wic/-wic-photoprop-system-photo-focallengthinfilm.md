---
description: Die fotometadatenrichtlinie für die System. Photo. focallengthinfilm-Eigenschaft.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: System. Photo. focallengthinfilm-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485702"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>System. Photo. focallengthinfilm-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. focallengthinfilm](../properties/props-system-photo-focallengthinfilm.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ focallengthinfilm

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



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                            |
|-------|---------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /IFD/EXIF/{ushort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. focallengthinfilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
