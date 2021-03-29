---
description: 'Eine Linie ist ein Satz hervorgehobener Pixel in einem Raster Display (oder einer Gruppe von Punkten auf einer gedruckten Seite), die durch zwei Punkte identifiziert werden: ein Anfangspunkt und ein Endpunkt.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Linien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215193"
---
# <a name="lines"></a>Linien

Eine Linie ist ein Satz hervorgehobener Pixel in einem Raster Display (oder einer Gruppe von Punkten auf einer gedruckten Seite), die durch zwei Punkte identifiziert werden: ein Anfangspunkt und ein Endpunkt. Das Pixel am Ausgangspunkt ist immer in der Zeile enthalten, und das Pixel am Endpunkt wird immer ausgeschlossen. (Diese Art von Zeile wird manchmal als inklusiv bezeichnet.)

Wenn eine Anwendung eine der Zeilen Zeichnungsfunktionen aufruft (Graphics Device Interface, GDI), oder in einigen Fällen ein Gerätetreiber, bestimmt, welche Pixel hervorgehoben werden sollen. GDI ist eine Dynamic Link Library (dll), die Grafik Funktionsaufrufe von einer Anwendung verarbeitet und diese Aufrufe an einen Gerätetreiber übergibt. Ein Gerätetreiber ist eine DLL, die eine Eingabe aus GDI empfängt, die Eingabe in Geräte Befehle konvertiert und diese Befehle an das entsprechende Gerät übergibt. GDI verwendet einen Digital Differential Analyzer (DDA), um den Satz von Pixeln zu ermitteln, die eine Linie definieren. Ein DDA bestimmt den Satz von Pixeln, indem jeder Punkt in der Zeile überprüft und die Pixel auf der Anzeige Oberfläche (oder Punkte auf einer gedruckten Seite) identifiziert werden, die den Punkten entsprechen. In der folgenden Abbildung werden eine Linie, Ihr Anfangspunkt, Ihr Endpunkt und die Pixel, die mithilfe eines einfachen DDA hervorgehoben werden, gezeigt.

![Abbildung mit einem Raster von Pixeln, Anfangs-und Endpunkten, einer Linie und Schattierung in den Pixeln, die entlang der Linie liegen](images/cslcv-01.png)

Der einfachste und häufigste DDA ist der Bresenham-oder inkrementelle DDA. Eine geänderte Version dieses Algorithmus zeichnet Zeilen in Windows. Der inkrementelle DDA ist aus Gründen der Einfachheit zu beachten, aber er ist auch für seine Ungenauigkeit vermerkt. Da der Wert auf den nächstgelegenen ganzzahligen Wert gerundet wird, kann er manchmal nicht die ursprüngliche von der Anwendung angeforderte Zeile darstellen. Der von GDI verwendete DDA ist nicht auf die nächste ganze Zahl gerundet. Folglich erzeugt dieser neue DDA Ausgaben, die in der ursprünglichen, von der Anwendung angeforderten Zeile vorkommen.

> [!Note]  
> Wenn eine Anwendung eine Zeilen Ausgabe erfordert, die nicht mit dem neuen DDA erreicht werden kann, können Sie Ihre eigenen Zeilen zeichnen, indem Sie die [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) -Funktion aufrufen und eine private DDA ([**lineddaproc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)) bereitstellen. Die **LineDDA** -Funktion zeichnet jedoch Zeilen, die viel langsamer als die Zeilen Zeichnungsfunktionen sind. Verwenden Sie diese Funktion nicht in einer Anwendung, wenn die Geschwindigkeit ein primäres Problem ist.

 

Eine Anwendung kann den neuen DDA zum Zeichnen einzelner Zeilen und mehrerer verbundener Liniensegmente verwenden. Eine Anwendung kann eine einzelne Zeile zeichnen [**, indem Sie die LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) -Funktion aufrufen. Diese Funktion zeichnet eine Linie von der aktuellen Position bis zum, jedoch nicht einschließlich, eines angegebenen Endpunkts. Eine Anwendung kann eine Reihe verbundener Liniensegmente zeichnen, indem Sie die [**polylinienfunktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) aufrufen und ein Array von Punkten bereitstellt, die den Endpunkt der einzelnen Zeilen Segmente angeben. Eine Anwendung kann mehrere, separate Zeilen Segmente zeichnen, indem Sie die [**polypolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) -Funktion aufrufen und die erforderlichen Endpunkte bereitstellt.

Die folgende Abbildung zeigt die Zeilen Ausgabe, die durch Aufrufen der Funktionen [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)und [**polypolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) erstellt wurde.

![Abbildung, die eine gerade Linie, ein "l"-geformtes Feld und zwei Formen anzeigt, die dreidimensional erscheinen](images/cslcv-02.png)

 

 



