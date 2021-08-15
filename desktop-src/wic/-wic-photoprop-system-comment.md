---
description: Die Fotometadatenrichtlinie für die System.Comment-Eigenschaft.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Richtlinie für System.Comment-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45b3511e0a459a2b652b29828060be6f0a92a36639aef63d4fa087e54ec9d80b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205629"
---
# <a name="systemcomment-photo-metadata-policy"></a>Richtlinie für System.Comment-Fotometadaten

Die Fotometadatenrichtlinie für die [System.Comment-Eigenschaft.](../properties/props-system-comment.md)

### <a name="pkey"></a>PKEY

\_PKEY-Kommentar

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

VT \_ LPWSTR oder VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                | Datenträgerformat    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092}            | \_Unicodebytes |
| 2     | /app1/ifd/{ushort=37510}            | Unicode        |
| 3     | /xmp/ <xmpalt> exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                     | Datenträgerformat    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092} | \_Unicodebytes |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/{ushort=40092}      |
| 2     | /app1/ifd/exif/{ushort=37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                    | Datenträgerformat    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40092}                     | \_Unicodebytes |
| 2     | /ifd/{ushort=37510}                     | Unicode        |
| 3     | /ifd/xmp/ <xmpalt> exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                | Datenträgerformat    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40092} | \_Unicodebytes |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=40092}       |
| 2     | /ifd/{ushort=37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
