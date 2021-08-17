---
description: Die Richtlinie für Fotometadaten für die System.Photo.MeteringMode-Eigenschaft.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: System.Photo.MeteringMode-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424b14fa6216d5c88c350512d1583b311f92ef2f487e604760b1836b296d3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964779"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>System.Photo.MeteringMode-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.MeteringMode-Eigenschaft.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MeteringMode

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37383} | ushort      |
| 2     | /xmp/exif:MeteringMode        | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37383} |
| 2     | /xmp/exif:meteringmode        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /ifd/exif/{ushort=37383}   | ushort      |
| 2     | /ifd/xmp/exif:MeteringMode | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /ifd/exif/{ushort=37383}   |
| 2     | /ifd/xmp/exif:meteringmode |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.MeteringMode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
