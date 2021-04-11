---
description: Die fotometadatenrichtlinie für die System. Keywords-Eigenschaft.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: System. Keywords Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217830"
---
# <a name="systemkeywords-photo-metadata-policy"></a>System. Keywords Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Keywords](../properties/props-system-keywords.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Schlüsselwörter

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ Vector \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Der VT- \_ Vektor \| VT \_ LPWSTR wird bevorzugt. Ein VT \_ LPWSTR, das eine durch Semikolons getrennte Zeichenfolge enthält, wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas werden zusammengeführt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                              | Datenträger Format    |
|-------|-----------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: Subject     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /App1/IFD/{ushort = 18247}          | Unicode- \_ Bytes |
| 4     | /App1/IFD/{ushort = 40094}          | Unicode- \_ Bytes |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                              | Datenträger Format    |
|-------|---------------------------------------------------|----------------|
| 1     | /XMP/ <xmpbag> DC: Subject                     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /App1/IFD/{ushort = 18247}                          | Unicode- \_ Bytes |
| 4     | /App1/IFD/{ushort = 40094}                          | Unicode- \_ Bytes |
| 5     | /XMP/ <xmpbag> microsoftphoto: lastkeywordxmp  | Unicode        |
| 6     | /XMP/ <xmpbag> microsoftphoto: lastkeywordiptc | Unicode        |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                              |
|-------|---------------------------------------------------|
| 1     | /XMP/DC: Betreff                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /App1/IFD/{ushort = 18247}                          |
| 4     | /App1/IFD/{ushort = 40094}                          |
| 5     | /XMP/ <xmpbag> microsoftphoto: lastkeywordxmp  |
| 6     | /XMP/ <xmpbag> microsoftphoto: lastkeywordiptc |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                              | Datenträger Format    |
|-------|-----------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: Subject | Unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /IFD/{ushort = 18247}               | Unicode- \_ Bytes |
| 4     | /IFD/{ushort = 40094}               | Unicode- \_ Bytes |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                                             | Datenträger Format    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /IFD/XMP/ <xmpbag> DC: Subject                                | Unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /IFD/{ushort = 18247}                                              | Unicode- \_ Bytes |
| 5     | /IFD/{ushort = 40094}                                              | Unicode- \_ Bytes |
| 6     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp             | Unicode        |
| 7     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc            | Unicode        |
| 8     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc \_ TIFF- \_ UNB | Unicode        |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                                             |
|-------|------------------------------------------------------------------|
| 1     | /IFD/XMP/DC: Betreff                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /IFD/{ushort = 18247}                                              |
| 5     | /IFD/{ushort = 40094}                                              |
| 6     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordxmp             |
| 7     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc            |
| 8     | /IFD/XMP/ <xmpbag> microsoftphoto: lastkeywordiptc \_ TIFF- \_ UNB |



 

### <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
