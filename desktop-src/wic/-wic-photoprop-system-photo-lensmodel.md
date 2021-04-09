---
description: Die fotometadatenrichtlinie für die System. Photo. lensmodel-Eigenschaft.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: System. Photo. lensmodel-fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050298"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a>System. Photo. lensmodel-fotometadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. lensmodel](../properties/props-system-photo-lensmodel.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey- \_ Foto \_ lensmodel

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



| Auftrag | Pfad                          | Datenträger Format | Erforderlich |
|-------|-------------------------------|-------------|----------|
| 1     | /XMP/MicrosoftPhoto: lensmodel | Unicode     | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                              | Datenträger Format | Erforderlich |
|-------|-----------------------------------|-------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: lensmodel | Unicode     | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. lensmodel](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
