---
description: Die folgenden Funktionen werden beim Zeichnen und Zeichnen verwendet.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Zeichnungs-und Zeichnungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162ce40c88766a81320f72ea7c2e4a84dd92c478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978481"
---
# <a name="painting-and-drawing-functions"></a>Zeichnungs-und Zeichnungsfunktionen

Die folgenden Funktionen werden beim Zeichnen und Zeichnen verwendet.



| Funktion                                       | BESCHREIBUNG                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Bereitet ein Fenster für die Zeichnung vor.                                                                             |
| [**Drawanimatedrects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Zeichnet ein Rechteck und animiert es, um ein Symbol oder eine Fenster Aktivität anzugeben.                                      |
| [**Drawcaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Zeichnet eine Fenster Beschriftung.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Zeichnet einen oder mehrere Kanten des Rechtecks.                                                                       |
| [**DrawFocus-Rect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Zeichnet ein Rechteck im Stil, das angibt, dass das Rechteck den Fokus besitzt.                                  |
| [**Drawframecontrol**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Zeichnet ein Frame-Steuerelement.                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Zeigt ein Bild an und wendet einen visuellen Effekt an, um einen Zustand anzugeben.                                          |
| [**Drawstateproc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Eine Rückruffunktion, die ein komplexes Bild für [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)rendert.                        |
| [**Endpaint auf**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Markiert das Ende des Bildes in einem Fenster.                                                                      |
| [**Excluentupdatergn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Verhindert das Zeichnen innerhalb von ungültigen Bereichen eines Fensters.                                                          |
| [**Gdiflush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Leert den aktuellen Batch des aufrufenden Threads.                                                                 |
| [**Gdigetbatchlimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Gibt die maximale Anzahl von Funktionsaufrufen zurück, die im aktuellen Batch des aufrufenden Threads gesammelt werden können. |
| [**Gdisetbatchlimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Legt die maximale Anzahl von Funktionsaufrufen fest, die im aktuellen Batch des aufrufenden Threads gesammelt werden können.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Gibt die Hintergrundfarbe für einen Gerätekontext zurück.                                                          |
| [**Getbkmode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Gibt den Hintergrund Mischungs Modus für einen Gerätekontext zurück.                                                       |
| [**Getboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Ruft das akkumulierte umgebende Rechteck für einen Gerätekontext ab.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Ruft den Vordergrund Mischungs Modus eines Geräte Kontexts ab.                                                           |
| [**Getupdaterierten**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Ruft die Koordinaten des kleinsten Rechtecks ab, das den Aktualisierungs Bereich eines Fensters einschließt.                 |
| [**Getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Ruft den Aktualisierungs Bereich eines Fensters ab.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Ruft den Gerätekontext für ein Fenster ab, einschließlich Titelleiste, Menüs und Bild Lauf leisten.                          |
| [**Getwindowrgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Ruft eine Kopie des Fenster Bereichs eines Fensters ab.                                                               |
| [**Getwindowrgnbox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Ruft die Dimensionen des Begrenzungs Rechtecks für den Fensterbereich eines Fensters ab.                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Zeichnet grauen Text an einem Speicherort.                                                                              |
| [**Invalidateruieren**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Fügt dem Aktualisierungs Bereich eines Fensters ein Rechteck hinzu.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Macht den Client Bereich innerhalb einer Region ungültig.                                                                |
| [**Lockwindowupdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Deaktiviert oder aktiviert das Zeichnen in einem Fenster.                                                                    |
| [**Outputproc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Eine Rückruffunktion, die mit der [**graystring**](/windows/desktop/api/Winuser/nf-winuser-graystringa) -Funktion verwendet wird. Sie wird verwendet, um eine Zeichenfolge zu zeichnen.   |
| [**Paintdesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Füllt den Clippingbereich in einem Gerätekontext mit einem Muster.                                               |
| [**Redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Aktualisiert einen Bereich im Client Bereich eines Fensters.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Legt den Hintergrund auf einen Farbwert fest.                                                                       |
| [**Setbkmode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Legt den Hintergrund Mischungs Modus eines Geräte Kontexts fest.                                                           |
| [**Setboundsrect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Steuert die Ansammlung von umgebenden Rechteck Informationen für einen Gerätekontext.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Legt den Vordergrund-Mischungs Modus fest.                                                                               |
| [**Setwindowrgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Legt den Fensterbereich eines Fensters fest.                                                                         |
| [**Update Window**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Aktualisiert den Client Bereich eines Fensters.                                                                        |
| [**Validaterierten**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Überprüft den Client Bereich innerhalb eines Rechtecks.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Überprüft den Client Bereich innerhalb einer Region.                                                                  |
| [**Windowfromdc**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Gibt ein Handle für das Fenster zurück, das einem Gerätekontext zugeordnet ist.                                            |



 

 

 



