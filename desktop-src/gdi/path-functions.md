---
description: Die folgenden Funktionen werden verwendet, um Pfade zu erstellen, zu ändern oder zu zeichnen.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Pfadfunktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700298056ac595b0e9208c0b8535d7a3d2e822e048e4c656d0b4501947764533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759426"
---
# <a name="path-functions-windows-gdi"></a>Pfadfunktionen (Windows GDI)

Die folgenden Funktionen werden verwendet, um Pfade zu erstellen, zu ändern oder zu zeichnen.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortPath**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Schließt alle Pfade im angegebenen Gerätekontext und verwirft sie.                                                                                                   |
| [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Öffnet eine Pfadklammer im angegebenen Gerätekontext.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Schließt eine geöffnete Figur in einem Pfad.                                                                                                                                 |
| [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Schließt eine Pfadklammer und wählt den durch die Klammer definierten Pfad im angegebenen Gerätekontext aus.                                                             |
| [**Fillpath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Schließt alle offenen Abbildungen im aktuellen Pfad und füllt das Innere des Pfads mithilfe des aktuellen Pinsels und des Polygonfüllmodus aus.                                   |
| [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Transformiert alle Kurven im ausgewählten Pfad in den aktuellen Gerätekontext (DC), und wandelt jede Kurve in eine Sequenz von Linien um.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Ruft den Mitergrenzwert für den angegebenen Gerätekontext ab.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Ruft die Koordinaten ab, die die Endpunkte von Linien und die Kontrollpunkte von Kurven definieren, die im Pfad gefunden werden, der im angegebenen Gerätekontext ausgewählt ist. |
| [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Erstellt einen Bereich aus dem Pfad, der im angegebenen Gerätekontext ausgewählt ist.                                                                               |
| [**SetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Legt den Grenzwert für die Länge von Miter-Joins für den angegebenen Gerätekontext fest.                                                                                   |
| [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Schließt alle offenen Abbildungen in einem Pfad, strichiert den Umriss des Pfads mithilfe des aktuellen Stifts und füllt sein Inneres mithilfe des aktuellen Pinsels.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Rendert den angegebenen Pfad mithilfe des aktuellen Stifts.                                                                                                             |
| [**WidenPath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Definiert den aktuellen Pfad als den Bereich neu, der gestrichelt wird, wenn der Pfad mithilfe des aktuell im angegebenen Gerätekontext ausgewählten Stifts gestrichelt wird.            |



 

 

 



