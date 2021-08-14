---
description: Die Richtlinie für Fotometadaten für die System.Photo.FNumber-Eigenschaft.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: System.Photo.FNumber-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90ad29c4dc6211f66df8621cfb589c2947f08dbb9f0b4f0fe03196c23909a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204810"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>System.Photo.FNumber-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.FNumber-Eigenschaft.](../properties/props-system-photo-fnumber.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FNumber

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert wird von System.Photo.FNumberNumerator und System.Photo.FNumberDenominator generiert. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             | 
 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=33437} |
| 2     | /xmp/exif:fnumber             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=33437} |
| 2     | /ifd/xmp/exif:fnumber    |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.FNumber](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
