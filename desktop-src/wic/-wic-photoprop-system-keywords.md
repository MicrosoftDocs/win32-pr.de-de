---
description: Die Richtlinie für Fotometadaten für die System.Keywords-Eigenschaft.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: System.Keywords-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa5387bfb8cca7fffe83f7615a979d8e23ae890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886651"
---
# <a name="systemkeywords-photo-metadata-policy"></a>System.Keywords-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Keywords-Eigenschaft.](../properties/props-system-keywords.md)

### <a name="pkey"></a>PKEY

\_PKEY-Schlüsselwörter

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ VECTOR \| VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

VT \_ VECTOR \| VT \_ LPWSTR wird bevorzugt. Ein VT \_ LPWSTR mit einer durch Semikolons getrennten Zeichenfolge wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden zusammengeführt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                              | Datenträgerformat    |
|-------|-----------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords |                |
| 3     | /app1/ifd/{ushort=18247}          | \_Unicode-Bytes |
| 4     | /app1/ifd/{ushort=40094}          | \_Unicode-Bytes |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                              | Datenträgerformat    |
|-------|---------------------------------------------------|----------------|
| 1     | /xmp/ &lt; xmpbag &gt; dc:subject                     | Unicode        |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |                |
| 3     | /app1/ifd/{ushort=18247}                          | \_Unicode-Bytes |
| 4     | /app1/ifd/{ushort=40094}                          | \_Unicode-Bytes |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  | Unicode        |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC | Unicode        |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                              |
|-------|---------------------------------------------------|
| 1     | /xmp/dc:subject                                   |
| 2     | /app13/irb/8bimiptc/iptc/keywords                 |
| 3     | /app1/ifd/{ushort=18247}                          |
| 4     | /app1/ifd/{ushort=40094}                          |
| 5     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP  |
| 6     | /xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                              | Datenträgerformat    |
|-------|-----------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject | Unicode        |
| 2     | /ifd/iptc/keywords                |                |
| 3     | /ifd/{ushort=18247}               | \_Unicode-Bytes |
| 4     | /ifd/{ushort=40094}               | \_Unicode-Bytes |
| 5     | /ifd/irb/8bimiptc/iptc/keywords   |                |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                                             | Datenträgerformat    |
|-------|------------------------------------------------------------------|----------------|
| 1     | /ifd/xmp/ &lt; xmpbag &gt; dc:subject                                | Unicode        |
| 2     | /ifd/iptc/keywords                                               |                |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |                |
| 4     | /ifd/{ushort=18247}                                              | \_Unicode-Bytes |
| 5     | /ifd/{ushort=40094}                                              | \_Unicode-Bytes |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             | Unicode        |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            | Unicode        |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB | Unicode        |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                                             |
|-------|------------------------------------------------------------------|
| 1     | /ifd/xmp/dc:subject                                              |
| 2     | /ifd/iptc/keywords                                               |
| 3     | /ifd/irb/8bimiptc/iptc/keywords                                  |
| 4     | /ifd/{ushort=18247}                                              |
| 5     | /ifd/{ushort=40094}                                              |
| 6     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordXMP             |
| 7     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC            |
| 8     | /ifd/xmp/ &lt; xmpbag &gt; MicrosoftPhoto:LastKeywordIPTC \_ TIFF \_ IRB |



 

### <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Keywords](../properties/props-system-keywords.md)
</dt> </dl>

 

 
