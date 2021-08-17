---
description: Die Richtlinie für Fotometadaten für die System.Photo.LensModel-Eigenschaft.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: System.Photo.LensModel-Richtlinie für Fotometadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07fff44e14a04dab220f8dbce243a638710f30db253c43c1ff79a240bb32f3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441870"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>System.Photo.LensModel-Richtlinie für Fotometadaten

Die Richtlinie für Fotometadaten für die [System.Photo.LensModel-Eigenschaft.](../properties/props-system-photo-lensmodel.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ LensModel

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ LPWSTR

### <a name="input-type"></a>Eingabetyp

Eine Zeichenfolge.

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus verschiedenen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vor liegt, verwendet der Handler beim Lesen oder Schreiben der Daten den folgenden Pfad.



| Auftrag | Pfad                          | Datenträgerformat | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:LensModel | Unicode     | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vor liegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                              | Datenträgerformat | Erforderlich |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:LensModel | Unicode     | Ja      |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.Photo.LensModel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
