---
title: Button. Cursor
description: Das Cursor Attribut gibt den Cursor an oder ruft ihn ab, der angezeigt wird, wenn der Mauszeiger über die Schaltfläche bewegt wird.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Button. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2641491a5a73498da2c43fd74d4187b5594e177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356428"
---
# <a name="buttoncursor"></a>Button. Cursor

Das **Cursor** Attribut gibt den Cursor an oder ruft ihn ab, der angezeigt wird, wenn der Mauszeiger über die **Schaltfläche** bewegt wird.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert            | Beschreibung                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| System           | Standard. Platt Form abhängiger Cursor (in der Regel ein Pfeil).                                     |
| linken             | Linken.                                                                                      |
| help             | Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.                                     |
| SizeAll          | Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.                                  |
| sizenesw         | Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.                                     |
| SizeNS           | Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.                                             |
| sizenwse         | Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.                                     |
| SizeWE           | Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.                                               |
| oben          | Vertikaler Pfeil nach oben.                                                            |
| \*. ani oder \* . cur | Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden) |



 

## <a name="remarks"></a>Bemerkungen

Wenn das System den angegebenen Cursor Wert nicht erkennt, verbleibt der Cursor Wert am zuvor festgelegten Wert.

Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> </dl>

 

 





