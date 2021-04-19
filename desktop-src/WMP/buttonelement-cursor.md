---
title: ButtonElement. Cursor
description: Das Cursor Attribut gibt den Wert des ButtonElement-Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem ButtonElement befindet.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- ButtonElement. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374035"
---
# <a name="buttonelementcursor"></a>ButtonElement. Cursor

Das **Cursor** Attribut gibt den Wert des **ButtonElement** -Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich der Mauszeiger über dem **ButtonElement** befindet.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.



| Wert            | Beschreibung                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| System           | Standard. Platt Form abhängiger Cursor (in der Regel ein Pfeil).                                      |
| linken             | Linken.                                                                                       |
| help             | Pfeil mit Fragezeichen, das angibt, dass Hilfe verfügbar ist.                                      |
| SizeAll          | Vierstufige Pfeil, der nach Norden, Süden, Osten und Westen zeigt.                                   |
| sizenesw         | Ein Pfeil mit zwei Spitzen, der auf Nordost und Südwest zeigt.                                      |
| SizeNS           | Ein Pfeil mit zwei Spitzen, der nach Norden und Süden zeigt.                                              |
| sizenwse         | Ein Pfeil mit zwei Spitzen, der auf Nordwest und Südost zeigt.                                      |
| SizeWE           | Ein Pfeil mit zwei Spitzen, der nach Westen und Osten zeigt.                                                |
| oben          | Vertikaler Pfeil nach oben.                                                             |
| \*. ani oder \* . cur | Alle. ani-oder. cur-Dateien (müssen sich in demselben Verzeichnis wie die WMS-Datei oder in der WMZ-Datei befinden). |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Wert beibehalten.

Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonElement-Element**](buttonelement-element.md)
</dt> </dl>

 

 





