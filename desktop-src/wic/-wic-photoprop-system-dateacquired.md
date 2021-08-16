---
description: Die Fotometadatenrichtlinie für die System.DateAcquired-Eigenschaft.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: System.DateAcquired-Fotometadatenrichtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95b8f68d99476db0832a321de1f61c6f3c4dc6be6f10d679735bd51fc92ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087881"
---
# <a name="systemdateacquired-photo-metadata-policy"></a>System.DateAcquired-Fotometadatenrichtlinie

Die Fotometadatenrichtlinie für die [System.DateAcquired-Eigenschaft.](../properties/props-system-dateacquired.md)

### <a name="pkey"></a>PKEY

PKEY \_ DateAcquired

### <a name="containers"></a>Container

JPEG, TIFF

### <a name="read-only"></a>Schreibgeschützt

Nein

### <a name="output-propvariant-type"></a>PROPVARIANT-Ausgabetyp

VT \_ FILETIME

### <a name="input-propvariant-type"></a>Propvariant-Eingabetyp

VT \_ FILETIME

### <a name="conflict-resolution-policy"></a>Konfliktlösungsrichtlinie

Werte aus unterschiedlichen Schemas werden abgestimmt.

### <a name="precedence-of-paths-jpeg"></a>Rangfolge von Pfaden (JPEG)

Wenn die Datei im JPEG-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:



| Auftrag | Pfad                             | Datenträgerformat                        | Erforderlich |
|-------|----------------------------------|------------------------------------|----------|
| 1     | /xmp/MicrosoftPhoto:DateAcquired | Unicode-Zeichenfolge im XMP-Datumsformat. | Ja      |



 

### <a name="precedence-of-paths-tiff"></a>Rangfolge von Pfaden (Precedence of Paths, TIFF)

Wenn die Datei im TIFF-Format vorliegt, sucht der Handler in der folgenden Reihenfolge nach den Daten:



| Auftrag | Pfad                                 | Datenträgerformat                        | Erforderlich |
|-------|--------------------------------------|------------------------------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:DateAcquired | Unicode-Zeichenfolge im XMP-Datumsformat. | Ja      |



 

## <a name="remarks"></a>Hinweise

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System.DateAcquired](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
