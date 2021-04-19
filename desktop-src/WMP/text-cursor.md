---
title: Text. Cursor
description: Mit dem Cursor Attribut wird ein Wert angegeben oder abgerufen, der angibt, welcher Cursor angezeigt wird, wenn sich die Maus über dem Text Steuerelement befindet.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Text. Cursor-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373631"
---
# <a name="textcursor"></a>Text. Cursor

Mit dem **Cursor** Attribut wird ein Wert angegeben oder abgerufen, der angibt, welcher Cursor angezeigt wird, wenn sich die Maus über dem Text Steuerelement befindet.

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



 

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> </dl>

 

 





