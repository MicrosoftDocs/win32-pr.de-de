---
description: Die fotometadatenrichtlinie für die System. Copyright-Eigenschaft.
ms.assetid: 84d2f55b-5ca4-4912-b038-c18a72e6fc34
title: System. Copyright Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc65024458d88088e3c0cbeccc3bc9ea0211910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364230"
---
# <a name="systemcopyright-photo-metadata-policy"></a>System. Copyright Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Copyright](../properties/props-system-copyright.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Copyright

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

String

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                      | Datenträger Format |
|-------|-------------------------------------------|-------------|
|       | /App1/IFD/{ushort = 33432}                  | ascii       |
|       | /app13/IRB/8bimiptc/IPTC/Copyright Hinweis |             |
|       | /XMP/ <xmpalt> DC: Rechte              | Unicode     |
|       | /XMP/DC: Rechte                            | Unicode     |
|       | /app13/IRB/8bimiptc/IPTC/Copyright Hinweis |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                      | Datenträger Format |
|-------|-------------------------------------------|-------------|
|       | /XMP/DC: Rechte                            | Unicode     |
|       | /XMP/ <xmpalt> DC: Rechte              | Unicode     |
|       | /app13/IRB/8bimiptc/IPTC/Copyright Hinweis |             |
|       | /App1/IFD/{ushort = 33432}                  | ascii       |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                      |
|-------|-------------------------------------------|
|       | /XMP/DC: Rechte                            |
|       | /app13/IRB/8bimiptc/IPTC/Copyright Hinweis |
|       | /App1/IFD/{ushort = 33432}                  |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
|       | /IFD/{ushort = 33432}                     | ascii       |
|       | /IFD/IPTC/Copyright Hinweis              |             |
|       | /IFD/XMP/ <xmpalt> DC: Rechte        | Unicode     |
|       | /IFD/XMP/DC: Rechte                      | Unicode     |
|       | /IFD/IPTC/Copyright Hinweis              |             |
|       | /IFD/IRB/8bimiptc/IPTC/Copyright Hinweis |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
|       | /IFD/XMP/DC: Rechte                      | Unicode     |
|       | /IFD/XMP/ <xmpalt> DC: Rechte        | Unicode     |
|       | /IFD/IPTC/Copyright Hinweis              |             |
|       | /IFD/IRB/8bimiptc/IPTC/Copyright Hinweis |             |
|       | /IFD/{ushort = 33432}                     | ascii       |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
|       | /IFD/XMP/DC: Rechte                      |
|       | /IFD/IPTC/Copyright Hinweis              |
|       | /IFD/IRB/8bimiptc/IPTC/Copyright Hinweis |
|       | /IFD/{ushort = 33432}                     |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Copyright](../properties/props-system-copyright.md)
</dt> </dl>

 

 
