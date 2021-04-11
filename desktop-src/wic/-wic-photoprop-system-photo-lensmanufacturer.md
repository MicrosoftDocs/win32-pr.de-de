---
description: Die fotometadatenrichtlinie für die System. Photo. lensmanufacturer-Eigenschaft.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: System. Photo. lensmanufacturer-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217382"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a>System. Photo. lensmanufacturer-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. lensmanufacturer](../properties/props-system-photo-lensmanufacturer.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ lensmanufacturer

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



| Auftrag | Pfad                                 | Datenträger Format | Erforderlich |
|-------|--------------------------------------|-------------|----------|
| 1     | /XMP/MicrosoftPhoto: lensmanufacturer | Unicode     | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                                     | Datenträger Format | Erforderlich |
|-------|------------------------------------------|-------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: lensmanufacturer | Unicode     | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. lensmanufacturer](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
