---
description: Die fotometadatenrichtlinie für die System. GPS. latituderef-Eigenschaft.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: System. GPS. latituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217518"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>System. GPS. latituderef-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. latituderef](../properties/props-system-gps-latitude.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS- \_ Struktur

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



| Auftrag | Pfad                         | Datenträger Format | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /XMP/EXIF: gpslatituderef     | Unicode     | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 1 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                         | Datenträger Format | Erforderlich |
|-------|------------------------------|-------------|----------|
| 1     | /IFD/XMP/EXIF: gpslatituderef | Unicode     | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 1 \\ }      | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. latituderef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
