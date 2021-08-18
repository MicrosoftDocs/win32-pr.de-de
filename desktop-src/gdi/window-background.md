---
description: Der Fensterhintergrund ist die Farbe oder das Muster, die verwendet wird, um den Clientbereich zu füllen, bevor ein Fenster mit dem Zeichnen beginnt.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Fensterhintergrund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819f3bf333728909bdd0e374d41b7665f0517bcc17666b88c58f610e0127d942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848940"
---
# <a name="window-background"></a>Fensterhintergrund

Der Fensterhintergrund ist die Farbe oder das Muster, die verwendet wird, um den Clientbereich zu füllen, bevor ein Fenster mit dem Zeichnen beginnt. Der Fensterhintergrund deckt alles auf dem Bildschirm ab, bevor das Fenster verschoben wurde, löschen vorhandene Bilder und verhindern, dass die neue Ausgabe der Anwendung mit nicht verknüpften Informationen gemischt wird.

Das System zeichnet den Hintergrund für ein Fenster oder gibt dem Fenster die Möglichkeit, dies zu tun, indem es eine [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) sendet, wenn die Anwendung [**BeginPaint aufruft.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Wenn eine Anwendung die Nachricht nicht verarbeiten, sondern an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, löscht das System den Hintergrund, indem es ihn mit dem Muster in dem Hintergrundpinsel füllt, der von der -Klasse des Fensters angegeben wird. Wenn der Pinsel ungültig ist oder die Klasse über keinen Hintergrundpinsel verfügt, legt das System den **fErase-Member** in der [**PAINTSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-paintstruct) fest, die **BeginPaint** zurückgibt, aber keine andere Aktion ausgibt. Die Anwendung hat dann bei Bedarf eine zweite Möglichkeit, den Fensterhintergrund zu zeichnen.

Wenn WM [**\_ ERASEBKGND verarbeitet**](../winmsg/wm-erasebkgnd.md)wird, sollte die Anwendung den *wParam-Parameter* der Nachricht verwenden, um den Hintergrund zu zeichnen. Dieser Parameter enthält ein Handle für den Anzeigegerätekontext für das Fenster. Nach dem Zeichnen des Hintergrunds sollte die Anwendung einen Wert ungleich 0 (null) zurückgeben. Dadurch wird sichergestellt, dass [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) den **fErase-Member** der [**PAINTSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-paintstruct) nicht fälschlicherweise auf einen Wert ungleich null (der angibt, dass der Hintergrund gelöscht werden soll) festgelegt wird, wenn die Anwendung die nachfolgende [**WM \_ PAINT-Nachricht**](wm-paint.md) verarbeitet.

Eine Anwendung kann einen Klassenhintergrundpinsel definieren, indem dem **hbrBackground-Member** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) beim Registrieren der Klasse mit der [**RegisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassa) ein Pinselhandpunkt oder ein Systemfarbwert zugewiesen wird. Die [**GetStockObject-**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) [**oder CreateSolidBrush-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) kann verwendet werden, um ein Pinselhandle zu erstellen. Ein Systemfarbwert kann einer der für die [**SetSysColors-Funktion definierten**](/windows/win32/api/winuser/nf-winuser-setsyscolors) Werte sein. (Der Wert muss um eins erhöht werden, bevor er dem Member zugewiesen wird.)

Eine Anwendung kann die [**WM \_ ERASEBKGND-Nachricht**](../winmsg/wm-erasebkgnd.md) verarbeiten, obwohl ein Klassenhintergrundpinsel definiert ist. Dies ist typisch für Anwendungen, die es dem Benutzer ermöglichen, die Hintergrundfarbe oder das Muster des Fensters für ein angegebenes Fenster zu ändern, ohne andere Fenster in der Klasse zu beeinflussen. In solchen Fällen darf die Anwendung die Nachricht nicht an [**DefWindowProc übergeben.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Es ist nicht erforderlich, dass eine Anwendung Pinsel auszurichten, da das System den Pinsel mithilfe des Fensterinsprungs als Bezugspunkt zeichnet. In diesem Fall kann der Benutzer das Fenster verschieben, ohne die Ausrichtung von Musterpinsel zu beeinträchtigen.

 

 
