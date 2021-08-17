---
description: Die Richtlinie für Fotometadaten für die System.Photo.Orientation-Eigenschaft.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Richtlinie für System.Photo.Orientation-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f9496942e6be971e0e047596125669fc9112cf82bce6eb02ec7e1cdbddc4de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087066"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Richtlinie für System.Photo.Orientation-Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.Orientation-Eigenschaft.](../properties/props-system-photo-meteringmode.md)

### <a name="pkey"></a>PKEY

\_ \_ PKEY-Fotoausrichtung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                   | Datenträgerformat |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=274} | ushort      |
| 2     | /xmp/tiff:Orientation  | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=274} |
| 2     | /xmp/tiff:orientation  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=274}         | ushort      |
| 2     | /ifd/xmp/tiff:Orientation | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=274}         |
| 2     | /ifd/xmp/tiff:orientation |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
