---
description: Die fotometadatenrichtlinie für die System. Photo. f Number-Eigenschaft.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: System. Photo. f Number-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216810"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>System. Photo. f Number-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. f Number](../properties/props-system-photo-fnumber.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ f-Nummer

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. vnumzähler" und "System. Photo. f-Nenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33437} |             |
| 2     | /XMP/EXIF: f-Nummer             |             |



 

### <a name="write-paths"></a>Schreib Pfade



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| Auftrag | Pfad                          | Datenträger Format |     |
| 1     | /App1/IFD/EXIF/{ushort = 33437} |             |     |
| 2     | /XMP/EXIF: f-Nummer             |             |     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 33437} |
| 2     | /XMP/EXIF: f-Nummer             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33437} |             |
| 2     | /IFD/XMP/EXIF: f-Nummer    |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33437} |             |
| 2     | /IFD/XMP/EXIF: f-Nummer    |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /IFD/EXIF/{ushort = 33437} |
| 2     | /IFD/XMP/EXIF: f-Nummer    |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. f Number](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
