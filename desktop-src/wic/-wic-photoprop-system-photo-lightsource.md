---
description: Die fotometadatenrichtlinie für die System. Photo. LightSource-Eigenschaft.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: System. Photo. LightSource-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529936"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a>System. Photo. LightSource-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. LightSource](../properties/props-system-photo-lightsource.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo \_ LightSource

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
| 1     | /App1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /XMP/EXIF: LightSource         | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                          | Datenträger Format |
|-------|-------------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 37384} | ushort      |
| 2     | /XMP/EXIF: LightSource         | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                          |
|-------|-------------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 37384} |
| 2     | /XMP/EXIF: LightSource         |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: LightSource | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 37384}  | ushort      |
| 2     | /IFD/XMP/EXIF: LightSource | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 37384}  |
| 2     | /IFD/XMP/EXIF: LightSource |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. LightSource](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
