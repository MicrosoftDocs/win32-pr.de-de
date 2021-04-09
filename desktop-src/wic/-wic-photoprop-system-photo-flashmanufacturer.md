---
description: Die fotometadatenrichtlinie für die System. Photo. Flash Manufacturer-Eigenschaft.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: System. Photo. Flash Manufacturer-Foto-metadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050437"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>System. Photo. Flash Manufacturer-Foto-metadatenrichtlinie

Die fotometadatenrichtlinie für die [System. Photo. Flash Manufacturer](../properties/props-system-photo-flashmanufacturer.md) -Eigenschaft.

### <a name="pkey"></a>Pkey

Pkey \_ Photo- \_ Flash Hersteller

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



| Auftrag | Pfad                                  | Datenträger Format | Datenformat | Erforderlich |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /XMP/MicrosoftPhoto: Flash Hersteller | Unicode     |             | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (TIFF)

Wenn die Datei im TIFF-Format vorliegt, verwendet der Handler beim Lesen oder Schreiben der Daten die folgende Rangfolge.



| Auftrag | Pfad                                      | Datenträger Format | Datenformat | Erforderlich |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /IFD/XMP/MicrosoftPhoto: Flash Hersteller | Unicode     |             | Ja      |



 

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System. Photo. Flash Hersteller](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
