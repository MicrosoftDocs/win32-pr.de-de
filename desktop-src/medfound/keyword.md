---
description: Gibt ein Schlüsselwort für einen MF-Ablaufverfolgungs-Anbieter an.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Keywords-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362902"
---
# <a name="keyword-element"></a>Keywords-Element

Gibt ein Schlüsselwort für einen [MF-Ablaufverfolgungs](mftrace.md) -Anbieter an.

## <a name="usage"></a>Verbrauch

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Attribute



| Attribut         | type             | Erforderlich       | BESCHREIBUNG                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Ja<br/> | Der Name oder die Maske des Schlüssel Worts.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                   |
|-------------------------------------------|
| [**MF-Umleitungen**](mfdetours.md)<br/> |
| [**ab**](provider.md)<br/>   |



## <a name="remarks"></a>Bemerkungen

Für das [**mfumleitungen**](mfdetours.md) -Element werden die gültigen Schlüsselwörter im Thema [mftrace-Schlüsselwörter](mftrace-keywords.md)aufgelistet.

Für das [**Provider**](provider.md) -Element sind die Schlüsselwörter vom Ereignis Anbieter abhängig. Mit dem Wevtutil.exe-Hilfsprogramm können Sie die Schlüsselwörter für einen bestimmten Anbieter auflisten.

## <a name="element-information"></a>Elementinformationen



|              |     |
|--------------|-----|
| Kann leer bleiben | Ja |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MF-Ablauf Verfolgungs Konfigurationsdatei](mftrace-configuration-file.md)
</dt> <dt>

[MF Trace-Schlüsselwörter](mftrace-keywords.md)
</dt> </dl>

 

 




