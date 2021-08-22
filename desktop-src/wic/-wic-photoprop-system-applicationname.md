---
description: Die Fotometadatenrichtlinie für die System.ApplicationName-Eigenschaft.
ms.assetid: bf4b310a-7e63-45c5-a327-2638fb31d676
title: Richtlinie für System.ApplicationName-Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3084f21453a82c79925d4a164f5f847c3a24968009b7b8c4236ce3a40872dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710919"
---
# <a name="systemapplicationname-photo-metadata-policy"></a>Richtlinie für System.ApplicationName-Fotometadaten

Die Fotometadatenrichtlinie für die [System.ApplicationName-Eigenschaft.](../properties/props-system-applicationname.md)

### <a name="pkey"></a>PKEY

PKEY \_ ApplicationName

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

String

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                         | Datenträgerformat |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /xmp/tiff:Software                           | Unicode     |
|       | /xmp/tiff:software                           | Unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                         | Datenträgerformat |
|-------|----------------------------------------------|-------------|
|       | /app1/ifd/{ushort=305}                       | ascii       |
|       | /xmp/xmp:CreatorTool                         | Unicode     |
|       | /xmp/xmp:creatortool                         | Unicode     |
|       | /xmp/tiff:Software                           | Unicode     |
|       | /xmp/tiff:software                           | Unicode     |
|       | /app13/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                         |
|-------|----------------------------------------------|
|       | /app1/ifd/{ushort=305}                       |
|       | /xmp/xmp:CreatorTool                         |
|       | /xmp/xmp:creatortool                         |
|       | /xmp/tiff:Software                           |
|       | /xmp/tiff:software                           |
|       | /app13/irb/8bimiptc/iptc/Originating Program |



 

### <a name="tiff-policy"></a>TIFF-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                                       | Datenträgerformat |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /ifd/xmp/tiff:Software                     | Unicode     |
|       | /ifd/xmp/tiff:software                     | Unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                                       | Datenträgerformat |
|-------|--------------------------------------------|-------------|
|       | /ifd/{ushort=305}                          | ascii       |
|       | /ifd/xmp/xmp:CreatorTool                   | Unicode     |
|       | /ifd/xmp/xmp:creatortool                   | Unicode     |
|       | /ifd/xmp/tiff:Software                     | Unicode     |
|       | /ifd/xmp/tiff:software                     | Unicode     |
|       | /ifd/iptc/Originating Program              |             |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |             |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                                       |
|-------|--------------------------------------------|
|       | /ifd/{ushort=305}                          |
|       | /ifd/xmp/xmp:CreatorTool                   |
|       | /ifd/xmp/xmp:creatortool                   |
|       | /ifd/xmp/tiff:Software                     |
|       | /ifd/xmp/tiff:software                     |
|       | /ifd/iptc/Originating Program              |
|       | /ifd/irb/8bimiptc/iptc/Originating Program |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.ApplicationName](../properties/props-system-applicationname.md)
</dt> </dl>

 

 
