---
description: Die Richtlinie für Fotometadaten für die System.Photo.Brightness-Eigenschaft.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: System.Photo.Brightness Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78549d86d50f9b48359932698b02c827bd454a439476f2dc82627e4aab21d25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882060"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>System.Photo.Brightness Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.Photo.Brightness-Eigenschaft.](../properties/props-system-photo-aperture.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Brightness

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.Photo.ApertureNumerator und System.Photo.ApertureDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37379} |             |
| 2     | /xmp/exif:BrightnessValue     |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37379} |
| 2     | /xmp/exif:brightnessvalue     |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37379}      |             |
| 2     | /ifd/xmp/exif:BrightnessValue |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /ifd/exif/{ushort=37379}      |
| 2     | /ifd/xmp/exif:brightnessvalue |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Brightness](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
