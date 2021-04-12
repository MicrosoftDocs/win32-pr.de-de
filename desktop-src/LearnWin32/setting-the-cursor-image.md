---
title: Festlegen des Cursor Bilds
description: Festlegen des Cursor Bilds
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472893"
---
# <a name="setting-the-cursor-image"></a>Festlegen des Cursor Bilds

Der *Cursor* ist das kleine Bild, das die Position der Maus oder eines anderen Zeige Geräts anzeigt. Viele Anwendungen ändern das Cursor Bild, um dem Benutzer Feedback zu geben. Obwohl es nicht erforderlich ist, wird Ihrer Anwendung ein gutes Paar von Polnisch hinzugefügt.

Windows stellt eine Reihe von Standard Cursor Images bereit, die als *System Cursor* bezeichnet werden. Diese umfassen den Pfeil, die Hand, den I-Beam, den Sanduhr (der jetzt ein drehende Kreis ist) und andere. In diesem Abschnitt wird die Verwendung der systemcursorn beschrieben. Erweiterte Aufgaben, wie das Erstellen von benutzerdefinierten Cursorn, finden Sie unter [Cursors](/windows/desktop/menurc/cursors).

Sie können einen Cursor einer Fenster Klasse zuordnen, indem Sie den **hcursor** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -oder [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur festlegen. Andernfalls ist der Standard Cursor der Pfeil. Wenn die Maus über ein Fenster bewegt wird, empfängt das Fenster eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht (es sei denn, ein anderes Fenster hat die Maus erfasst). An diesem Punkt tritt eines der folgenden Ereignisse auf:

-   Die Anwendung legt den Cursor fest, und die Fenster Prozedur gibt **true** zurück.
-   Die Anwendung führt nichts aus und übergibt [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Zum Festlegen des Cursors führt ein Programm Folgendes aus:

1.  Ruft [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) auf, um den Cursor in den Arbeitsspeicher zu laden. Diese Funktion gibt ein Handle für den Cursor zurück.
2.  Ruft [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) auf und übergibt im Cursor handle.

Andernfalls verwendet die **defwindowproc** -Funktion den folgenden Algorithmus zum Festlegen des Cursor Bilds, wenn die Anwendung [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt:

1.  Wenn das Fenster über ein übergeordnetes Element verfügt, leiten Sie die [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Meldung an das übergeordnete Element weiter, um
2.  Wenn das Fenster über einen Klassen Cursor verfügt, legen Sie den Cursor auf den Klassen Cursor fest.
3.  Wenn kein Klassen Cursor vorhanden ist, legen Sie den Cursor auf den Pfeilcursor fest.

Die [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) -Funktion kann entweder einen benutzerdefinierten Cursor aus einer Ressource oder einen der systemcursorn laden. Im folgenden Beispiel wird gezeigt, wie der Cursor auf den System Hand Cursor festgelegt wird.


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



Wenn Sie den Cursor ändern, setzt das Cursor Bild bei der nächsten Mausbewegung zurück, es sei denn, Sie fangen die [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Meldung an und legen den Cursor erneut fest. Der folgende Code zeigt, wie **WM \_ SetCursor** behandelt wird.


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



Mit diesem Code werden zunächst die unteren 16 Bits von *LPARAM* überprüft. Wenn `LOWORD(lParam)` " **htclient**" ist, bedeutet dies, dass sich der Cursor über dem Client Bereich des Fensters befindet. Andernfalls befindet sich der Cursor über dem nicht-Client Bereich. Normalerweise sollten Sie nur den Cursor für den Client Bereich festlegen und Windows den Cursor für den nicht-Client Bereich festlegen lassen.

## <a name="next"></a>Nächste

[Benutzereingabe: erweitertes Beispiel](user-input--extended-example.md)

 

 