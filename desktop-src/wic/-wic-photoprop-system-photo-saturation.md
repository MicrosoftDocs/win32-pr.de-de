---
description: Die fotometadatenrichtlinie für die System. Photo. Sättigung-Eigenschaft.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: System. Photo. Sättigung-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050296"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>System. Photo. Sättigung-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Sättigung](../properties/props-system-photo-saturation.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Sättigung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI4

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /XMP/EXIF: Sättigung          | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /XMP/EXIF: Sättigung          | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41993} |
| 2     | /XMP/EXIF: Sättigung          |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: Sättigung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/EXIF: Sättigung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 41993} |
| 2     | /IFD/XMP/EXIF: Sättigung |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Sättigung](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
