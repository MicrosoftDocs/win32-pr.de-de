---
description: Die fotometadatenrichtlinie für die System. Photo. meteringmode-Eigenschaft.
ms.assetid: cb0bf0d5-eccf-4345-a242-76769c34e02d
title: System. Photo. meteringmode Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12a4443521c84113e4e2a6f4c2b9b2b3f822ae90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373217"
---
# <a name="systemphotometeringmode-photo-metadata-policy"></a>System. Photo. meteringmode Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Photo. meteringmode](../properties/props-system-photo-meteringmode.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto ( \_ meteringmode)

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /XMP/EXIF: meteringmode        | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37383} | ushort      |
| 2     | /XMP/EXIF: meteringmode        | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37383} |
| 2     | /XMP/EXIF: meteringmode        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37383}   | ushort      |
| 2     | /IFD/XMP/EXIF: meteringmode | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37383}   | ushort      |
| 2     | /IFD/XMP/EXIF: meteringmode | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{ushort = 37383}   |
| 2     | /IFD/XMP/EXIF: meteringmode |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. meteringmode](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
