---
title: ButtonGroup. Cursor
description: Das Cursor Attribut gibt den Typ des Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über einer Schaltfläche in der ButtonGroup befindet.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- ButtonGroup. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371186"
---
# <a name="buttongroupcursor"></a>ButtonGroup. Cursor

Das **Cursor** Attribut gibt den Typ des Cursors an oder ruft ihn ab, der angezeigt wird, wenn sich die Maus über einer Schaltfläche in der **ButtonGroup** befindet.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.



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

Der angegebene Cursor gilt für alle Schaltflächen in der **ButtonGroup**.

Wenn Sie einen ungültigen Cursor Wert angeben, verbleibt er am zuvor festgelegten Wert.

Cursor-Dateinamen Pfade werden ignoriert, sodass sich die Cursor Datei im Standardverzeichnis befinden muss.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> </dl>

 

 





