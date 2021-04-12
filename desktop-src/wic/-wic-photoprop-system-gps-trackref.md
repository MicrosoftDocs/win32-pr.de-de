---
description: Die fotometadatenrichtlinie für die System. GPS. trackref-Eigenschaft.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: System. GPS. trackref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218569"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a>System. GPS. trackref-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. trackref](../properties/props-system-gps-trackref.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ trackref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /XMP/EXIF: gpstrackref     | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 14} | ascii       |
| 2     | /XMP/EXIF: gpstrackref     | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 14} |
| 2     | /XMP/EXIF: gpstrackref     |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 14}      | ascii       |
| 2     | /IFD/XMP/EXIF: gpstrackref | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 14}      | ascii       |
| 2     | /IFD/XMP/EXIF: gpstrackref | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 14}      |
| 2     | /IFD/XMP/EXIF: gpstrackref |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. trackref](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
