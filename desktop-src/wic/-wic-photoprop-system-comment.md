---
description: Die Richtlinie für Fotometadaten für die System.Comment-Eigenschaft.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: System.Comment Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa1a62fd5afa131a714c365ed2fda2c307bc955
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883904"
---
# <a name="systemcomment-photo-metadata-policy"></a>System.Comment Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.Comment-Eigenschaft.](../properties/props-system-comment.md)

### <a name="pkey"></a>PKEY

\_PKEY-Kommentar

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ LPWSTR oder VT \_ LPSTR

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                | Datenträgerformat    |
|-------|-------------------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092}            | \_Unicode-Bytes |
| 2     | /app1/ifd/{ushort=37510}            | Unicode        |
| 3     | /xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                     | Datenträgerformat    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40092} | \_Unicode-Bytes |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                          |
|-------|-------------------------------|
| 1     | /app1/ifd/{ushort=40092}      |
| 2     | /app1/ifd/exif/{ushort=37510} |
| 3     | /xmp/exif:UserComment         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                    | Datenträgerformat    |
|-------|-----------------------------------------|----------------|
| 1     | /ifd/{ushort=40092}                     | \_Unicode-Bytes |
| 2     | /ifd/{ushort=37510}                     | Unicode        |
| 3     | /ifd/xmp/ &lt; xmpalt &gt; exif:UserComment | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                | Datenträgerformat    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40092} | \_Unicode-Bytes |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=40092}       |
| 2     | /ifd/{ushort=37510}       |
| 3     | /ifd/xmp/exif:UserComment |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Comment](../properties/props-system-comment.md)
</dt> </dl>

 

 
