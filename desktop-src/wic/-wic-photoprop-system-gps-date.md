---
description: Die fotometadatenrichtlinie für die System. GPS. Date-Eigenschaft.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: System. GPS. Date-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218033"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>System. GPS. Date-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. Date](../properties/props-system-gps-date.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ -GPS- \_ Datum

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /XMP/EXIF: gpstimestamp    | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /XMP/EXIF: gpstimestamp    | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /App1/IFD/GPS/{ushort = 29} |
| 2     | /XMP/EXIF: gpstimestamp    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /IFD/XMP/EXIF: gpstimestamp | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /IFD/XMP/EXIF: gpstimestamp | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 29}       |
| 2     | /IFD/XMP/EXIF: gpstimestamp |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
