---
title: BUTTONELEMENT.cursor
description: Das Cursorattribut gibt den Wert des BUTTONELEMENT-Cursors an, der angezeigt wird, wenn sich der Mauszeiger über BUTTONELEMENT befindet, oder ruft diesen ab.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT.cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f08d8e6b26ac2227d9040249b2daca55dcbe0ec068e120f1aba962bea0f089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764480"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT.cursor

Das  Cursorattribut gibt den Wert des **BUTTONELEMENT-Cursors** an oder ruft diesen ab, der angezeigt wird, wenn sich der Mauszeiger über **dem BUTTONELEMENT befindet.**

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**



| Wert            | Beschreibung                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| System           | Standard. Plattformabhängiger Cursor (in der Regel ein Pfeil).                                      |
| Hand             | Hand.                                                                                       |
| Hilfe             | Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.                                      |
| sizeall          | Vier zeigende Pfeile, die nach Norden, Süden, Osten und Westen zeigen.                                   |
| sizenesw         | Doppelspitzenpfeil, der auf Nordosten und Nordosten zeigt.                                      |
| Größen           | Doppelter Pfeil, der nach Norden und Süden zeigt.                                              |
| sizenwse         | Doppelspitzenpfeil, der nach Nordosten und Südosten zeigt.                                      |
| sizewe           | Doppelter Pfeil, der nach Westen und Osten zeigt.                                                |
| Uparrow          | Vertikaler Pfeil, der nach oben zeigt.                                                             |
| \*.ani oder \* .cur | Jede ANI- oder CUR-Datei (muss sich im gleichen Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden). |



 

## <a name="remarks"></a>Hinweise

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Wert beibehalten.

Cursordateinamenpfade werden ignoriert, sodass sich die Cursordatei im Standardverzeichnis befinden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONELEMENT-Element**](buttonelement-element.md)
</dt> </dl>

 

 





