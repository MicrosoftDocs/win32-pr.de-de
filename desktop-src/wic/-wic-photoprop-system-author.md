---
description: Die fotometadatenrichtlinie für die System. Author-Eigenschaft.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: System. Author-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369026"
---
# <a name="systemauthor-photo-metadata-policy"></a>System. Author-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Author](../properties/props-system-author.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Autor

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Der VT- \_ Vektor \| VT \_ LPWSTR wird bevorzugt, aber VT \_ LPWSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format    |
|-------|----------------------------------|----------------|
| 1     | /App1/IFD/{ushort = 315}           | ascii          |
| 2     | /app13/irb/8bimiptc/iptc/by-line |                |
| 3     | /XMP/ <xmpseq> DC: Creator    | Unicode        |
| 4     | /app13/irb/8bimiptc/iptc/by-line |                |
| 5     | /App1/IFD/{ushort = 40093}         | Unicode- \_ Bytes |
| 6     | /XMP/TIFF: Künstlerin                 | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                             | Datenträger Format    |
|-------|----------------------------------|----------------|
| 1     | /XMP/ <xmpseq> DC: Creator    | Unicode        |
| 2     | /XMP/TIFF: Künstlerin                 | Unicode        |
| 3     | /app13/irb/8bimiptc/iptc/by-line |                |
| 4     | /App1/IFD/{ushort = 315}           | ascii          |
| 5     | /App1/IFD/{ushort = 40093}         | Unicode- \_ Bytes |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /XMP/DC: Ersteller                  |
| 2     | /XMP/TIFF: Künstlerin                 |
| 3     | /app13/irb/8bimiptc/iptc/by-line |
| 4     | /App1/IFD/{ushort = 315}           |
| 5     | /App1/IFD/{ushort = 40093}         |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                              | Datenträger Format    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/{ushort = 315}                 | ascii          |
| 2     | /ifd/iptc/by-line                 |                |
| 3     | /IFD/XMP/ <xmpseq> DC: Creator | Unicode        |
| 4     | /ifd/iptc/by-line                 |                |
| 5     | /IFD/{ushort = 40093}               | Unicode- \_ Bytes |
| 6     | /ifd/irb/8bimiptc/iptc/by-line    |                |
| 7     | /IFD/XMP/TIFF: Künstlerin              | Unicode        |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                              | Datenträger Format    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpseq> DC: Creator | Unicode        |
| 2     | /IFD/XMP/TIFF: Künstlerin              | Unicode        |
| 3     | /ifd/iptc/by-line                 |                |
| 4     | /IFD/{ushort = 315}                 | ASCII- \_ Vektor  |
| 5     | /IFD/{ushort = 40093}               | Unicode- \_ Bytes |
| 6     | /ifd/iptc/by-line                 |                |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/XMP/DC: Ersteller            |
| 2     | /IFD/XMP/TIFF: Künstlerin           |
| 3     | /ifd/iptc/by-line              |
| 4     | /ifd/irb/8bimiptc/iptc/by-line |
| 5     | /IFD/{ushort = 315}              |
| 6     | /IFD/{ushort = 40093}            |



 

### <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Author](../properties/props-system-author.md)
</dt> </dl>

 

 
