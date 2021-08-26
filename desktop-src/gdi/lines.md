---
description: 'Eine Linie ist ein Satz hervorgehobener Pixel auf einer Rasteranzeige (oder eine Reihe von Punkten auf einer gedruckten Seite), die durch zwei Punkte identifiziert werden: einen Ausgangspunkt und einen Endpunkt.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Linien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b81976984cecc3d4d3b27fb3e474e896c6e81f03e6f601db36418b9e3cf197c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062100"
---
# <a name="lines"></a>Linien

Eine Linie ist ein Satz hervorgehobener Pixel auf einer Rasteranzeige (oder eine Reihe von Punkten auf einer gedruckten Seite), die durch zwei Punkte identifiziert werden: einen Ausgangspunkt und einen Endpunkt. Das Pixel, das sich am Anfangspunkt befindet, ist immer in der Zeile enthalten, und das Pixel am Endpunkt wird immer ausgeschlossen. (Diese Art von Zeile wird manchmal auch als inklusiv-exklusiv bezeichnet.)

Wenn eine Anwendung eine der Linienzeichnungsfunktionen aufruft, bestimmt die Grafikgeräteschnittstelle (GDI) oder in einigen Fällen ein Gerätetreiber, welche Pixel hervorgehoben werden sollen. GDI ist eine Dll (Dynamic Link Library), die Grafikfunktionsaufrufe von einer Anwendung verarbeitet und diese Aufrufe an einen Gerätetreiber übergibt. Ein Gerätetreiber ist eine DLL, die Eingaben von GDI empfängt, die Eingabe in Gerätebefehle konvertiert und diese Befehle an das entsprechende Gerät übergibt. GDI verwendet ein digitales differenzielles Analysegerät (Digital Differential Analyzer, DDA), um den Satz von Pixeln zu bestimmen, die eine Linie definieren. Ein DDA bestimmt den Satz von Pixeln, indem er jeden Punkt in der Linie untersucht und die Pixel auf der Anzeigeoberfläche (oder Punkte auf einer gedruckten Seite) identifiziert, die den Punkten entsprechen. Die folgende Abbildung zeigt eine Linie, ihren Ausgangspunkt, ihren Endpunkt und die mithilfe eines einfachen DDA hervorgehobenen Pixel.

![Abbildung eines Rasters aus Pixeln, Start- und Endpunkten, einer Linie und Schattierung auf den Pixeln, die entlang der Linie liegen](images/cslcv-01.png)

Der einfachste und gängigste DDA ist der Bresenham-DDA(inkrementell). Eine geänderte Version dieses Algorithmus zeichnet Linien in Windows. Der inkrementelle DDA ist der Einfachheit halber bekannt, aber auch seine Ungenauigkeit. Da er auf den nächsten ganzzahligen Wert aufgerundet wird, kann er manchmal nicht die ursprüngliche Zeile darstellen, die von der Anwendung angefordert wird. Der von GDI verwendete DDA wird nicht auf die nächste ganze Zahl aufgerundet. Daher erzeugt dieser neue DDA eine Ausgabe, die manchmal viel näher an der ursprünglichen Zeile liegt, die von der Anwendung angefordert wird.

> [!Note]  
> Wenn eine Anwendung eine Zeilenausgabe erfordert, die mit dem neuen DDA nicht erreicht werden kann, kann sie eigene Zeilen zeichnen, indem sie die [**LineDDA-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) aufruft und einen privaten DDA [**(LineDDAProc) anfordert.**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc) Die **LineDDA-Funktion** zeichnet jedoch Linien viel langsamer als die Linienzeichnungsfunktionen. Verwenden Sie diese Funktion nicht innerhalb einer Anwendung, wenn die Geschwindigkeit ein hauptanliegend ist.

 

Eine Anwendung kann den neuen DDA verwenden, um einzelne Linien und mehrere verbundene Liniensegmente zu zeichnen. Eine Anwendung kann eine einzelne Linie zeichnen, indem sie die [**LineTo-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) aufruft. Diese Funktion zeichnet eine Linie von der aktuellen Position bis zu einem angegebenen Endpunkt, jedoch nicht einschließlich. Eine Anwendung kann eine Reihe verbundener Liniensegmente zeichnen, indem die [**Polyline-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) aufruft und ein Array von Punkten angegeben wird, die den Endpunkt jedes Liniensegments angeben. Eine Anwendung kann mehrere, nicht verbundene Reihen verbundener Liniensegmente zeichnen, indem sie die [**PolyPolyline-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) aufruft und die erforderlichen Endpunkte liefert.

Die folgende Abbildung zeigt die Zeilenausgabe, die durch Aufrufen der [**Funktionen LineTo,**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)und [**PolyPolyline erstellt**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) wurde.

![Abbildung mit einer geraden Linie, einem l-förmigen Feld und zwei formen, die dreidimensional angezeigt werden](images/cslcv-02.png)

 

 



