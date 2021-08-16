---
description: Die Fotometadatenrichtlinie für die System.Photo.PhotometricInterpretation-Eigenschaft.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Richtlinie für System.Photo.PhotometricInterpretation-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5479c747e2a1cc60a1867a7dc5906e5c4710abf9da33b5328980e0188403ecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204684"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>Richtlinie für System.Photo.PhotometricInterpretation-Fotometadaten

Die Fotometadatenrichtlinie für die [System.Photo.PhotometricInterpretation-Eigenschaft.](../properties/props-system-photo-photometricinterpretation.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PhotometricInterpretation

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                | Datenträgerformat |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                | Datenträgerformat |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort=262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
