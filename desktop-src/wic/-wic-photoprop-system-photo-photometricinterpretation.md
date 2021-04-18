---
description: Die fotometadatenrichtlinie für die System. Photo. photomezcinterpretation-Eigenschaft.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: System. Photo. photomezcinterpretation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352615"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>System. Photo. photomezcinterpretation-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. photomezcinterpretation](../properties/props-system-photo-photometricinterpretation.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ foequcinterpretation

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI2

### <a name="input-type"></a>Eingabetyp

UShort

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /App1/IFD/{ushort = 262}              | ushort      |
| 2     | /XMP/TIFF: photomezcinterpretation | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                | Datenträger Format |
|-------|-------------------------------------|-------------|
| 1     | /App1/IFD/{ushort = 262}              | ushort      |
| 2     | /XMP/TIFF: photomezcinterpretation | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                |
|-------|-------------------------------------|
| 1     | /App1/IFD/{ushort = 262}              |
| 2     | /XMP/TIFF: photomezcinterpretation |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{ushort = 262}                       | ushort      |
| 2     | /IFD/XMP/TIFF: photomezcinterpretation | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                                    | Datenträger Format |
|-------|-----------------------------------------|-------------|
| 1     | /IFD/{ushort = 262}                       | ushort      |
| 2     | /IFD/XMP/TIFF: photomezcinterpretation | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                                    |
|-------|-----------------------------------------|
| 1     | /IFD/{ushort = 262}                       |
| 2     | /IFD/XMP/TIFF: photomezcinterpretation |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. photomezcinterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
