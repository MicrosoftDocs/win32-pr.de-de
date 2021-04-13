---
description: Die fotometadatenrichtlinie für die System. Rating-Eigenschaft.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: System. Rating Photo Metadata-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347178"
---
# <a name="systemrating-photo-metadata-policy"></a>System. Rating Photo Metadata-Richtlinie

Die fotometadatenrichtlinie für die [System. Rating](../properties/props-system-rating.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Bewertung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ UI4

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

Kann "VT \_ UI1", "VT \_ UI2" oder "VT UI4" lauten \_ . Der Wert kann zwischen 0 und 99 liegen.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18249}   | ushort      |
| 2     | /XMP/MicrosoftPhoto: Bewertung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                       | Datenträger Format |
|-------|----------------------------|-------------|
| 1     | /App1/IFD/{ushort = 18249}   | ushort      |
| 2     | /XMP/MicrosoftPhoto: Bewertung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /App1/IFD/{ushort = 18249}   |
| 2     | /XMP/microsoftphoto: Bewertung |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Pfade lesen



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /IFD/XMP/MicrosoftPhoto: Bewertung | Unicode     |



 

### <a name="write-paths"></a>Schreib Pfade



| Auftrag | Pfad                           | Datenträger Format |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /IFD/XMP/MicrosoftPhoto: Bewertung | Unicode     |



 

### <a name="remove-paths"></a>Pfade entfernen



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /IFD/{ushort = 18249}            |
| 2     | /IFD/XMP/microsoftphoto: Bewertung |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
