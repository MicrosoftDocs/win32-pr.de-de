---
description: Die Fotometadatenrichtlinie für die System.Photo.DigitalZoom-Eigenschaft.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: System.Photo.DigitalZoom Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19dfaf2838c8f321b1406d951fcc335076bcdfc00e3a17de0954f1a62022570e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205376"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>System.Photo.DigitalZoom Photo Metadata Policy

Die Fotometadatenrichtlinie für die [System.Photo.DigitalZoom-Eigenschaft.](../properties/props-system-photo-digitalzoom.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ DigitalZoom

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird aus System.Photo.DigitalZoomNumerator und System.Photo.DigitalZoomDenominator generiert. Er kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41988} |             |
| 2     | /xmp/exif:DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41988} |
| 2     | /xmp/exif:digitalzoomratio    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=41988}       |             |
| 2     | /ifd/xmp/exif:DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=41988}       |
| 2     | /ifd/xmp/exif:digitalzoomratio |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
