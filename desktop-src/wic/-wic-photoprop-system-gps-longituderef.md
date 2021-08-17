---
description: Die Richtlinie für Fotometadaten für die System.GPS.LongitudeRef-Eigenschaft.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: System.GPS.LongitudeRef-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00908f0c76305c745e1146677f32bee7b9724c08510f273c1627ed56e139d02b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931730"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>System.GPS.LongitudeRef-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.LongitudeRef-Eigenschaft.](../properties/props-system-gps-longituderef.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LongitudeRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                         | Datenträgerformat | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Ja      |
| 2     | /app1/ifd/gps/ \\ {ushort=3 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                          | Datenträgerformat | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Ja      |
| 2     | /ifd/gps/ \\ {ushort=3 \\ }       | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
