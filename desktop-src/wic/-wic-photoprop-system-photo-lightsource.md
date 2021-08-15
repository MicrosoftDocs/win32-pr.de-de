---
description: Die Fotometadatenrichtlinie für die System.Photo.LightSource-Eigenschaft.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: System.Photo.LightSource-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195d165a6a929c8e0b4bf2dd165a5f22068a8b75e8ea4dfcddb5b8979900b035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204722"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>System.Photo.LightSource-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.LightSource-Eigenschaft.](../properties/props-system-photo-lightsource.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LightSource

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI4

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                          | Datenträgerformat |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37384} | ushort      |
| 2     | /xmp/exif:LightSource         | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37384} |
| 2     | /xmp/exif:lightsource         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /ifd/exif/{ushort=37384}  | ushort      |
| 2     | /ifd/xmp/exif:LightSource | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/exif/{ushort=37384}  |
| 2     | /ifd/xmp/exif:lightsource |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
