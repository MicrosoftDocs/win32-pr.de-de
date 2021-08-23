---
description: Die Richtlinie für Fotometadaten für die System.Author-Eigenschaft.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Richtlinie für System.Author-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b898f450fe1d370f94a9be2922eb650db47ac8c2e414c27d9eede23f0dada276
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088002"
---
# <a name="systemauthor-photo-metadata-policy"></a>Richtlinie für System.Author-Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Author-Eigenschaft.](../properties/props-system-author.md)

### <a name="pkey"></a>PKEY

PKEY \_ Author

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ VECTOR \| VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPWSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                             | Datenträgerformat    |
|-------|----------------------------------|----------------|
| 1     | /app1/ifd/{ushort=315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /xmp/ <xmpseq> dc:creator    | Unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /app1/ifd/{ushort=40093}         | \_Unicode-Bytes |
| 6     | /xmp/tiff:interpret                 | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                             | Datenträgerformat    |
|-------|----------------------------------|----------------|
| 1     | /xmp/ <xmpseq> dc:creator    | Unicode        |
| 2     | /xmp/tiff:interpret                 | Unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /app1/ifd/{ushort=315}           | ascii          |
| 5     | /app1/ifd/{ushort=40093}         | \_Unicode-Bytes |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /xmp/dc:creator                  |
| 2     | /xmp/tiff:interpret                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /app1/ifd/{ushort=315}           |
| 5     | /app1/ifd/{ushort=40093}         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                              | Datenträgerformat    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/{ushort=315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /ifd/xmp/ <xmpseq> dc:creator | Unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /ifd/{ushort=40093}               | \_Unicode-Bytes |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /ifd/xmp/tiff:interpret              | Unicode        |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                              | Datenträgerformat    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ <xmpseq> dc:creator | Unicode        |
| 2     | /ifd/xmp/tiff:interpret              | Unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /ifd/{ushort=315}                 | \_ASCII-Vektor  |
| 5     | /ifd/{ushort=40093}               | \_Unicode-Bytes |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/xmp/dc:creator            |
| 2     | /ifd/xmp/tiff:interpret           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /ifd/{ushort=315}              |
| 6     | /ifd/{ushort=40093}            |



 

### <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
