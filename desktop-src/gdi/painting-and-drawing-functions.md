---
description: Die folgenden Funktionen werden beim Zeichnen und Zeichnen verwendet.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Zeichnen und Zeichnen von Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51b8acb0ea187c17d220d80f105ad6ae49371688d4eb8671c2a8eb5949b6e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666620"
---
# <a name="painting-and-drawing-functions"></a>Zeichnen und Zeichnen von Funktionen

Die folgenden Funktionen werden beim Zeichnen und Zeichnen verwendet.



| Funktion                                       | Beschreibung                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Bereitet ein Fenster für das Zeichnen vor.                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Zeichnet ein Rechteck und animiert es, um eine Symbol- oder Fensteraktivität anzugeben.                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Zeichnet eine Fensterbeschriftung.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Zeichnet einen oder mehrere Ränder des Rechtecks.                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Zeichnet ein Rechteck im Stil, das angibt, dass das Rechteck den Fokus besitzt.                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Zeichnet ein Rahmensteuerelement.                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Zeigt ein Bild an und wendet einen visuellen Effekt an, um einen Zustand anzugeben.                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Eine Rückruffunktion, die ein komplexes Bild für [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)rendert.                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Markiert das Ende des Zeichnens in einem Fenster.                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Verhindert das Zeichnen in ungültigen Bereichen eines Fensters.                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Leert den aktuellen Batch des aufrufenden Threads.                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Gibt die maximale Anzahl von Funktionsaufrufen zurück, die im aktuellen Batch des aufrufenden Threads gesammelt werden können. |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Legt die maximale Anzahl von Funktionsaufrufen fest, die im aktuellen Batch des aufrufenden Threads gesammelt werden können.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Gibt die Hintergrundfarbe für einen Gerätekontext zurück.                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Gibt den Hintergrundmischungsmodus für einen Gerätekontext zurück.                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Ruft das kumulierte umgebende Rechteck für einen Gerätekontext ab.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Ruft den Vordergrundmischungsmodus eines Gerätekontexts ab.                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Ruft die Koordinaten des kleinsten Rechtecks ab, das den Aktualisierungsbereich eines Fensters einschließt.                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Ruft den Updatebereich eines Fensters ab.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Ruft den Gerätekontext für ein Fenster ab, einschließlich Titelleiste, Menüs und Bildlaufleisten.                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Ruft eine Kopie des Fensterbereichs eines Fensters ab.                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Ruft die Abmessungen des engsten umschließenden Rechtecks für den Fensterbereich eines Fensters ab.                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Zeichnet grauen Text an einer Position.                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Fügt dem Updatebereich eines Fensters ein Rechteck hinzu.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Macht den Clientbereich innerhalb einer Region ungültig.                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Deaktiviert oder aktiviert das Zeichnen in einem Fenster.                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Eine Rückruffunktion, die mit der [**GrayString-Funktion**](/windows/desktop/api/Winuser/nf-winuser-graystringa) verwendet wird. Sie wird verwendet, um eine Zeichenfolge zu zeichnen.   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Füllt den Ausschneidebereich in einem Gerätekontext mit einem Muster aus.                                               |
| [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Aktualisiert eine Region im Clientbereich eines Fensters.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Legt den Hintergrund auf einen Farbwert fest.                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Legt den Hintergrundmischungsmodus eines Gerätekontexts fest.                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Steuert die Ansammlung von umgebenden Rechteckinformationen für einen Gerätekontext.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Legt den Vordergrundmischungsmodus fest.                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Legt den Fensterbereich eines Fensters fest.                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Aktualisiert den Clientbereich eines Fensters.                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Überprüft den Clientbereich innerhalb eines Rechtecks.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Überprüft den Clientbereich innerhalb einer Region.                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Gibt ein Handle für das Fenster zurück, das einem Gerätekontext zugeordnet ist.                                            |



 

 

 



