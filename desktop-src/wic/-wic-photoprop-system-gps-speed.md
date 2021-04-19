---
description: Die fotometadatenrichtlinie für die System. GPS. Speed-Eigenschaft.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: System. GPS. Speed Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363290"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>System. GPS. Speed Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. GPS. Speed](../properties/props-system-gps-speed.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ -GPS- \_ Geschwindigkeit

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. GPS. speednumerator" und "System. GPS. speednenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |             |
| 2     | /XMP/EXIF: gpsspeed        |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |             |
| 2     | /XMP/EXIF: gpsspeed        |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 13} |
| 2     | /XMP/EXIF: gpsspeed        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /IFD/XMP/EXIF: gpsspeed |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /IFD/XMP/EXIF: gpsspeed |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /IFD/GPS/{ushort = 13}   |
| 2     | /IFD/XMP/EXIF: gpsspeed |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
