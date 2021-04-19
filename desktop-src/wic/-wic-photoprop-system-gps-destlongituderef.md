---
description: Die fotometadatenrichtlinie für die Eigenschaft System. GPS. destlängs Deref.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: System. GPS. destlängs Deref-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362900"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>System. GPS. destlängs Deref-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die Eigenschaft [System. GPS. destlängs Deref](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>Pkey

pkey \_ GPS. Destlängs Deref

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ LPWSTR wird bevorzugt, aber VT \_ LPSTR wird ebenfalls akzeptiert.

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                          | Datenträger Format | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /XMP/EXIF: gpsdestlängs Deref | Unicode     | Ja      |
| 2     | /App1/IFD/GPS/ \\ {UShort = 21 \\ } | ASCII       | Nein       |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, wird der Handler die Daten in der folgenden Reihenfolge lesen, schreiben und entfernen:



| Auftrag | Pfad                              | Datenträger Format | Erforderlich |
|-------|-----------------------------------|-------------|----------|
| 1     | /IFD/XMP/EXIF: gpsdestlängs Deref | Unicode     | Ja      |
| 2     | /IFD/GPS/ \\ {UShort = 21 \\ }          | ASCII       | Nein       |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. GPS. destlängs Deref](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
