---
description: Die Richtlinie für Fotometadaten für die System.Photo.Speed-Eigenschaft.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: System.Photo.Speed-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad11550a19cd043fd5d182b2cf508aec3e26c64a0dc2ee1d1c24576ebf18f8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710099"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>System.Photo.Speed-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.Speed-Eigenschaft.](../properties/props-system-photo-shutterspeed.md)

### <a name="pkey"></a>PKEY

PKEY \_ \_ PhotoSpeed

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.Photo.SpeedNumerator und System.Photo.SpeedSpeedDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedSpeedValue   |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedSpeedValue   |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37377} |
| 2     | /xmp/exif:speedspeedvalue   |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                            | Datenträgerformat |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedSpeedValue |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                            | Datenträgerformat |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedSpeedValue |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort=37377}        |
| 2     | /ifd/xmp/exif:speedspeedvalue |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Speed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
