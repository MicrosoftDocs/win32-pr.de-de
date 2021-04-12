---
description: Die fotometadatenrichtlinie für die System. GPS. destbearingref-Eigenschaft.
ms.assetid: d1c8b3cc-ed52-43ca-a0ba-045a2c5fe274
title: System. GPS. destbearingref Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f00d3083459fe365fc54e81dc485ddd26887a46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216814"
---
# <a name="systemgpsdestbearingref-photo-metadata-policy"></a>System. GPS. destbearingref Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. GPS. destbearingref](../properties/props-system-gps-destbearingref.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ destbearingref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /XMP/EXIF: gpsdestbearingref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 23}   | ascii       |
| 2     | /XMP/EXIF: gpsdestbearingref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /App1/IFD/GPS/{ushort = 23}   |
| 2     | /XMP/EXIF: gpsdestbearingref |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 23}            | ascii       |
| 2     | /IFD/XMP/EXIF: gpsdestbearingref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                            | Datenträger Format |
|-------|---------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 23}            | ascii       |
| 2     | /IFD/XMP/EXIF: gpsdestbearingref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| order | path                            |
|-------|---------------------------------|
| 1     | /IFD/GPS/{ushort = 23}            |
| 2     | /IFD/XMP/EXIF: gpsdestbearingref |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destbearingref](../properties/props-system-gps-destbearingref.md)
</dt> </dl>

 

 
