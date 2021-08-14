---
description: Die Richtlinie für Fotometadaten für die System.GPS.Latitude-Eigenschaft.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: System.GPS.Latitude Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41dd1eb0ee21ab02eeb8c83d5ea84f28c07c2811929f2b8c973cace4a4a06fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710624"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a>System.GPS.Latitude Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.GPS.Latitude-Eigenschaft.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ Latitude

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert kann durch Schreiben in System.GPS.LatitudeNumerator und System.GPS.LatitudeDenominator geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSL übertragen    |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=2} |             |
| 2     | /xmp/exif:GPSL übertragen    |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=2} |
| 2     | /xmp/exif:gpsl veralten    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSL zu |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/gps/{ushort=2}       |             |
| 2     | /ifd/xmp/exif:GPSL zu |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/gps/{ushort=2}       |
| 2     | /ifd/xmp/exif:gpsl zu |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Latitude](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
