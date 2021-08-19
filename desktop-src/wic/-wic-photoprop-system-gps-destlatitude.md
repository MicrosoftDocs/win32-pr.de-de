---
description: Die Richtlinie für Fotometadaten für die System.GPS.DestL persistent-Eigenschaft.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: System.GPS.DestL persistente Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57cce67b13235933816e244e17b5c761e1f0d230055eb82d683eb610579e5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882350"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>System.GPS.DestL persistente Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.DestL persistent-Eigenschaft.](../properties/props-system-gps-destlatitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestL veralten

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.GPS.DestLatorsNumerator und System.GPS.DestL persistentDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestL zu |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestL zu |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=20} |
| 2     | /xmp/exif:gpsdestl übertragen |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestL zu |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestL zu |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=20}          |
| 2     | /ifd/xmp/exif:gpsdestl geo |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DestL persistent](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
