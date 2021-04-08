---
description: Die fotometadatenrichtlinie für die System. GPS. messremode-Eigenschaft.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: System. GPS. messremode Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959883"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>System. GPS. messremode Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. GPS. messremode](../properties/props-system-gps-measuremode.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ messremode

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
| 1     | /App1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /XMP/EXIF: gpsmessremode  | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 10} | ascii       |
| 2     | /XMP/EXIF: gpsmessremode  | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 10} |
| 2     | /XMP/EXIF: gpsmessremode  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 10}         | ascii       |
| 2     | /IFD/XMP/EXIF: gpsmessremode | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 10}         | ascii       |
| 2     | /IFD/XMP/EXIF: gpsmessremode | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /IFD/GPS/{ushort = 10}         |
| 2     | /IFD/XMP/EXIF: gpsmessremode |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. messremode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
