---
title: System. Image. HorizontalResolution-Foto-metadatenrichtlinie
description: Die fotometadatenrichtlinie für die System. Image. HorizontalResolution-Eigenschaft.
ms.assetid: 1fe73c50-4179-4ea4-be1c-9e103fb65d59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade406e644524fea84ef6baf957aed661d2adf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756918"
---
# <a name="systemimagehorizontalresolution-photo-metadata-policy"></a>System. Image. HorizontalResolution-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Image \_ HorizontalResolution

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja.

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert wird vom System generiert und kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 282} |             |
| 2     | /XMP/TIFF: XResolution  |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        | Datenträgerformat |
|-------|-----------------------------|-------------|
| 1     | /App1/IFD/EXIF/{ushort = 282} |             |
| 2     | /XMP/TIFF: XResolution       |             |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 282}    |             |
| 2     | /IFD/XMP/TIFF: XResolution |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      | Datenträgerformat |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 282}    |             |
| 2     | /IFD/XMP/TIFF: XResolution |             |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. HorizontalResolution](../properties/props-system-image-horizontalresolution.md)
</dt> </dl>

 

 
