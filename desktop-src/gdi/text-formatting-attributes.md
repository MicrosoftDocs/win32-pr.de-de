---
description: 'Eine Anwendung kann sechs Funktionen verwenden, um die Text Formatierungs Attribute für einen Gerätekontext festzulegen: SetBkColor, setbkmode, setTextAlign, settextcharakteriextra, SetTextColor und settextbegrün dung.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Text-Formatting Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d345bfcfe1693a7ff0b25bb323615dffe221ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561270"
---
# <a name="text-formatting-attributes"></a>Text-Formatting Attribute

Eine Anwendung kann sechs Funktionen verwenden, um die Text Formatierungs Attribute für einen Gerätekontext festzulegen: [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor), [setbkmode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode), [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign), [settextcharakteriextra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra), [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)und [settextbegrün dung](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification). Diese Funktionen beeinflussen die Textausrichtung, den Abstand zwischen Zeichen, die Textausrichtung und Text-und Hintergrundfarben. Außerdem können sechs weitere Funktionen verwendet werden, um die aktuellen Text Formatierungs Attribute für jeden Gerätekontext abzurufen: [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor), [getbkmode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode), [gettextalign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign), [gettextcharakteriextra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra), [gettextcolor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)und [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a).

## <a name="text-alignment"></a>Textausrichtung

Anwendungen können die [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) -Funktion verwenden, um anzugeben, wie das System die Zeichen in einer Text Zeichenfolge positionieren soll, wenn Sie eine der Zeichnungsfunktionen aufrufen. Diese Funktion kann verwendet werden, um Überschriften, Seitenzahlen, Legenden usw. zu positionieren. Das System positioniert eine Text Zeichenfolge durch Ausrichten eines Bezugspunkts an einem imaginären Rechteck, das die Zeichenfolge umgibt, mit der aktuellen Cursorposition oder mit einem Punkt, der als Argument an eine der Text Zeichnungsfunktionen weitergegeben wird. Mit der [**setTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) -Funktion kann die Anwendung den Speicherort dieses Bezugspunkts angeben. Im folgenden finden Sie eine Liste der möglichen Bezugspunkt Positionen.



| Standort         | BESCHREIBUNG                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| Links/unten      | Der Bezugspunkt befindet sich in der unteren linken Ecke des Rechtecks.                                               |
| Links/Basislinie   | Der Bezugspunkt befindet sich an der Schnittmenge der Zeichen Zellen-Basislinie und der linken Kante des Rechtecks.  |
| Links/oben         | Der Bezugspunkt befindet sich in der linken oberen Ecke des Rechtecks.                                                 |
| zentriert/unten    | Der Bezugspunkt befindet sich in der Mitte des Rechtecks.                                            |
| zentrieren/Basislinie | Der Bezugspunkt befindet sich an der Schnittmenge der Zeichen Zellen-Basislinie und der Mitte des Rechtecks.     |
| zentriert/oben       | Der Bezugspunkt befindet sich in der Mitte des oberen Rands des Rechtecks.                                               |
| rechts/unten     | Der Bezugspunkt befindet sich in der unteren rechten Ecke des Rechtecks.                                              |
| rechts/Basislinie  | Der Bezugspunkt befindet sich an der Schnittmenge der Zeichen Zellen-Basislinie und der rechten Kante des Rechtecks. |
| rechts/oben        | Der Bezugspunkt befindet sich in der oberen rechten Ecke des Rechtecks.                                                |



 

Die folgende Abbildung zeigt eine Text Zeichenfolge, die durch Aufrufen der [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion gezeichnet wird. Vor dem Zeichnen des Texts wurde die Funktion " [setTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) " aufgerufen, um den Bezugspunkt an jedem der neun möglichen Orte zu verschieben.

![die Abbildung zeigt neun Mal denselben Text, einen für jeden möglichen Verweis Punkt Speicherort.](images/csftx-04.png)

Die Standardtext Ausrichtung für einen Gerätekontext ist die linke obere Ecke des imaginären Rechtecks, das den Text umgibt. Eine Anwendung kann die aktuelle Einstellung für die Textausrichtung für beliebige Geräte Kontexte abrufen, indem Sie die [gettextalign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) -Funktion aufrufen.

## <a name="intercharacter-spacing"></a>Intercharacter-Abstand

Anwendungen können die Funktion " [settextcharacter extra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) " verwenden, um den zwischen Raum von Textausgabe Vorgängen in einem angegebenen Gerätekontext zu ändern. Die folgende Abbildung zeigt eine Text Zeichenfolge, die zweimal durch Aufrufen der [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) -Funktion gezeichnet wird. Bevor der Text beim zweiten Mal gezeichnet wird, wurde die Funktion [**settextcharacter extra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) aufgerufen, um den intercharacter-Abstand zu erhöhen.

![zweimaliges durchlaufen desselben Texts: zuerst mit normalem Zeichenabstand, dann mit größerem Abstand](images/csftx-06.png)

Der standardmäßige intercharacter-Abstands Wert für alle Geräte Kontexte ist 0 (null). Eine Anwendung kann den aktuellen intercharacter-Abstands Wert für einen Gerätekontext abrufen, indem die [gettextcharakteriextra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) -Funktion aufgerufen wird.

## <a name="text-justification"></a>Text Ausrichtung

Anwendungen können eine Textzeile mithilfe der Funktionen [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) und [settextbegrün dung](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) rechtfertigen. Die Text Ausrichtung ist ein gängiger Vorgang bei jeder Desktop Veröffentlichung und in den meisten Textverarbeitungsanwendungen. Die [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion berechnet die Breite und Höhe einer Text Zeichenfolge. Nachdem die Breite berechnet wurde, kann die Anwendung die [**settextspecification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) -Funktion aufrufen, um den zusätzlichen Abstand zwischen den Wörtern in einer Textzeile zu verteilen. Die folgende Abbildung zeigt einen Absatz von Text, der zweimal gedruckt wurde: im ersten Absatz wurde der Text nicht gerechtfertigt. im zweiten Absatz wurde der Text durch Aufrufen der Funktionen **GetTextExtentPoint32** und **settextbegrün dung** gerechtfertigt.

![die Abbildung zeigt einen Absatz, der sich nur auf der linken Seite richtet, dann den gleichen Absatz auf der linken und rechten Seite.](images/csftx-05.png)

## <a name="text-and-background-color"></a>Text und Hintergrundfarbe

Anwendungen können die [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) -Funktion verwenden, um die Farbe des Texts, der im Client Bereich ihrer Fenster gezeichnet wird, sowie die Farbe des Texts, der auf einem Farbdrucker gezeichnet wird, festzulegen. Eine Anwendung kann die [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) -Funktion verwenden, um die Farbe festzulegen, die hinter jedem Zeichen angezeigt wird, und die [setbkmode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) -Funktion, um anzugeben, wie das System die ausgewählte Hintergrundfarbe mit der aktuellen Farbe oder den Farben in der Videoanzeige vermischen soll.

Die Standard Textfarbe für einen Anzeigegeräte Kontext ist schwarz. die Standard Hintergrundfarbe ist weiß. und der Standard Hintergrundmodus ist nicht transparent. Eine Anwendung kann die aktuelle Textfarbe für einen Gerätekontext abrufen, indem Sie die [gettextcolor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) -Funktion aufrufen. Eine Anwendung kann die aktuelle Hintergrundfarbe für einen Gerätekontext abrufen, indem Sie die [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) -Funktion und den aktuellen Hintergrundmodus durch Aufrufen der [getbkmode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) -Funktion aufrufen.

 

 
