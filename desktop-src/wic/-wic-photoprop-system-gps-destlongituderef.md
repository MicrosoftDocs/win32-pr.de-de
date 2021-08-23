---
description: Die Fotometadatenrichtlinie für die System.GPS.DestLongitudeRef-Eigenschaft.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: System.GPS.DestLongitudeRef-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fca1095138b35767da94e2eeed85a11892ba6edea3fa32f37ea6bd85fb76462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964949"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>System.GPS.DestLongitudeRef-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.GPS.DestLongitudeRef-Eigenschaft.](../properties/props-system-gps-destlongituderef.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS. DestLongitudeRef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber auch VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                          | Datenträgerformat | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Ja      |
| 2     | /app1/ifd/gps/ \\ {ushort=21 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (Precedence of Paths, TIFF)

Wenn die Datei im TIFF-Format vorliegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                              | Datenträgerformat | Erforderlich |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Ja      |
| 2     | /ifd/gps/ \\ {ushort=21 \\ }          | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
