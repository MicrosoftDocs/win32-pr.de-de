---
description: Die fotometadatenrichtlinie für die System. Photo. Brightness-Eigenschaft.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: System. Photo. Helligkeit Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960580"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a>System. Photo. Helligkeit Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Brightness](../properties/props-system-photo-aperture.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Helligkeit

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="input-type"></a>Eingabetyp

Double

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von "System. Photo. aperturenumerator" und "System. Photo. aperturenenner" generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /XMP/EXIF: brightnessvalue     |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |             |
| 2     | /XMP/EXIF: brightnessvalue     |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37379} |
| 2     | /XMP/EXIF: brightnessvalue     |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |             |
| 2     | /IFD/XMP/EXIF: brightnessvalue |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |             |
| 2     | /IFD/XMP/EXIF: brightnessvalue |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /IFD/EXIF/{ushort = 37379}      |
| 2     | /IFD/XMP/EXIF: brightnessvalue |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Helligkeit](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
