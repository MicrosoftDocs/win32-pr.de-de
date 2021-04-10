---
description: Die fotometadatenrichtlinie für die System. Photo. Orientation-Eigenschaft.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: System. Photo. Orientation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050297"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>System. Photo. Orientation-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ Ausrichtung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: Ausrichtung  | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                   | Datenträger Format |
|-------|------------------------|-------------|
| 1     | /App1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: Ausrichtung  | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                   |
|-------|------------------------|
| 1     | /App1/IFD/{ushort = 274} |
| 2     | /XMP/TIFF: Ausrichtung  |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: Ausrichtung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                      | Datenträger Format |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: Ausrichtung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 274}         |
| 2     | /IFD/XMP/TIFF: Ausrichtung |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
