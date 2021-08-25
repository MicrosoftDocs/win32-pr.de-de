---
description: 'Eine Anwendung kann sechs Funktionen verwenden, um die Textformatierungsattribute für einen Gerätekontext festzulegen: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor und SetTextJustification.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Text-Formatting Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e74cb8d30a0eb9b44f05be611da963b413e8798b81da2a334dc083bd3cc1651
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015280"
---
# <a name="text-formatting-attributes"></a>Text-Formatting Attribute

Eine Anwendung kann sechs Funktionen verwenden, um die Textformatierungsattribute für einen Gerätekontext festzulegen: [SetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) [SetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) [SetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) [SetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)und [SetTextJustification.](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) Diese Funktionen wirken sich auf die Textausrichtung, den Abstand des Interzeichens, die Textausrichtung sowie Text- und Hintergrundfarben aus. Darüber hinaus können sechs weitere Funktionen verwendet werden, um die aktuellen Textformatierungsattribute für jeden Gerätekontext abzurufen: [GetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) [GetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) [GetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) [GetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)und [GetTextExtentPoint32.](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)

## <a name="text-alignment"></a>Textausrichtung

Anwendungen können die [SetTextAlign-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) verwenden, um anzugeben, wie das System die Zeichen in einer Textzeichenfolge positionieren soll, wenn sie eine der Zeichnungsfunktionen aufrufen. Diese Funktion kann verwendet werden, um Überschriften, Seitenzahlen, Aufrufe usw. zu positionieren. Das System positioniert eine Textzeichenfolge durch Ausrichten eines Verweispunkts auf einem imaginären Rechteck, das die Zeichenfolge umgibt, mit der aktuellen Cursorposition oder mit einem Punkt, der als Argument an eine der Textzeichnungsfunktionen übergeben wird. Mit der [**SetTextAlign-Funktion**](/windows/win32/api/wingdi/nf-wingdi-settextalign) kann die Anwendung den Speicherort dieses Referenzpunkts angeben. Im Folgenden sind die möglichen Referenzpunktpositionen aufgeführt.



| Standort         | BESCHREIBUNG                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| links/unten      | Der Verweispunkt befindet sich in der unteren linken Ecke des Rechtecks.                                               |
| linke/Basislinie   | Der Verweispunkt befindet sich an der Schnittmenge der Basislinie der Zeichenzelle und am linken Rand des Rechtecks.  |
| links/oben         | Der Verweispunkt befindet sich in der oberen linken Ecke des Rechtecks.                                                 |
| Mitte/Unten    | Der Verweispunkt befindet sich in der Mitte des unteren Rands des Rechtecks.                                            |
| Mitte/Basislinie | Der Verweispunkt befindet sich an der Schnittmenge der Basislinie der Zeichenzelle und der Mitte des Rechtecks.     |
| Center/Top       | Der Verweispunkt befindet sich in der Mitte des oberen Rands des Rechtecks.                                               |
| rechts/unten     | Der Verweispunkt befindet sich in der unteren rechten Ecke des Rechtecks.                                              |
| rechte/Basislinie  | Der Verweispunkt befindet sich an der Schnittmenge der Basislinie der Zeichenzelle und am rechten Rand des Rechtecks. |
| rechts/oben        | Der Verweispunkt befindet sich in der oberen rechten Ecke des Rechtecks.                                                |



 

Die folgende Abbildung zeigt eine Zeichenfolge mit Text, die durch Aufrufen der [TextOut-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-textouta) gezeichnet wurde. Vor dem Zeichnen des Texts wurde die [SetTextAlign-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) aufgerufen, um den Verweispunkt an jeder der neun möglichen Positionen zu verschieben.

![Abbildung, die neunmal den gleichen Text zeigt, einen für jede mögliche Referenzpunktposition](images/csftx-04.png)

Die Standardtextausrichtung für einen Gerätekontext ist die obere linke Ecke des imaginären Rechtecks, das den Text umgibt. Eine Anwendung kann die aktuelle Textausrichtungseinstellung für jeden Gerätekontext abrufen, indem sie die [GetTextAlign-Funktion aufruft.](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)

## <a name="intercharacter-spacing"></a>Intercharacter-Abstand

Anwendungen können die [SetTextCharacterExtra-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) verwenden, um den Interzeichenabstand für alle Textausgabevorgänge in einem angegebenen Gerätekontext zu ändern. Die folgende Abbildung zeigt eine Zeichenfolge mit Text, die zweimal durch Aufrufen der [TextOut-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-textouta) gezeichnet wurde. Vor dem zweiten Zeichnen des Texts wurde die [**SetTextCharacterExtra-Funktion**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) aufgerufen, um den Abstand zwischen Zeichen zu erhöhen.

![Abbildung, in der derselbe Text zweimal angezeigt wird: zuerst mit normalem Interzeichenabstand, dann mit größerem Abstand](images/csftx-06.png)

Der Standardmäßige Intercharacter-Abstandswert für jeden Gerätekontext ist 0 (null). Eine Anwendung kann den aktuellen Intercharacter-Abstandswert für einen Gerätekontext abrufen, indem sie die [GetTextCharacterExtra-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) aufruft.

## <a name="text-justification"></a>Text-Begründung

Anwendungen können die Funktionen [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) und [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) verwenden, um eine Textzeile zu rechtfertigen. Die Textgrundlage ist ein gängiger Vorgang in jeder Desktopveröffentlichung und in den meisten Textverarbeitungsanwendungen. Die [**GetTextExtentPoint32-Funktion**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) berechnet die Breite und Höhe einer Textzeichenfolge. Nachdem die Breite berechnet wurde, kann die Anwendung die [**SetTextJustification-Funktion**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) aufrufen, um zusätzliche Abstände zwischen den einzelnen Wörtern in einer Textzeile zu verteilen. Die folgende Abbildung zeigt einen Absatz von Text, der zweimal gedruckt wird: Im ersten Absatz wurde der Text nicht gerechtfertigt. Im zweiten Absatz wurde der Text durch Aufrufen der Funktionen **GetTextExtentPoint32** und **SetTextJustification** gerechtfertigt.

![Abbildung eines Absatzes, der nur links und dann links und rechts ausgerichtet ist](images/csftx-05.png)

## <a name="text-and-background-color"></a>Text- und Hintergrundfarbe

Anwendungen können die [SetTextColor-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) verwenden, um die Farbe des im Clientbereich der Fenster gezeichneten Texts sowie die Farbe des Texts festzulegen, der auf einem Farbdrucker gezeichnet wird. Eine Anwendung kann die [SetBkColor-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) verwenden, um die Farbe festzulegen, die hinter jedem Zeichen angezeigt wird, und die [SetBkMode-Funktion,](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) um anzugeben, wie das System die ausgewählte Hintergrundfarbe mit der aktuellen Farbe oder den aktuellen Farben auf der Videoanzeige kombinieren soll.

Die Standardtextfarbe für einen Anzeigegerätekontext ist schwarz. Die Standardhintergrundfarbe ist weiß. und der Standardhintergrundmodus ist OPAQUE. Eine Anwendung kann die aktuelle Textfarbe für einen Gerätekontext abrufen, indem sie die [GetTextColor-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) aufruft. Eine Anwendung kann die aktuelle Hintergrundfarbe für einen Gerätekontext abrufen, indem sie die [GetBkColor-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) und den aktuellen Hintergrundmodus aufruft, indem sie die [GetBkMode-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) aufruft.

 

 
