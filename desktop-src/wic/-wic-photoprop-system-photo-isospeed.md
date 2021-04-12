---
description: Die fotometadatenrichtlinie für die System. Photo. Isospeed-Eigenschaft.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: System. Photo. Isospeed-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346599"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>System. Photo. Isospeed-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Isospeed](../properties/props-system-photo-focallengthinfilm.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ Isospeed

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



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /XMP/EXIF: Isospeed                      | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /XMP/EXIF: Isospeed                      | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 34855}           |
| 2     | /XMP/ <xmpseq> EXIF: ISOSpeedRatings |
| 3     | /XMP/EXIF: Isospeed                      |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                        | Datenträger Format |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /IFD/XMP/EXIF: Isospeed                      | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                        | Datenträger Format |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings | Unicode     |
| 3     | /IFD/XMP/EXIF: Isospeed                      | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                        |
|-------|---------------------------------------------|
| 1     | /IFD/EXIF/{ushort = 34855}                    |
| 2     | /IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings |
| 3     | /IFD/XMP/EXIF: Isospeed                      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Isospeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
