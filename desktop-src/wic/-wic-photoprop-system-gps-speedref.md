---
description: Die fotometadatenrichtlinie für die System. GPS. speedref-Eigenschaft.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: System. GPS. speedref-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363636"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>System. GPS. speedref-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. speedref](../properties/props-system-gps-speedref.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ speedref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /XMP/EXIF: gpsspeedref     | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /XMP/EXIF: gpsspeedref     | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 12} |             |
| 2     | /XMP/EXIF: gpsspeedref     |             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      |         |
|-------|---------------------------|---------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii   |
| 2     | /IFD/XMP/EXIF: gpsspeedref | Unicode |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii       |
| 2     | /IFD/XMP/EXIF: gpsspeedref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 12}      |
| 2     | /IFD/XMP/EXIF: gpsspeedref |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. speedref](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
