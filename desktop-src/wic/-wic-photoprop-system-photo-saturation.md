---
description: Die Richtlinie für Fotometadaten für die System.Photo.Saturation-Eigenschaft.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: System.Photo.Saturation-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087013"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>System.Photo.Saturation-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.Saturation-Eigenschaft.](../properties/props-system-photo-saturation.md)

### <a name="pkey"></a>PKEY

\_PKEY-Fotosättigung \_

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI4

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Sättigung          | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Sättigung          | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41993} |
| 2     | /xmp/exif:Sättigung          |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Sättigung | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Sättigung | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41993} |
| 2     | /ifd/xmp/exif:Sättigung |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Saturation](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
