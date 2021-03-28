---
description: In der Regel wird eine Anwendung als Antwort auf eine WM-Zeichnungs Nachricht in ein Fenster gezeichnet \_ .
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: Die WM_PAINT Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69f7dab736972d8b7226890144efd8763de856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995119"
---
# <a name="the-wm_paint-message"></a>Die WM-Zeichnungs \_ Meldung

In der Regel wird eine Anwendung als Antwort auf eine WM- [**Zeichnungs \_**](wm-paint.md) Nachricht in ein Fenster gezeichnet. Das System sendet diese Meldung an eine Fenster Prozedur, wenn Änderungen am Fenster den Inhalt des Client Bereichs geändert haben. Das System sendet die Nachricht nur, wenn keine weiteren Meldungen in der Warteschlange der Anwendungs Nachricht vorhanden sind.

Nach dem Empfang [**einer \_ WM**](wm-paint.md) -Zeichnungs Nachricht kann eine Anwendung [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) aufrufen, um den Anzeigegeräte Kontext für den Client Bereich abzurufen und in Aufrufen von GDI-Funktionen zu verwenden, um die für die Aktualisierung des Client Bereichs erforderlichen Zeichnungsvorgänge auszuführen. Nachdem die Zeichnungsvorgänge abgeschlossen sind, ruft die Anwendung die [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) -Funktion auf, um den Anzeigegeräte kontextfrei zugeben.

Bevor [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) den Anzeigegeräte Kontext zurückgibt, bereitet das System den Gerätekontext für das angegebene Fenster vor. Zuerst wird der Clippingbereich für den Gerätekontext auf die Schnittmenge des zu aktualisierenden Fensters und des Teils festgelegt, der für den Benutzer sichtbar ist. Es werden nur die geänderten Teile des Fensters neu gezeichnet. Versuche, außerhalb dieses Bereichs zu zeichnen, werden abgeschnitten und nicht auf dem Bildschirm angezeigt.

Das System kann auch die Nachrichten [**WM \_ ncpaint**](wm-ncpaint.md) und [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) an die Fenster Prozedur senden, bevor [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) zurückgibt. Diese Nachrichten leiten die Anwendung an, den nicht-Client Bereich und den Fenster Hintergrund zu zeichnen. Der *nicht-Client Bereich* ist der Teil eines Fensters außerhalb des Client Bereichs. Der Bereich umfasst Features wie Titelleiste, Fenstermenü (auch als **Systemmenü** bezeichnet) und Bild Lauf leisten. Die meisten Anwendungen basieren auf der Standardfenster Funktion [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), um diesen Bereich zu zeichnen, und übergeben daher die **WM \_ ncpaint** -Meldung an diese Funktion. Der *Hintergrund des Fensters* ist die Farbe oder das Muster, mit dem ein Fenster gefüllt wird, bevor andere Zeichnungsvorgänge beginnen. Der Hintergrund deckt alle Bilder ab, die sich zuvor im Fenster oder auf dem Bildschirm im Fenster befinden. Wenn ein Fenster zu einer Fenster Klasse gehört, die über einen klassenhintergrund Pinsel verfügt, zeichnet die **defwindowproc** -Funktion den Hintergrund des Fensters automatisch.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) füllt eine [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur mit Informationen wie z. b. den Abmessungen des zu aktualisierenden Fensters und einem Flag, das angibt, ob der Hintergrund des Fensters gezeichnet wurde. Die Anwendung kann diese Informationen verwenden, um das Zeichnen zu optimieren. Beispielsweise kann es die Dimensionen des Aktualisierungs Bereichs verwenden, die vom **rcpaint** -Member angegeben werden, um das Zeichnen auf die Teile des Fensters zu beschränken, die aktualisiert werden müssen. Wenn eine Anwendung eine sehr einfache Ausgabe aufweist, kann Sie den Aktualisierungs Bereich ignorieren und im gesamten Fenster zeichnen, wobei das System die nicht benötigte Ausgabe verwerfen (Clip) soll. Da das Zeichnen von System Clips, das sich außerhalb des Clippingbereichs erstreckt, angezeigt wird, ist nur das Zeichnen in der Aktualisierungs Region sichtbar.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) legt den Aktualisierungs Bereich eines Fensters auf **null** fest. Dadurch wird die Region gelöscht, sodass keine nachfolgenden [**WM \_**](wm-paint.md) -Zeichnungs Meldungen mehr erzeugt werden. Wenn eine Anwendung eine **WM- \_** Zeichnungs Nachricht verarbeitet, aber nicht **BeginPaint** aufruft oder den Update Bereich anderweitig löscht, empfängt die Anwendung weiterhin **WM \_** -Zeichnungs Meldungen, solange der Bereich nicht leer ist. In allen Fällen muss eine Anwendung den Update Bereich löschen, bevor Sie von der **WM \_** -Zeichnungs Nachricht zurückgegeben wird.

Nachdem die Anwendung das Zeichnen abgeschlossen hat, sollte Sie [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)aufgerufen werden. In den meisten Fenstern gibt **endpaint** den Anzeigegeräte kontextfrei, sodass er für andere Fenster verfügbar ist. **Endpaint** zeigt auch das Caretzeichen an, wenn es zuvor durch [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)ausgeblendet wurde. **BeginPaint** blendet die Einfügemarke aus, um zu verhindern, dass Sie durch Zeichnungsvorgänge beschädigt werden

-   [Der Aktualisierungs Bereich](the-update-region.md)
-   [Ungültig machen und Validieren der Update Region](invalidating-and-validating-the-update-region.md)
-   [Der Aktualisierungs Bereich wird abgerufen.](retrieving-the-update-region.md)
-   [Ausschließen der Update Region](excluding-the-update-region.md)
-   [Synchrone und asynchrone Zeichnung](synchronous-and-asynchronous-drawing.md)

 

 
