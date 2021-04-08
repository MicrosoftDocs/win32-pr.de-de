---
description: Die fotometadatenrichtlinie für die System. GPS. DOP-Eigenschaft.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: System. GPS. DOP-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960660"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>System. GPS. DOP-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. DOP-](../properties/props-system-gps-dop.md) Eigenschaft.

### <a name="pkey"></a>Pkey

pkey \_ GPS- \_ DOP

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Ja

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ R8

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Dieser Wert kann durch Schreiben in System. GPS. dopnumerator und System. GPS. dopnenner geschrieben werden. Sie kann nicht direkt geschrieben werden. Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                          | Datenträger Format   | Erforderlich |
|-------|-------------------------------|---------------|----------|
| 1     | /XMP/EXIF: gpsdop              | XMP-rational  | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 11 \\ } | EXIF rational | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                     | Datenträger Format   | Erforderlich |
|-------|--------------------------|---------------|----------|
| 1     | /IFD/XMP/EXIF: gpsdop     | XMP-rational  | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 11 \\ } | EXIF rational | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
