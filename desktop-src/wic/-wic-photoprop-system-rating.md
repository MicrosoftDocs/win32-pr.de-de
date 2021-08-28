---
description: Die Richtlinie für Fotometadaten für die System.Rating-Eigenschaft.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: System.Rating-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25278ad7d881a0acadc5199fd07227bb650aaae4da2b6342070a64d69fd75240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086983"
---
# <a name="systemrating-photo-metadata-policy"></a>System.Rating-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Rating-Eigenschaft.](../properties/props-system-rating.md)

### <a name="pkey"></a>PKEY

\_PKEY-Bewertung

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ UI4

### <a name="input-propvariant-type"></a>PROPVARIANT-Eingabetyp

Dies kann VT \_ UI1, VT \_ UI2 oder VT \_ UI4 sein. Der Wert kann zwischen 0 und 99 liegen.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="jpeg-policy"></a>JPEG-Richtlinie

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                       | Datenträgerformat |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                       |
|-------|----------------------------|
| 1     | /app1/ifd/{ushort=18249}   |
| 2     | /xmp/microsoftphoto:rating |



 

### <a name="tiff-policies"></a>TIFF-Richtlinien

### <a name="read-paths"></a>Lesepfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | Unicode     |



 

### <a name="write-paths"></a>Schreibpfade



| Auftrag | Pfad                           | Datenträgerformat |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | Unicode     |



 

### <a name="remove-paths"></a>Entfernen von Pfaden



| Auftrag | Pfad                           |
|-------|--------------------------------|
| 1     | /ifd/{ushort=18249}            |
| 2     | /ifd/xmp/microsoftphoto:rating |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
