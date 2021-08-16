---
description: Die folgenden Funktionen werden zum Erstellen, Ändern oder Zeichnen von Pfaden verwendet.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Path Functions (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700298056ac595b0e9208c0b8535d7a3d2e822e048e4c656d0b4501947764533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759426"
---
# <a name="path-functions-windows-gdi"></a>Path Functions (Windows GDI)

Die folgenden Funktionen werden zum Erstellen, Ändern oder Zeichnen von Pfaden verwendet.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Schließt alle Pfade im angegebenen Gerätekontext und verwirft sie.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Öffnet eine Pfadklammer im angegebenen Gerätekontext.                                                                                                            |
| [**SchließenAbbildung**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Schließt eine geöffnete Figur in einem Pfad.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Schließt eine Pfadklammer und wählt den durch die Klammer definierten Pfad in den angegebenen Gerätekontext aus.                                                             |
| [**Fillpath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Schließt alle offenen Abbildungen im aktuellen Pfad und füllt das Innere des Pfads mithilfe des aktuellen Pinsel- und Polygonfüllmodus aus.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transformiert alle Kurven im ausgewählten Pfad in den aktuellen Gerätekontext (DC) und wandelt jede Kurve in eine Sequenz von Linien um.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Ruft den Grenzwert für den angegebenen Gerätekontext ab.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Ruft die Koordinaten ab, die die Endpunkte von Linien und die Kontrollpunkte von Kurven definieren, die sich im Pfad befinden, der im angegebenen Gerätekontext ausgewählt ist. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Erstellt einen Bereich aus dem Pfad, der im angegebenen Gerätekontext ausgewählt ist.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Legt den Grenzwert für die Länge von Miter-Joins für den angegebenen Gerätekontext fest.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Schließt alle offenen Abbildungen in einem Pfad, stricht die Kontur des Pfads mithilfe des aktuellen Stifts und füllt das Innere mithilfe des aktuellen Pinsels aus.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Rendert den angegebenen Pfad mithilfe des aktuellen Stifts.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Definiert den aktuellen Pfad als Bereich neu, der gezeichnet würde, wenn der Pfad mit dem Stift gezeichnet würde, der derzeit im angegebenen Gerätekontext ausgewählt ist.            |



 

 

 



