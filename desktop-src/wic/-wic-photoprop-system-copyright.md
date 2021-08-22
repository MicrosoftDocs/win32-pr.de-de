---
description: Die Richtlinie für Fotometadaten für die System.Copyright-Eigenschaft.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: System.Copyright Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00b57bc3523feaa29da9008340bd34c32401879a8fc4e872082bbdcddd1fdf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710813"
---
# <a name="systemcopyright-photo-metadata-policy"></a>System.Copyright Photo Metadata Policy

Die Richtlinie für Fotometadaten für die [System.Copyright-Eigenschaft.](../properties/props-system-copyright.md)

### <a name="pkey"></a>PKEY

PKEY \_ Copyright

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                      | Datenträgerformat |
|-------|-------------------------------------------|-------------|
|       | /app1/ifd/{ushort=33432}                  | ascii       |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /xmp/ <xmpalt> dc:rights              | Unicode     |
|       | /xmp/dc:rights                            | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                      | Datenträgerformat |
|-------|-------------------------------------------|-------------|
|       | /xmp/dc:rights                            | Unicode     |
|       | /xmp/ <xmpalt> dc:rights              | Unicode     |
|       | /app13/irb/8bimiptc/iptc/copyright notice |             |
|       | /app1/ifd/{ushort=33432}                  | ascii       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                      |
|-------|-------------------------------------------|
|       | /xmp/dc:rights                            |
|       | /app13/irb/8bimiptc/iptc/copyright notice |
|       | /app1/ifd/{ushort=33432}                  |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
|       | /ifd/{ushort=33432}                     | ascii       |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/xmp/ <xmpalt> dc:rights        | Unicode     |
|       | /ifd/xmp/dc:rights                      | Unicode     |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                    | Datenträgerformat |
|-------|-----------------------------------------|-------------|
|       | /ifd/xmp/dc:rights                      | Unicode     |
|       | /ifd/xmp/ <xmpalt> dc:rights        | Unicode     |
|       | /ifd/iptc/copyright notice              |             |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |             |
|       | /ifd/{ushort=33432}                     | ascii       |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
|       | /ifd/xmp/dc:rights                      |
|       | /ifd/iptc/copyright notice              |
|       | /ifd/irb/8bimiptc/iptc/copyright notice |
|       | /ifd/{ushort=33432}                     |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
