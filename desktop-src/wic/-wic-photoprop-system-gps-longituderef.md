---
description: Die fotometadatenrichtlinie für die System. GPS. die-Eigenschaft.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: System. GPS.-metadatenrichtlinie für Fotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350900"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>System. GPS.-metadatenrichtlinie für Fotos

Die fotometadatenrichtlinie für die [System. GPS. die-](../properties/props-system-gps-longituderef.md) Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ längs

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

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                         | Datenträger Format | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /XMP/EXIF: gpsordneref    | Unicode     | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 3 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                          | Datenträger Format | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /IFD/XMP/EXIF: gpsordneref | Unicode     | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 3 \\ }       | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. längs-EF](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
