---
description: Die Richtlinie für Fotometadaten für die System.Photo.CameraModel-Eigenschaft.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: System.Photo.CameraModel-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e205d4d886d050e45b958f2ba0f06c6411584c4a96a717378f243e5d1dd4fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882050"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>System.Photo.CameraModel-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.CameraModel-Eigenschaft.](../properties/props-system-photo-cameramodel.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ CameraModel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | Unicode     |
| 3     | /xmp/tiff:model        | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=272} | ascii       |
| 2     | /xmp/tiff:Model        | Unicode     |
| 3     | /xmp/tiff:model        | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=272} |
| 2     | /xmp/tiff:Model        |
| 3     | /xmp/tiff:model        |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                | Datenträgerformat |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | Unicode     |
| 3     | /ifd/xmp/tiff:model | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                | Datenträgerformat |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=272}   | ascii       |
| 2     | /ifd/xmp/tiff:Model | Unicode     |
| 3     | /ifd/xmp/tiff:model | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                |
|-------|---------------------|
| 1     | /ifd/{ushort=272}   |
| 2     | /ifd/xmp/tiff:Model |
| 3     | /ifd/xmp/tiff:model |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
