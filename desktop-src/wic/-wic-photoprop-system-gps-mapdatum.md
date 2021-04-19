---
description: Die fotometadatenrichtlinie für die System. GPS. mapdatum-Eigenschaft.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: System. GPS. mapdatum-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373309"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>System. GPS. mapdatum-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. mapdatum](../properties/props-system-gps-mapdatum.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ mapdatum

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                          | Datenträger Format | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /XMP/EXIF: gpsmapdatum         | Unicode     | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 18 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                      | Datenträger Format | Erforderlich |
|-------|---------------------------|-------------|----------|
| 1     | /IFD/XMP/EXIF: gpsmapdatum | Unicode     | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 18 \\ }  | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. mapdatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
