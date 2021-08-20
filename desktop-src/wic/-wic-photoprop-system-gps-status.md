---
description: Die Fotometadatenrichtlinie für die System.GPS.Status-Eigenschaft.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: System.GPS.Status Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710515"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>System.GPS.Status Photo Metadata Policy

Die Fotometadatenrichtlinie für die [System.GPS.Status-Eigenschaft.](../properties/props-system-gps-status.md)

### <a name="pkey"></a>PKEY

PKEY \_ \_ GPS-Status

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                    | Datenträgerformat |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                    | Datenträgerformat |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                    |
|-------|-------------------------|
| 1     | /ifd/gps/{ushort=9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.Status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
