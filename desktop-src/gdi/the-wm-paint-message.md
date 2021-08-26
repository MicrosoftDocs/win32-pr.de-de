---
description: In der Regel zeichnet eine Anwendung in einem Fenster als Reaktion auf eine WM \_ PAINT-Nachricht.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: Die WM_PAINT-Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965180"
---
# <a name="the-wm_paint-message"></a>DIE \_ WM-PAINT-Nachricht

In der Regel zeichnet eine Anwendung in einem Fenster als Reaktion auf eine [**WM \_ PAINT-Nachricht.**](wm-paint.md) Das System sendet diese Meldung an eine Fensterprozedur, wenn Änderungen am Fenster den Inhalt des Clientbereichs geändert haben. Das System sendet die Nachricht nur, wenn keine anderen Nachrichten in der Anwendungsnachrichtenwarteschlange vorhanden sind.

Wenn eine [**\_ WM-PAINT-Nachricht**](wm-paint.md) empfangen wird, kann eine Anwendung [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) aufrufen, um den Anzeigegerätekontext für den Clientbereich abzurufen und ihn in Aufrufen von GDI-Funktionen zu verwenden, um alle Zeichnungsvorgänge auszuführen, die zum Aktualisieren des Clientbereichs erforderlich sind. Nach Abschluss der Zeichnungsvorgänge ruft die Anwendung die [**EndPaint-Funktion**](/windows/desktop/api/Winuser/nf-winuser-endpaint) auf, um den Anzeigegerätekontext freizugeben.

Bevor [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) den Anzeigegerätekontext zurückgibt, bereitet das System den Gerätekontext für das angegebene Fenster vor. Zunächst wird der Clippingbereich für den Gerätekontext so festgelegt, dass er der Schnittmenge des Bereichs des Fensters entspricht, der aktualisiert werden muss, und dem Teil, der für den Benutzer sichtbar ist. Nur die Teile des Fensters, die geändert wurden, werden neu gezeichnet. Versuche, außerhalb dieses Bereichs zu zeichnen, werden abgeschnitten und nicht auf dem Bildschirm angezeigt.

Das System kann auch [**WM \_ NCPAINT-**](wm-ncpaint.md) und [**WM \_ ERASEBKGND-Nachrichten**](../winmsg/wm-erasebkgnd.md) an die Fensterprozedur senden, bevor [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) zurückgegeben wird. Diese Meldungen weisen die Anwendung an, den Nichtclientbereich und den Fensterhintergrund zu zeichnen. Der *Nichtclientbereich* ist der Teil eines Fensters, das sich außerhalb des Clientbereichs befindet. Der Bereich enthält Features wie die Titelleiste, das Fenstermenü (auch als **Systemmenü** bezeichnet) und Scrollleisten. Die meisten Anwendungen verwenden die Standardfensterfunktion [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)um diesen Bereich zu zeichnen und daher die **WM \_ NCPAINT-Nachricht** an diese Funktion zu übergeben. Der *Fensterhintergrund* ist die Farbe oder das Muster, mit der ein Fenster gefüllt wird, bevor andere Zeichnungsvorgänge beginnen. Der Hintergrund deckt alle Bilder ab, die zuvor im Fenster oder auf dem Bildschirm unter dem Fenster angezeigt wurden. Wenn ein Fenster zu einer Fensterklasse mit einem Klassenhintergrundpinsel gehört, zeichnet die **DefWindowProc-Funktion** den Fensterhintergrund automatisch.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) füllt eine [**PAINTSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-paintstruct) mit Informationen wie den Dimensionen des zu aktualisierenden Fensterteils und einem Flag, das angibt, ob der Fensterhintergrund gezeichnet wurde. Die Anwendung kann diese Informationen verwenden, um das Zeichnen zu optimieren. Sie kann z. B. die Vom **rcPaint-Element** angegebenen Dimensionen des Updatebereichs verwenden, um das Zeichnen auf die Teile des Fensters zu beschränken, die aktualisiert werden müssen. Wenn eine Anwendung über eine sehr einfache Ausgabe verfügt, kann sie den Updatebereich ignorieren und im gesamten Fenster zeichnen, wobei das System jede nicht benötigte Ausgabe verwirft (ausschneiden) muss. Da das System zeichnungsclips, das sich außerhalb des Ausschneidebereichs erstreckt, ist nur das Zeichnen sichtbar, das sich im Updatebereich befindet.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) legt den Updatebereich eines Fensters auf **NULL** fest. Dadurch wird die Region gelöscht, sodass keine weiteren [**WM \_ PAINT-Meldungen**](wm-paint.md) generiert werden können. Wenn eine Anwendung eine **WM \_ PAINT-Nachricht** verarbeitet, aber **BeginPaint** nicht aufruft oder die Updateregion anderweitig löscht, empfängt die Anwendung weiterhin **WM \_ PAINT-Nachrichten,** solange die Region nicht leer ist. In allen Fällen muss eine Anwendung den Updatebereich löschen, bevor sie von der **WM \_ PAINT-Nachricht** zurückgegeben wird.

Nachdem die Anwendung das Zeichnen abgeschlossen hat, sollte sie [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)aufrufen. Für die meisten Fenster gibt **EndPaint** den Anzeigegerätekontext frei und macht ihn für andere Fenster verfügbar. **EndPaint** zeigt auch den Caretstrich an, wenn er zuvor von [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)ausgeblendet wurde. **BeginPaint** blendet das Caretzeichen aus, um zu verhindern, dass Zeichnungsvorgänge es beschädigen.

-   [Die Updateregion](the-update-region.md)
-   [Invalidieren und Überprüfen des Updatebereichs](invalidating-and-validating-the-update-region.md)
-   [Abrufen der Updateregion](retrieving-the-update-region.md)
-   [Ausschließen der Updateregion](excluding-the-update-region.md)
-   [Synchrones und asynchrones Zeichnen](synchronous-and-asynchronous-drawing.md)

 

 
