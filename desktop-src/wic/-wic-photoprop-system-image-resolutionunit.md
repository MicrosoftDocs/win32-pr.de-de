---
description: Die fotometadatenrichtlinie für die System. Image. ResolutionUnit-Eigenschaft.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: System. Image. ResolutionUnit Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351718"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>System. Image. ResolutionUnit Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Image \_ ResolutionUnit

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja.

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ I2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 296}   | ushort      |
| 2     | /XMP/TIFF: ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                     | Datenträger Format |
|-------|--------------------------|-------------|
| 1     | /App1/IFD/{ushort = 296}   | ushort      |
| 2     | /XMP/TIFF: ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                     |
|-------|--------------------------|
| 1     | /App1/IFD/{ushort = 296}   |
| 2     | /XMP/TIFF: ResolutionUnit |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /IFD/XMP/TIFF: ResolutionUnit | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /IFD/XMP/TIFF: ResolutionUnit | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /IFD/{ushort = 296}            |
| 2     | /IFD/XMP/TIFF: ResolutionUnit |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
