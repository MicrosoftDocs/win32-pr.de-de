---
description: Die fotometadatenrichtlinie für die System. Photo. Aperture-Eigenschaft.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: System. Photo. Aperture-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352674"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>System. Photo. Aperture-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Aperture](../properties/props-system-photo-aperture.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ Aperture

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. aperturenumerator" und "System. Photo. aperturenenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /XMP/EXIF: aperturevalue       |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |             |
| 2     | /XMP/EXIF: aperturevalue       |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37378} |
| 2     | /XMP/EXIF: aperturevalue       |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |             |
| 2     | /IFD/XMP/EXIF: aperturevalue |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                        | Datenträger Format |
|-------|-----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |             |
| 2     | /IFD/XMP/EXIF: aperturevalue |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /IFD/EXIF/{ushort = 37378}    |
| 2     | /IFD/XMP/EXIF: aperturevalue |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Aperture](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
