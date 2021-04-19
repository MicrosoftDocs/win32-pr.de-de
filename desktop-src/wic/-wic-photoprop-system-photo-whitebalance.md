---
description: Die fotometadatenrichtlinie für die System. Photo. WhiteBalance-Eigenschaft.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: System. Photo. WhiteBalance Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349596"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a>System. Photo. WhiteBalance Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ WhiteBalance

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
| 1     | /App1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /XMP/EXIF: WhiteBalance        | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41987} | ushort      |
| 2     | /XMP/EXIF: WhiteBalance        | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41987} |
| 2     | /XMP/EXIF: WhiteBalance        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41987}   | ushort      |
| 2     | /IFD/XMP/EXIF: WhiteBalance | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41987}   | ushort      |
| 2     | /IFD/XMP/EXIF: WhiteBalance | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{ushort = 41987}   |
| 2     | /IFD/XMP/EXIF: WhiteBalance |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. WhiteBalance](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
