---
title: Wiedergabeliste. leftstatus
description: Das leftstatus-Attribut gibt den Status Text an oder ruft ihn ab, der auf der linken und unteren Seite des Wiedergabelisten Elements angezeigt wird.
ms.assetid: c83f4fd1-d0e6-4822-9208-8e968c409a78
keywords:
- Wiedergabeliste. leftstatus Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.leftStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33d4c3d235a7bba67219378063cb9811601e68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354152"
---
# <a name="playlistleftstatus"></a>Wiedergabeliste. leftstatus

Das **leftstatus** -Attribut gibt den Status Text an oder ruft ihn ab, der auf der linken und unteren Seite des **Wiedergabe** Listen Elements angezeigt wird.

``` syntax
        elementID.leftStatus
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann beliebigen Text mit bestimmten Schlüsselwörtern kombinieren, die die gewünschten Informationen anzeigen, z. b. die Gesamtdauer der Wiedergabeliste. Die Schlüsselwörter sind von Prozentzeichen (%) umgeben. , wenn Sie sich vom normalen Text unterscheiden.

Die folgenden Schlüsselwörter können verwendet werden.



| Schlüsselwort               | BESCHREIBUNG                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count                 | Anzahl der Elemente in der Wiedergabeliste.                                                                                                                                                                             |
| Größe                  | Gesamtgröße der Wiedergabeliste.                                                                                                                                                                                  |
| duration              | Gesamtdauer der Wiedergabeliste.                                                                                                                                                                              |
| *XXX*                 | Führt ein **getiteminfo** -Element auf der Wiedergabeliste mit *xxx* als Element aus, das empfangen werden soll.                                                                                                                                 |
| SelectedSize          | Gesamtgröße der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                          |
| SelectedCount         | Die Gesamtanzahl der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                            |
| Selectedduration      | Gesamtdauer der ausgewählten Einträge in der Wiedergabeliste.                                                                                                                                                      |
| Checkedcount          | Die Gesamtanzahl der überprüften Titel in der Wiedergabeliste.                                                                                                                                                              |
| Checkedduration       | Gesamtdauer der aktivierten Titel in der Wiedergabeliste.                                                                                                                                                        |
| Checkedsize           | Gesamtgröße der aktivierten Titel in der Wiedergabeliste.                                                                                                                                                            |
| DurationString        | Zeigt Text an, der die Dauer in Abhängigkeit davon, ob die Gesamtwerte bekannt sind, als "Gesamtzeit" oder "geschätzte Zeit" beschreibt. Auf diesen Text folgt "% Duration%".                                       |
| Checkeddurationstring | Zeigt Text an, der die Dauer für alle aktivierten Elemente in der Wiedergabeliste als "gesamte Zeit" oder "geschätzte Zeit" beschreibt, abhängig davon, ob die Gesamtwerte bekannt sind. Auf diesen Text folgt "% Duration%". |



 

Der Wert "Gesamtzeit:% Duration%" für eine Wiedergabeliste, die eine Gesamtdauer von sieben Minuten enthält, wird "Gesamtzeit: 07:00" angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> </dl>

 

 





