---
description: Die fotometadatenrichtlinie für die System. Image. VerticalResolution-Eigenschaft.
ms.assetid: a58b7463-3572-4ca8-8299-93d92d2f06fb
title: System. Image. VerticalResolution Photo-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e895ef9e1181a3ec40b474940c6dfaaa3e1329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368789"
---
# <a name="systemimageverticalresolution-photo-metadata-policy"></a>System. Image. VerticalResolution Photo-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Verticalauflösung des pkey- \_ Bilds \_

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
| 1     | /App1/IFD/{ushort = 283} |             |
| 2     | /XMP/TIFF: YResolution  |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                        |
|-------|-----------------------------|
| 1     | /App1/IFD/EXIF/{ushort = 283} |
| 2     | /XMP/TIFF: YResolution       |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/EXIF/{ushort = 283}    |             |
| 2     | /IFD/XMP/TIFF: YResolution |             |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/EXIF/{ushort = 283}    |
| 2     | /IFD/XMP/TIFF: YResolution |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. VerticalResolution](../properties/props-system-image-verticalresolution.md)
</dt> </dl>

 

 
