---
description: Die fotometadatenrichtlinie für die System. GPS. destlatituderef-Eigenschaft.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: System. GPS. destlatituderef-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357882"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>System. GPS. destlatituderef-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. GPS. destlatituderef](../properties/props-system-gps-destlatituderef.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ GPS \_ destlatituderef

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                          | Datenträger Format | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /XMP/EXIF: gpsdestlatituderef  | Unicode     | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 19 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                             | Datenträger Format | Erforderlich |
|-------|----------------------------------|-------------|----------|
| 1     | /IFD/XMP/EXIF: gpsdestlatituderef | Unicode     | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 19 \\ }         | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destlatituderef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
