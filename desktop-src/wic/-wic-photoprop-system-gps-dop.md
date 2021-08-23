---
description: Die Richtlinie für Fotometadaten für die System.GPS.DOP-Eigenschaft.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: System.GPS.DOP-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c414b7cb8648210175953e4c7b5f51a66f026cb45a06fd4d62918f2f8ac369
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087788"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>System.GPS.DOP-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.GPS.DOP-Eigenschaft.](../properties/props-system-gps-dop.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ R8

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Dieser Wert kann durch Schreiben in System.GPS.DOPNumerator und System.GPS.DOPDenominator geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                          | Datenträgerformat   | Erforderlich |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP rational  | Ja      |
| 2     | /app1/ifd/gps/ \\ {ushort=11 \\ } | EXIF rational | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vor liegt, liest, schreibt und entfernt der Handler die Daten in der folgenden Reihenfolge:



| Auftrag | Pfad                     | Datenträgerformat   | Erforderlich |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP rational  | Ja      |
| 2     | /ifd/gps/ \\ {ushort=11 \\ } | EXIF rational | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.GPS.DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
