---
description: Die folgenden Funktionen werden verwendet, um Pfade zu erstellen, zu ändern oder zu zeichnen.
ms.assetid: 68390601-1542-41dc-bea0-78f6c3318806
title: Path-Funktionen (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab85e52392b3e600877f8f5adac08d5de77e873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978448"
---
# <a name="path-functions-windows-gdi"></a>Path-Funktionen (Windows GDI)

Die folgenden Funktionen werden verwendet, um Pfade zu erstellen, zu ändern oder zu zeichnen.



| Funktion                                       | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbruch Pfad**](/windows/desktop/api/Wingdi/nf-wingdi-abortpath)                 | Schließt und verwirft alle Pfade im angegebenen Gerätekontext.                                                                                                   |
| [**Beginpath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath)                 | Öffnet eine Pfad Klammer im angegebenen Gerätekontext.                                                                                                            |
| [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)             | Schließt eine geöffnete Figur in einem Pfad.                                                                                                                                 |
| [**Endpath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath)                     | Schließt eine Pfad Klammer und wählt den von der Klammer definierten Pfad im angegebenen Gerätekontext aus.                                                             |
| [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath)                   | Schließt alle geöffneten Abbildungen im aktuellen Pfad und füllt das Innere des Pfads mit dem aktuellen Pinsel und dem Polygon Füll Modus aus.                                   |
| [**Vereinfachder Pfad**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath)             | Wandelt alle Kurven im ausgewählten Pfad in den aktuellen Gerätekontext (DC) um und wandelt jede Kurve in eine Sequenz von Zeilen um.                            |
| [**GetMiterLimit**](/windows/desktop/api/Wingdi/nf-wingdi-getmiterlimit)         | Ruft das miterLimit für den angegebenen Gerätekontext ab.                                                                                                      |
| [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath)                     | Ruft die Koordinaten ab, die die Endpunkte von Linien und die Steuerungs Punkte der Kurven definieren, die in dem Pfad gefunden werden, der im angegebenen Gerätekontext ausgewählt ist. |
| [**Pathrenegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion)           | Erstellt einen Bereich aus dem Pfad, der im angegebenen Gerätekontext ausgewählt wird.                                                                               |
| [**Setmiterlimit**](/windows/desktop/api/Wingdi/nf-wingdi-setmiterlimit)         | Legt den Grenzwert für die Länge von Gehrungs-Joins für den angegebenen Gerätekontext fest.                                                                                   |
| [**Strokeandfillpath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) | Schließt alle geöffneten Abbildungen in einem Pfad, streift die Gliederung des Pfads mithilfe des aktuellen Stifts und füllt das Innere mit dem aktuellen Pinsel.                  |
| [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath)               | Rendert den angegebenen Pfad mit dem aktuellen Stift.                                                                                                             |
| [**Widenpath**](/windows/desktop/api/Wingdi/nf-wingdi-widenpath)                 | Definiert den aktuellen Pfad neu als den Bereich, der gezeichnet werden würde, wenn der Pfad mithilfe des derzeit im angegebenen Gerätekontext ausgewählten Stifts gezeichnet würde.            |



 

 

 



