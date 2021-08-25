---
title: Festlegen des Cursorbilds
description: Festlegen des Cursorbilds
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4723289155bc7898f6f49e188ad972ca152332c82994b57c79af493c8fe6b572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896910"
---
# <a name="setting-the-cursor-image"></a>Festlegen des Cursorbilds

Der *Cursor* ist das kleine Bild, das die Position der Maus oder eines anderen Zeigegeräts zeigt. Viele Anwendungen ändern das Cursorbild, um dem Benutzer Feedback zu geben. Obwohl dies nicht erforderlich ist, fügt sie Ihrer Anwendung ein wenig feiner hinzu.

Windows stellt eine Reihe von Standardcursorbildern( *Systemcursor) zur Unterstützung von .* Dazu gehören der Pfeil, die Hand, der Lichtstrahl, die Sanduhr (die jetzt ein rotierender Kreis ist) und andere. In diesem Abschnitt wird die Verwendung der Systemcursor beschrieben. Erweiterte Aufgaben wie das Erstellen benutzerdefinierter Cursor finden Sie unter [Cursor.](/windows/desktop/menurc/cursors)

Sie können einen Cursor einer Fensterklasse zuordnen, indem Sie den **hCursor-Member** der [**WNDCLASS-**](/windows/win32/api/winuser/ns-winuser-wndclassa) oder [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) festlegen. Andernfalls ist der Standardcursor der Pfeil. Wenn der Mauszeiger über ein Fenster bewegt wird, empfängt das Fenster eine [**WM \_ SETCURSOR-Meldung**](/windows/desktop/menurc/wm-setcursor) (es sei denn, die Maus wurde von einem anderen Fenster erfasst). An diesem Punkt tritt eines der folgenden Ereignisse auf:

-   Die Anwendung legt den Cursor fest, und die Fensterprozedur gibt **TRUE zurück.**
-   Die Anwendung führt nichts aus und übergibt [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) an [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Zum Festlegen des Cursors führt ein Programm Folgendes aus:

1.  Ruft [**LoadCursor auf,**](/windows/desktop/api/winuser/nf-winuser-loadcursora) um den Cursor in den Arbeitsspeicher zu laden. Diese Funktion gibt ein Handle an den Cursor zurück.
2.  Ruft [**SetCursor auf**](/windows/desktop/api/winuser/nf-winuser-setcursor) und übergibt das Cursorhandle.

Wenn die Anwendung WM [**\_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, verwendet die **DefWindowProc-Funktion** andernfalls den folgenden Algorithmus, um das Cursorbild zu setzen:

1.  Wenn das Fenster über ein übergeordnetes Element verfügt, senden Sie die [**WM \_ SETCURSOR-Nachricht**](/windows/desktop/menurc/wm-setcursor) an das übergeordnete Element, das behandelt werden soll.
2.  Wenn das Fenster über einen Klassencursor verfügt, legen Sie den Cursor andernfalls auf den Klassencursor fest.
3.  Wenn kein Klassencursor angezeigt wird, legen Sie den Cursor auf den Pfeilcursor fest.

Die [**LoadCursor-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadcursora) kann entweder einen benutzerdefinierten Cursor aus einer Ressource oder einen der Systemcursor laden. Das folgende Beispiel zeigt, wie der Cursor auf den Systemhandcursor festgelegt wird.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Wenn Sie den Cursor ändern, wird das Cursorbild bei der nächsten Mausbewegung zurückgesetzt, es sei denn, Sie fangen die [**WM \_ SETCURSOR-Meldung**](/windows/desktop/menurc/wm-setcursor) ab und setzen den Cursor erneut. Der folgende Code zeigt, wie WM **\_ SETCURSOR behandelt wird.**


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Dieser Code überprüft zuerst die unteren 16 Bits von *lParam.* Wenn `LOWORD(lParam)` **HTCLIENT entspricht,** bedeutet dies, dass sich der Cursor über dem Clientbereich des Fensters befindet. Andernfalls befindet sich der Cursor über dem Nichtclientbereich. In der Regel sollten Sie nur den Cursor für den Clientbereich festlegen und Windows den Cursor für den Nichtclientbereich festlegen.

## <a name="next"></a>Nächste

[Benutzereingabe: Erweitertes Beispiel](user-input--extended-example.md)

 

 