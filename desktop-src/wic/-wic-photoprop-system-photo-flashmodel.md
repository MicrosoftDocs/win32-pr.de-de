---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Model-Eigenschaft.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: System. Photo. Flash Model-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362332"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>System. Photo. Flash Model-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Flash Model](../properties/props-system-photo-flashmodel.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto- \_ Flash Modell

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

Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.



| Auftrag | Pfad                           | Datenträger Format | Datenformat | Erforderlich |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /XMP/MicrosoftPhoto: Flash Model | Unicode     |             | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                               | Datenträger Format | Datenformat | Erforderlich |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: Flash Model | Unicode     |             | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Flash Model](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
