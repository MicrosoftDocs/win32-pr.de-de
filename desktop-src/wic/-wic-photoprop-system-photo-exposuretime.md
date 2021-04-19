---
description: Die fotometadatenrichtlinie für die System. Photo. ExposureTime-Eigenschaft.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: System. Photo. ExposureTime-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349952"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a>System. Photo. ExposureTime-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ ExposureTime

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von System. Photo. exposuretimenenumerator und System. Photo. exposuretimenenner generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /XMP/EXIF: ExposureTime        |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |             |
| 2     | /XMP/EXIF: ExposureTime        |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 33434} |
| 2     | /XMP/EXIF: ExposureTime        |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: ExposureTime |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |             |
| 2     | /IFD/XMP/EXIF: ExposureTime |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /IFD/EXIF/{ushort = 33434}   |
| 2     | /IFD/XMP/EXIF: ExposureTime |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. ExposureTime](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
