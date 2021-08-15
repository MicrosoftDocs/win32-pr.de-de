---
description: Die Fotometadatenrichtlinie für die System.Photo.CameraManufacturer-Eigenschaft.
ms.assetid: 6710161c-4835-4385-9d4c-566acc000925
title: System.Photo.CameraManufacturer-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37744420babedf6b398cdf3ab9007c3895c09d33b9254221b5ba4760ab917a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087086"
---
# <a name="systemphotocameramanufacturer-photo-metadata-policy"></a>System.Photo.CameraManufacturer-Richtlinie für Fotometadaten

Die Fotometadatenrichtlinie für die [System.Photo.CameraManufacturer-Eigenschaft.](../properties/props-system-photo-cameramanufacturer.md)

### <a name="pkey"></a>PKEY

\_ \_ PKEY-FotokameraManufacturer

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | Unicode     |
| 3     | /xmp/tiff:make         | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=271} | ascii       |
| 2     | /xmp/tiff:Make         | Unicode     |
| 3     | /xmp/tiff:make         | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=271} |
| 2     | /xmp/tiff:Make         |
| 3     | /xmp/tiff:make         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad               | Datenträgerformat |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | Unicode     |
| 3     | /ifd/xmp/tiff:make | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad               | Datenträgerformat |
|-------|--------------------|-------------|
| 1     | /ifd/{ushort=271}  | ascii       |
| 2     | /ifd/xmp/tiff:Make | Unicode     |
| 3     | /ifd/xmp/tiff:make | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad               |
|-------|--------------------|
| 1     | /ifd/{ushort=271}  |
| 2     | /ifd/xmp/tiff:Make |
| 3     | /ifd/xmp/tiff:make |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.CameraManufacturer](../properties/props-system-photo-cameramanufacturer.md)
</dt> </dl>

 

 
