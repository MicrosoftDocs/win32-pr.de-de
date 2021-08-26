---
description: Die Richtlinie für Fotometadaten für die System.GPS.Differential-Eigenschaft.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: System.GPS.Differential Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728df47fd8e6e9748b7208b79444ba8fa257fa49c92587df199441de941f4fdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931800"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>System.GPS.Differential Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.GPS.Differential-Eigenschaft.](../properties/props-system-gps-differential.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ Differential

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI2

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ UI1, VT \_ UI2 und VT \_ UI4 werden akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
