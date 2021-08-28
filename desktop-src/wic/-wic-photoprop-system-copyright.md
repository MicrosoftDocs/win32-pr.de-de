---
description: Die Fotometadatenrichtlinie für die System.Copyright-Eigenschaft.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: Richtlinie für System.Copyright-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3e17190205b3df5c2ede9b1a7db231d0fdbbe21
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882692"
---
# <a name="systemcopyright-photo-metadata-policy"></a>Richtlinie für System.Copyright-Fotometadaten

Die Fotometadatenrichtlinie für die [System.Copyright-Eigenschaft.](../properties/props-system-copyright.md)

### <a name="pkey"></a>PKEY

PKEY \_ Copyright

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                      | Datenträgerformat |
|-------|-------------------------------------------|-------------|
|       | /app1/ifd/{ushort=33432}                  | ascii       |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /xmp/ &lt; xmpalt &gt; dc:rights              | Unicode     |
|       | /xmp/dc:rights                            | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                      | Datenträgerformat |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc:rights                            | Unicode     |
|       | /xmp/ &lt; xmpalt &gt; dc:rights              | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /app1/ifd/{ushort=33432}                  | ascii       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                      |
|-------|-------------------------------------------|
|       | /xmp/dc:rights                            |
|       | /app13/irb/8bimiptc/iptc/copyright notice |
|       | /app1/ifd/{ushort=33432}                  |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Order | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
|       | /ifd/{ushort=33432}                     | ascii       |
|       | /ifd/iptc/Copyrighthinweis              |             |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc:rights        | Unicode     |
|       | /ifd/xmp/dc:rights                      | Unicode     |
|       | /ifd/iptc/Copyrighthinweis              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Schreibpfade



| Order | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc:rights                      | Unicode     |
|       | /ifd/xmp/ &lt; xmpalt &gt; dc:rights        | Unicode     |
|       | /ifd/iptc/Copyrighthinweis              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |
|       | /ifd/{ushort=33432}                     | ascii       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Order | Pfad                                    |
|-------|-----------------------------------------|
|       | /ifd/xmp/dc:rights                      |
|       | /ifd/iptc/Copyrighthinweis              |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |
|       | /ifd/{ushort=33432}                     |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
