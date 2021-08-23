---
description: Die Richtlinie für Fotometadaten für die System.GPS.LatitudeRef-Eigenschaft.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: System.GPS.LatitudeRef-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04412af5359e39eaf8e033b059b1c5460e33f6d7537c4763b009b11010fbe87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087248"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>System.GPS.LatitudeRef-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.LatitudeRef-Eigenschaft.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LatitudeRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                         | Datenträgerformat | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLifiref     | Unicode     | Ja      |
| 2     | /app1/ifd/gps/ \\ {ushort=1 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                         | Datenträgerformat | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSL gpsref | Unicode     | Ja      |
| 2     | /ifd/gps/ \\ {ushort=1 \\ }      | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
