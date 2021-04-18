---
description: Die fotometadatenrichtlinie für die System. GPS. Status-Eigenschaft.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: System. GPS. Status Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358936"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>System. GPS. Status Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Status](../properties/props-system-gps-status.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Status

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



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /XMP/EXIF: gpsstatus      | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 9} | ascii       |
| 2     | /XMP/EXIF: gpsstatus      | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/GPS/{ushort = 9} |
| 2     | /XMP/EXIF: gpsstatus      |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                    | Datenträger Format |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 9}     | ascii       |
| 2     | /IFD/XMP/EXIF: gpsstatus | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                    | Datenträger Format |
|-------|-------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 9}     | ascii       |
| 2     | /IFD/XMP/EXIF: gpsstatus | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                    |
|-------|-------------------------|
| 1     | /IFD/GPS/{ushort = 9}     |
| 2     | /IFD/XMP/EXIF: gpsstatus |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
