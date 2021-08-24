---
description: Die Fotometadatenrichtlinie für die System.Photo.LensManufacturer-Eigenschaft.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: System.Photo.LensManufacturer-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f6beebc06ce690b05da62c023480bec25b675a7a9ec6093cec1752ac3a0e343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881982"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>System.Photo.LensManufacturer-Richtlinie für Fotometadaten

Die Fotometadatenrichtlinie für die [System.Photo.LensManufacturer-Eigenschaft.](../properties/props-system-photo-lensmanufacturer.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensManufacturer

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



| Auftrag | Pfad                                 | Datenträgerformat | Erforderlich |
|-------|--------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (Precedence of Paths, TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                                     | Datenträgerformat | Erforderlich |
|-------|------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensManufacturer | Unicode     | Ja      |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
