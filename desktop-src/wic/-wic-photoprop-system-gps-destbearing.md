---
description: Die fotometadatenrichtlinie für die System. GPS. destbearing-Eigenschaft.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: System. GPS. destbearing-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348588"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a>System. GPS. destbearing-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destbearing](../properties/props-system-gps-destbearing.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ destbearing

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert kann durch Schreiben in System. GPS. destbearingnumerator und System. GPS. destbearingnenner geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 24} |             |
| 2     | /XMP/EXIF: gpsdestbearing  |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 24} |             |
| 2     | /XMP/EXIF: gpsdestbearing  |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 24} |             |
| 2     | /XMP/EXIF: gpsdestbearing  |             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 24}         |             |
| 2     | /IFD/XMP/EXIF: gpsdestbearing |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 24}         |             |
| 2     | /IFD/XMP/EXIF: gpsdestbearing |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{ushort = 24}         |
| 2     | /IFD/XMP/EXIF: gpsdestbearing |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destbearing](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
