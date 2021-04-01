---
description: Zum Erstellen eines Pfads und auswählen des Pfads in einen Domänen Controller müssen Sie zuerst die Punkte definieren, die ihn beschreiben.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Pfad Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215184"
---
# <a name="path-creation"></a>Pfad Erstellung

Zum Erstellen eines Pfads und auswählen des Pfads in einen Domänen Controller müssen Sie zuerst die Punkte definieren, die ihn beschreiben. Dies erfolgt durch Aufrufen der [**beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) -Funktion unter Angabe der entsprechenden Zeichnungsfunktionen und durch Aufrufen der [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) -Funktion. Diese Kombination von Funktionen (**beginpath**, Zeichnungsfunktionen und **endpath**) bilden eine *Pfad Klammer*. Im folgenden finden Sie eine Liste der Zeichnungsfunktionen, die verwendet werden können.

-   [**Anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**Exttextout**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**"Muvezu Ex"**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Kreis**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**Polybezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Polylinie**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**PolyLineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**Polypolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Polypolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Rollen**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Wenn eine Anwendung [**endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)aufruft, wählt das System den zugeordneten Pfad in den angegebenen Domänen Controller aus. (Wenn zuvor ein anderer Pfad in den Domänen Controller ausgewählt wurde, löscht das System diesen Pfad, ohne ihn zu speichern.) Nachdem das System den Pfad zum Domänen Controller ausgewählt hat, kann eine Anwendung auf eine der folgenden Arten mit dem Pfad arbeiten:

-   Zeichnen Sie den Umriss des Pfads (mit dem aktuellen Stift).
-   Zeichnen Sie das Innere des Pfads (mit dem aktuellen Pinsel).
-   Zeichnen Sie die Kontur, und füllen Sie das Innere des Pfads aus.
-   Ändern des Pfads (umwandeln von Kurven in Liniensegmente).
-   Konvertieren Sie den Pfad in einen Clip Pfad.
-   Konvertieren Sie den Pfad in einen Bereich.
-   Vereinfachen Sie den Pfad, indem Sie jede Kurve im Pfad in eine Reihe von Liniensegmenten umrechnen.
-   Rufen Sie die Koordinaten der Linien und Kurven ab, die einen Pfad bilden.

 

 



