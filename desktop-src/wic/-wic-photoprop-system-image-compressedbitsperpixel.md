---
description: Die fotometadatenrichtlinie für die System. Image. CompressedBitsPerPixel-Eigenschaft.
ms.assetid: e97a5c68-6d4a-44af-8096-22680f8b16b8
title: System. Image. CompressedBitsPerPixel-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b45b3b1e8b29cdf992cd3b451a2e8a43947139a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356196"
---
# <a name="systemimagecompressedbitsperpixel-photo-metadata-policy"></a>System. Image. CompressedBitsPerPixel-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Image \_ CompressedBitsPerPixel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird aus System. Image. compressedbitsperpixelnumerator und System. Image. compressedbitsperpixelnenner generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37122}    |             |
| 2     | /XMP/EXIF: CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37122}    |
| 2     | /XMP/EXIF: CompressedBitsPerPixel |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                 | Datenträger Format |
|-------|--------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37122}             |             |
| 2     | /IFD/XMP/EXIF: CompressedBitsPerPixel |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                 |
|-------|--------------------------------------|
| 1     | /IFD/EXIF/{ushort = 37122}             |
| 2     | /IFD/XMP/EXIF: CompressedBitsPerPixel |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. CompressedBitsPerPixel](../properties/props-system-image-compressedbitsperpixel.md)
</dt> </dl>

 

 
