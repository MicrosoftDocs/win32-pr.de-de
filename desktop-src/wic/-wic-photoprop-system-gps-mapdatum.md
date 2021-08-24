---
description: Die Fotometadatenrichtlinie für die System.GPS.MapDatum-Eigenschaft.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: System.GPS.MapDatum-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bbd3671ec9e025dd2c5ea98fc36f4937abab315b09a2227fb6249d74e577da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882340"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>System.GPS.MapDatum-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.MapDatum-Eigenschaft.](../properties/props-system-gps-mapdatum.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                          | Datenträgerformat | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Ja      |
| 2     | /app1/ifd/gps/ \\ {ushort=18 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (Precedence of Paths, TIFF)

Wenn die Datei im TIFF-Format vorliegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                      | Datenträgerformat | Erforderlich |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Ja      |
| 2     | /ifd/gps/ \\ {ushort=18 \\ }  | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
