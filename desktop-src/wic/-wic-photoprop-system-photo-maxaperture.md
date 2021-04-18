---
description: Die fotometadatenrichtlinie für die System. Photo. maxaperture-Eigenschaft.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: System. Photo. maxaperture-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347675"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>System. Photo. maxaperture-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. maxaperture](../properties/props-system-photo-maxaperture.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto ( \_ maxaperture)

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. maxaperturenumerator" und "System. Photo. maxaperturenenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /XMP/EXIF: MaxApertureValue    |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |             |
| 2     | /XMP/EXIF: MaxApertureValue    |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37381} |
| 2     | /XMP/EXIF: MaxApertureValue    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |             |
| 2     | /IFD/XMP/EXIF: MaxApertureValue |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |             |
| 2     | /IFD/XMP/EXIF: MaxApertureValue |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 37381}       |
| 2     | /IFD/XMP/EXIF: MaxApertureValue |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. maxaperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
