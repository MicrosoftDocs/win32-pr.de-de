---
description: Die Fotometadatenrichtlinie für die System.Photo.FlashModel-Eigenschaft.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: System.Photo.FlashModel-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c9e45e1ef759f2bee0d383cde3bcdabe8be67dc55a463ab6c9f7e6e05889a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204881"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a>System.Photo.FlashModel-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.Photo.FlashModel-Eigenschaft.](../properties/props-system-photo-flashmodel.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FlashModel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.



| Auftrag | Pfad                           | Datenträgerformat | Datenformat | Erforderlich |
|-------|--------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (Precedence of Paths, TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                               | Datenträgerformat | Datenformat | Erforderlich |
|-------|------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashModel | Unicode     |             | Ja      |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
