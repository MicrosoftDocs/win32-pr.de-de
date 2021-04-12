---
description: Die fotometadatenrichtlinie für die System. dateerworgenschaft.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: System. dateerworbenes Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218034"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>System. dateerworbenes Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. dateerworgenschaft](../properties/props-system-dateacquired.md) .

### <a name="pkey"></a>Pkey

Pkey- \_ datebezogen

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>Ausgabe-PROPVARIANT-Typ

VT \_ FILETIME

### <a name="input-propvariant-type"></a>Eingabe-PROPVARIANT-Typ

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>Richtlinie zur Konfliktlösung

Werte aus unterschiedlichen Schemas sind abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:



| Auftrag | Pfad                             | Datenträger Format                        | Erforderlich |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /XMP/MicrosoftPhoto: dateerworbener | Unicode-Zeichenfolge im XMP-Datumsformat. | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:



| Auftrag | Pfad                                 | Datenträger Format                        | Erforderlich |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: dateerworbener | Unicode-Zeichenfolge im XMP-Datumsformat. | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. dateerworbener](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
