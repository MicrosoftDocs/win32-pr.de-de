---
title: BUTTON.cursor
description: Das Cursorattribut gibt den Cursor an, der angezeigt wird, wenn der Mauszeiger auf button zeigt, oder ruft diesen ab.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- BUTTON.cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa98c91080bc6d108e8ab62f0de99758c4eb6ba4229a83f8ded8b22bb2ec9695
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123790"
---
# <a name="buttoncursor"></a>BUTTON.cursor

Das  Cursorattribut gibt den Cursor an, der angezeigt wird, wenn der Mauszeiger auf button zeigt, oder ruft **diesen ab.**

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**



| Wert            | Beschreibung                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| System           | Standard. Plattformabhängiger Cursor (in der Regel ein Pfeil).                                     |
| Hand             | Hand.                                                                                      |
| Hilfe             | Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.                                     |
| sizeall          | Vier zeigende Pfeile, die nach Norden, Süden, Osten und Westen zeigen.                                  |
| sizenesw         | Doppelspitzenpfeil, der auf Nordosten und Nordosten zeigt.                                     |
| Größen           | Doppelter Pfeil, der nach Norden und Süden zeigt.                                             |
| sizenwse         | Doppelter Pfeil, der nach Nordosten und Südosten zeigt.                                     |
| sizewe           | Doppelter Pfeil, der nach Westen und Osten zeigt.                                               |
| Uparrow          | Vertikaler Pfeil, der nach oben zeigt.                                                            |
| \*.ani oder \* .cur | Jede ANI- oder CUR-Datei (muss sich im gleichen Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden) |



 

## <a name="remarks"></a>Hinweise

Wenn das System den angegebenen Cursorwert nicht erkennt, bleibt der Cursorwert beim zuvor festgelegten Wert.

Cursordateinamenpfade werden ignoriert, sodass sich die Cursordatei im Standardverzeichnis befinden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> </dl>

 

 





