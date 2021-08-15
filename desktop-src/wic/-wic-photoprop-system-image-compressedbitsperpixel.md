---
description: Die Richtlinie für Fotometadaten für die System.Image.CompressedBitsPerPixel-Eigenschaft.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: System.Image.CompressedBitsPerPixel-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a18cc76e22c5c409e19e08fc5a2e667ad374348bc753ffa85cd09003a8bdaf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032709"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>System.Image.CompressedBitsPerPixel-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Image.CompressedBitsPerPixel-Eigenschaft.](../properties/props-system-image-compressedbitsperpixel.md)

### <a name="pkey"></a>PKEY

\_PKEY-Image \_ CompressedBitsPerPixel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.Image.CompressedBitsPerPixelNumerator und System.Image.CompressedBitsPerPixelDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                             | Datenträgerformat |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |             |
| 2     | /xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37122}    |
| 2     | /xmp/exif:compressedbitsperpixel |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                 | Datenträgerformat |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37122}             |             |
| 2     | /ifd/xmp/exif:CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37122}             |
| 2     | /ifd/xmp/exif:compressedbitsperpixel |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Image.CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
