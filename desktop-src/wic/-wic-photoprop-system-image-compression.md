---
description: Die fotometadatenrichtlinie für die System. Image. Compression-Eigenschaft.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: System. Image. Compression-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362265"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>System. Image. Compression-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. Compression](../properties/props-system-image-compression.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Bild \_ Komprimierung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: Komprimierung  | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: Komprimierung  | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 259} |
| 2     | /XMP/TIFF: Komprimierung  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: Komprimierung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: Komprimierung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 259}         |
| 2     | /IFD/XMP/TIFF: Komprimierung |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
