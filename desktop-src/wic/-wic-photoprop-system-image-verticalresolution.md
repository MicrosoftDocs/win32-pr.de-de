---
description: Die Richtlinie für Fotometadaten für die System.Image.VerticalResolution-Eigenschaft.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: System.Image.VerticalResolution-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9962a00be34d227756d295e992174d6e80b6d058fc32af29ad9cde58a04ed07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710283"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>System.Image.VerticalResolution-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Image.VerticalResolution-Eigenschaft.](../properties/props-system-image-verticalresolution.md)

### <a name="pkey"></a>PKEY

\_PKEY-Image \_ VerticalResolution

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja.

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird vom System generiert und kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=283} |             |
| 2     | /xmp/tiff:YResolution  |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /app1/ifd/exif/{ushort=283} |
| 2     | /xmp/tiff:yresolution       |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=283}    |             |
| 2     | /ifd/xmp/tiff:YResolution |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=283}    |
| 2     | /ifd/xmp/tiff:yresolution |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Image.VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
