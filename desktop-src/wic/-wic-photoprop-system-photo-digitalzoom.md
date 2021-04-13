---
description: Die fotometadatenrichtlinie für die System. Photo. Digitalzoom-Eigenschaft.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: System. Photo. Digitalzoom-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347428"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a>System. Photo. Digitalzoom-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Digitalzoom](../properties/props-system-photo-digitalzoom.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Digitalzoom

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird von System. Photo. digitalzoomzähler und System. Photo. digitalzoomnenner generiert. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /XMP/EXIF: DigitalZoomRatio    |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |             |
| 2     | /XMP/EXIF: DigitalZoomRatio    |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 41988} |
| 2     | /XMP/EXIF: DigitalZoomRatio    |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |             |
| 2     | /IFD/XMP/EXIF: DigitalZoomRatio |             |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |             |
| 2     | /IFD/XMP/EXIF: DigitalZoomRatio |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/EXIF/{ushort = 41988}       |
| 2     | /IFD/XMP/EXIF: DigitalZoomRatio |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Digitalzoom](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
