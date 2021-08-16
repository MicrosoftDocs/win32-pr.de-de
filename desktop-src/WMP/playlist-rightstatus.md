---
title: PLAYLIST.rightStatus
description: Das rightStatus-Attribut gibt den Statustext an, der rechts und unten im PLAYLIST-Element angezeigt wird, oder ruft diesen ab.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- PLAYLIST.rightStatus-Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b79b0f4e3ad18ed4e044f894d63ec5059477f80999a8b96dc461d9499b29cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336563"
---
# <a name="playlistrightstatus"></a>PLAYLIST.rightStatus

Das **rightStatus-Attribut** gibt den Statustext an, der rechts und unten im **PLAYLIST-Element** angezeigt wird, oder ruft diesen ab.

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Dieses Attribut kann beliebigen Text mit bestimmten Schlüsselwörtern kombinieren, die die gewünschten Informationen anzeigen, z. B. die Gesamtdauer der Wiedergabeliste. Die Schlüsselwörter werden von Prozentzeichen (%) umgeben, um sie vom normalen Text zu unterscheiden.

Die folgenden Schlüsselwörter können verwendet werden.



| Stichwort               | BESCHREIBUNG                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Anzahl der Elemente in der Wiedergabeliste.                                                                                                                                                                             |
| Größe                  | Gesamtgröße der Wiedergabeliste.                                                                                                                                                                                  |
| duration              | Gesamtdauer der Wiedergabeliste.                                                                                                                                                                              |
| *Xxx*                 | Führt eine **getItemInfo** in der Wiedergabeliste aus, wobei *XXX* das zu empfangende Element ist.                                                                                                                                 |
| SelectedSize          | Gesamtgröße der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                          |
| SelectedCount         | Gesamtanzahl der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                            |
| SelectedDuration      | Gesamtdauer der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                      |
| CheckedCount          | Gesamtanzahl der überprüften Spuren in der Wiedergabeliste.                                                                                                                                                              |
| CheckedDuration       | Gesamtdauer der überprüften Spuren in der Wiedergabeliste.                                                                                                                                                        |
| CheckedSize           | Gesamtgröße der überprüften Spuren in der Wiedergabeliste.                                                                                                                                                            |
| DurationString        | Zeigt Text an, der die Dauer als "Gesamtzeit" oder "Geschätzte Zeit" beschreibt, je nachdem, ob die Gesamtwerte bekannt sind. Auf diesen Text folgt "%duration%".                                       |
| CheckedDurationString | Zeigt Text an, der die Dauer aller aktivierten Elemente in der Wiedergabeliste als "Gesamtzeit" oder "Geschätzte Zeit" beschreibt, je nachdem, ob die Gesamtwerte bekannt sind. Auf diesen Text folgt "%duration%". |



 

Der Wert "Gesamtzeit: %duration%" für eine Wiedergabeliste, die eine Gesamtdauer von sieben Minuten enthält, zeigt "Gesamtzeit: 07:00" an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> </dl>

 

 





