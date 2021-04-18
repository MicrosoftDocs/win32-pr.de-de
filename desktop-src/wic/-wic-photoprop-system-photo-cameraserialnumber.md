---
description: Die fotometadatenrichtlinie für die System. Photo. cameraserialnumber-Eigenschaft.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: System. Photo. cameraserialnumber-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352673"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a>System. Photo. cameraserialnumber-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. cameraserialnumber](../properties/props-system-photo-cameraserialnumber.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ cameraserialnumber

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

Wenn die Datei das JPEG-Format hat, werden die Daten vom Handler gelesen, geschrieben und aus folgendem Pfad entfernt:



| Auftrag | Pfad                                   | Datenträger Format | Erforderlich |
|-------|----------------------------------------|-------------|----------|
| 1     | /XMP/MicrosoftPhoto: cameraserialnumber | Unicode     | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, werden die Daten vom Handler gelesen, geschrieben und aus folgendem Pfad entfernt.



| Auftrag | Pfad                                       | Datenträger Format | Erforderlich |
|-------|--------------------------------------------|-------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: cameraserialnumber | Unicode     | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. cameraserialnumber](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
