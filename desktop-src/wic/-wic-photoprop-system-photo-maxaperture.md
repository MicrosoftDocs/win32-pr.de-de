---
description: Die Richtlinie für Fotometadaten für die System.Photo.MaxAperture-Eigenschaft.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: System.Photo.MaxAperture-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d692c12b9a5df584331a9a5ff4a82707d8549ab7891e1d9162eef318a77fe4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204712"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>System.Photo.MaxAperture-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.MaxAperture-Eigenschaft.](../properties/props-system-photo-maxaperture.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MaxAperture

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.Photo.MaxApertureNumerator und System.Photo.MaxApertureDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37381} |
| 2     | /xmp/exif:maxaperturevalue    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=37381}       |
| 2     | /ifd/xmp/exif:maxaperturevalue |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
