---
description: Die fotometadatenrichtlinie für die System. Photo. CameraModel-Eigenschaft.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: System. Photo. CameraModel Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868004"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a>System. Photo. CameraModel Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ CameraModel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: Modell        | Unicode     |
| 3     | /XMP/TIFF: Modell        | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 272} | ascii       |
| 2     | /XMP/TIFF: Modell        | Unicode     |
| 3     | /XMP/TIFF: Modell        | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 272} |
| 2     | /XMP/TIFF: Modell        |
| 3     | /XMP/TIFF: Modell        |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                | Datenträger Format |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: Modell | Unicode     |
| 3     | /IFD/XMP/TIFF: Modell | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                | Datenträger Format |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 272}   | ascii       |
| 2     | /IFD/XMP/TIFF: Modell | Unicode     |
| 3     | /IFD/XMP/TIFF: Modell | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                |
|-------|---------------------|
| 1     | /IFD/{ushort = 272}   |
| 2     | /IFD/XMP/TIFF: Modell |
| 3     | /IFD/XMP/TIFF: Modell |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
