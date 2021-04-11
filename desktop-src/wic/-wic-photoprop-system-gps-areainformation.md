---
description: Die fotometadatenrichtlinie für die System. GPS. areainformation-Eigenschaft.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: System. GPS. areainformation-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346418"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>System. GPS. areainformation-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. areainformation](../properties/props-system-gps-areainformation.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ areainformation

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policies"></a>JPEG-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |             |
| 2     | /XMP/EXIF: gpsareainformation | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                         | Datenträger Format |
|-------|------------------------------|-------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |             |
| 2     | /XMP/EXIF: gpsareainformation | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                         |
|-------|------------------------------|
| 1     | /App1/IFD/GPS/{ushort = 28}    |
| 2     | /XMP/EXIF: gpsareainformation |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 28}             |             |
| 2     | /IFD/XMP/EXIF: gpsareainformation | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                             | Datenträger Format |
|-------|----------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 28}             |             |
| 2     | /IFD/XMP/EXIF: gpsareainformation | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                             |
|-------|----------------------------------|
| 1     | /IFD/GPS/{ushort = 28}             |
| 2     | /IFD/XMP/EXIF: gpsareainformation |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. areainformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
