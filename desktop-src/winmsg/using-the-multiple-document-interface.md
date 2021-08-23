---
description: In diesem Abschnitt wird erläutert, wie Aufgaben ausgeführt werden, die der Schnittstelle für mehrere Dokumente zugeordnet sind.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Verwenden der Schnittstelle für mehrere Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09453e6f4a9301c8cdfc9d675ae1efd7853594fc472a446a021e3bd3e075fc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028328"
---
# <a name="using-the-multiple-document-interface"></a>Verwenden der Schnittstelle für mehrere Dokumente

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben ausgeführt werden:

-   [Registrieren von untergeordneten Klassen und Framefensterklassen](#registering-child-and-frame-window-classes)
-   [Erstellen von Frame- und untergeordneten Windows](#creating-frame-and-child-windows)
-   [Schreiben der Hauptnachrichtenschleife](#writing-the-main-message-loop)
-   [Schreiben der Framefensterprozedur](#writing-the-frame-window-procedure)
-   [Schreiben der Untergeordneten Fensterprozedur](#writing-the-child-window-procedure)
-   [Erstellen eines untergeordneten Fensters](#creating-a-child-window)

Zur Veranschaulichung dieser Aufgaben enthält dieser Abschnitt Beispiele aus Multipad, einer typischen MDI-Anwendung (Multiple Document Interface).

## <a name="registering-child-and-frame-window-classes"></a>Registrieren von untergeordneten Klassen und Framefensterklassen

Eine typische MDI-Anwendung muss zwei Fensterklassen registrieren: eine für ihr Rahmenfenster und eine für ihre untergeordneten Fenster. Wenn eine Anwendung mehrere Dokumenttypen unterstützt (z. B. ein Arbeitsblatt und ein Diagramm), muss sie für jeden Typ eine Fensterklasse registrieren.

Die Klassenstruktur für das Rahmenfenster ähnelt der Klassenstruktur für das Hauptfenster in Nicht-MDI-Anwendungen. Die Klassenstruktur für die untergeordneten MDI-Fenster unterscheidet sich geringfügig von der Struktur für untergeordnete Fenster in Nicht-MDI-Anwendungen wie folgt:

-   Die Klassenstruktur sollte über ein Symbol verfügen, da der Benutzer ein untergeordnetes MDI-Fenster so minimieren kann, als wäre es ein normales Anwendungsfenster.
-   Der Menüname sollte **NULL** sein, da ein untergeordnetes MDI-Fenster kein eigenes Menü haben kann.
-   Die Klassenstruktur sollte zusätzlichen Platz in der Fensterstruktur reservieren. Mit diesem Bereich kann die Anwendung Daten, z. B. einen Dateinamen, einem bestimmten untergeordneten Fenster zuordnen.

Das folgende Beispiel zeigt, wie Multipad seine Frame- und untergeordneten Fensterklassen registriert.


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a>Erstellen von Frame- und untergeordneten Windows

Nach dem Registrieren der Fensterklassen kann eine MDI-Anwendung ihre Fenster erstellen. Zunächst wird das Rahmenfenster mithilfe der Funktion [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) erstellt. Nach dem Erstellen des Rahmenfensters erstellt die Anwendung ihr Clientfenster, indem sie erneut **CreateWindow** oder **CreateWindowEx** verwendet. Die Anwendung sollte MDICLIENT als Klassennamen des Clientfensters angeben. **MDICLIENT** ist eine vorab registrierte Fensterklasse, die vom System definiert wird. Der *lpvParam-Parameter* von **CreateWindow** oder **CreateWindowEx** sollte auf eine [**CLIENTCREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) verweisen. Diese Struktur enthält die in der folgenden Tabelle beschriebenen Member:



| Member           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hWindowMenu**  | Handle für das Fenstermenü, das zum Steuern von untergeordneten MDI-Fenstern verwendet wird. Wenn untergeordnete Fenster erstellt werden, fügt die Anwendung ihre Titel dem Fenstermenü als Menüelemente hinzu. Der Benutzer kann dann ein untergeordnetes Fenster aktivieren, indem er im Fenstermenü auf seinen Titel klickt.                                                               |
| **idFirstChild** | Gibt den Bezeichner des ersten untergeordneten MDI-Fensters an. Dem ersten erstellten untergeordneten MDI-Fenster wird dieser Bezeichner zugewiesen. Zusätzliche Fenster werden mit inkrementierten Fensterbezeichnern erstellt. Wenn ein untergeordnetes Fenster zerstört wird, weist das System die Fensterbezeichner sofort neu zu, um ihren Bereich zusammenhängend zu halten. |



 

Wenn dem Fenstermenü der Titel eines untergeordneten Fensters hinzugefügt wird, weist das System dem untergeordneten Fenster einen Bezeichner zu. Wenn der Benutzer auf den Titel eines untergeordneten Fensters klickt, empfängt das Rahmenfenster eine [**WM \_ COMMAND-Meldung**](../menurc/wm-command.md) mit dem Bezeichner im *wParam-Parameter.* Sie sollten einen Wert für das **idFirstChild-Element** angeben, das nicht mit Menüelementbezeichnern im Menü des Rahmenfensters in Konflikt steht.

Die Prozedur "Framefenster" von Multipad erstellt das MDI-Clientfenster während der Verarbeitung der [**WM \_ CREATE-Nachricht.**](wm-create.md) Das folgende Beispiel zeigt, wie das Clientfenster erstellt wird.


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



Titel von untergeordneten Fenstern werden am unteren Rand des Fenstermenüs hinzugefügt. Wenn die Anwendung dem Fenstermenü mithilfe der [**AppendMenu-Funktion**](/windows/win32/api/winuser/nf-winuser-appendmenua) Zeichenfolgen hinzufügt, können diese Zeichenfolgen durch die Titel der untergeordneten Fenster überschrieben werden, wenn das Fenstermenü neu gezeichnet wird (wenn ein untergeordnetes Fenster erstellt oder zerstört wird). Eine MDI-Anwendung, die dem Fenstermenü Zeichenfolgen hinzufügt, sollte die [**InsertMenu-Funktion**](/windows/win32/api/winuser/nf-winuser-insertmenua) verwenden und überprüfen, ob die Titel untergeordneter Fenster diese neuen Zeichenfolgen nicht überschrieben haben.

Verwenden Sie den **WS \_ CLIPCHILDREN-Stil,** um das MDI-Clientfenster zu erstellen, um zu verhindern, dass das Fenster seine untergeordneten Fenster übermalt.

## <a name="writing-the-main-message-loop"></a>Schreiben der Hauptnachrichtenschleife

Die Hauptmeldungsschleife einer MDI-Anwendung ähnelt der von Zugriffstasten einer Nicht-MDI-Anwendung. Der Unterschied besteht darin, dass die MDI-Nachrichtenschleife die [**TranslateMDISysAccel-Funktion**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) aufruft, bevor sie auf anwendungsdefinierte Zugriffstasten überprüft oder die Nachricht versendet.

Das folgende Beispiel zeigt die Nachrichtenschleife einer typischen MDI-Anwendung. Beachten Sie, dass [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -1 zurückgeben kann, wenn ein Fehler auftritt.


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



Die [**TranslateMDISysAccel-Funktion**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) übersetzt [**WM \_ KEYDOWN-Nachrichten**](../inputdev/wm-keydown.md) in [**WM \_ SYSCOMMAND-Nachrichten**](../menurc/wm-syscommand.md) und sendet sie an das aktive untergeordnete MDI-Fenster. Wenn die Nachricht keine MDI-Zugriffstastennachricht ist, gibt die Funktion **FALSE** zurück. In diesem Fall verwendet die Anwendung die [**TranslateAccelerator-Funktion,**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) um zu bestimmen, ob eine der anwendungsdefinierten Zugriffstasten gedrückt wurde. Falls nicht, wird die Nachricht von der Schleife an die entsprechende Fensterprozedur gesendet.

## <a name="writing-the-frame-window-procedure"></a>Schreiben der Framefensterprozedur

Die Fensterprozedur für ein MDI-Rahmenfenster ähnelt der Prozedur für das Hauptfenster einer Nicht-MDI-Anwendung. Der Unterschied besteht darin, dass eine Framefensterprozedur alle Nachrichten übergibt, die sie nicht an die [**DefFrameProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defframeproca) und nicht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verarbeitet. Darüber hinaus muss die Framefensterprozedur auch einige Nachrichten übergeben, die sie verarbeitet, einschließlich der in der folgenden Tabelle aufgeführten Nachrichten.



| `Message`                                  | Response                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WM-BEFEHL**](../menurc/wm-command.md)     | Aktiviert das untergeordnete MDI-Fenster, das der Benutzer ausgibt. Diese Meldung wird gesendet, wenn der Benutzer im Fenstermenü des MDI-Rahmenfensters ein untergeordnetes MDI-Fenster ausgibt. Der fensterbezeichner, der dieser Meldung begleitet, identifiziert das untergeordnete MDI-Fenster, das aktiviert werden soll. |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)   | Öffnet das Fenstermenü des aktiven untergeordneten MDI-Fensters, wenn der Benutzer die Tastenkombination ALT+– (minus) drückt.                                                                                                                                                      |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md) | Übergibt den Tastaturfokus an das MDI-Clientfenster, das ihn wiederum an das aktive untergeordnete MDI-Fenster übergibt.                                                                                                                                                         |
| [**\_WM-GRÖßE**](wm-size.md)              | Passt die Größe des MDI-Clientfensters an den Clientbereich des neuen Rahmenfensters an. Wenn die Rahmenfensterprozedur die Größe des MDI-Clientfensters auf eine andere Größe anpasst, sollte die Meldung nicht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben werden.                   |



 

Die Framefensterprozedur in Multipad heißt MPFrameWndProc. Die Behandlung anderer Nachrichten durch MPFrameWndProc ähnelt der Behandlung von Nicht-MDI-Anwendungen. [**WM \_ COMMAND-Nachrichten**](../menurc/wm-command.md) in Multipad werden von der lokal definierten CommandHandler-Funktion verarbeitet. Für Befehlsmeldungen, die Multipad nicht verarbeitet, ruft CommandHandler die [**DefFrameProc-Funktion auf.**](/windows/win32/api/winuser/nf-winuser-defframeproca) Wenn Multipad **defFrameProc** standardmäßig nicht verwendet, kann der Benutzer ein untergeordnetes Fenster nicht über das Fenstermenü aktivieren, da die **WM \_ COMMAND-Meldung,** die durch Klicken auf das Menüelement des Fensters gesendet wird, verloren geht.

## <a name="writing-the-child-window-procedure"></a>Schreiben der Untergeordneten Fensterprozedur

Wie die Framefensterprozedur verwendet eine MDI-Prozedur für untergeordnete Fenster standardmäßig eine spezielle Funktion zum Verarbeiten von Nachrichten. Alle Nachrichten, die von der untergeordneten Fensterprozedur nicht verarbeitet werden, müssen an die [**DefMDIChildProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) und nicht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben werden. Darüber hinaus müssen einige Meldungen zur Fensterverwaltung an **DefMDIChildProc** übergeben werden, auch wenn die Anwendung die Nachricht verarbeitet, damit MDI ordnungsgemäß funktioniert. Im Folgenden werden die Meldungen angezeigt, die die Anwendung an **DefMDIChildProc** übergeben muss.



| `Message`                                       | Response                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHILDACTIVATE**](wm-childactivate.md) | Führt die Aktivierungsverarbeitung durch, wenn untergeordnete MDI-Fenster dimensioniert, verschoben oder angezeigt werden. Diese Meldung muss übergeben werden.                                                                                                                                        |
| [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) | Berechnet die Größe eines maximierten untergeordneten MDI-Fensters basierend auf der aktuellen Größe des MDI-Clientfensters.                                                                                                                                                  |
| [**WM \_ MENUCHAR**](../menurc/wm-menuchar.md)        | Übergibt die Nachricht an das MDI-Rahmenfenster.                                                                                                                                                                                                               |
| [**WM \_ MOVE**](wm-move.md)                   | Berechnet MDI-Client-Scrollleisten neu, sofern vorhanden.                                                                                                                                                                                                 |
| [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)      | Aktiviert das untergeordnete Fenster, wenn es sich nicht um das aktive untergeordnete MDI-Fenster handelt.                                                                                                                                                                                     |
| [**\_WM-GRÖßE**](wm-size.md)                   | Führt Vorgänge aus, die zum Ändern der Größe eines Fensters erforderlich sind, insbesondere zum Maximieren oder Wiederherstellen eines untergeordneten MDI-Fensters. Wenn diese Meldung nicht an die [**DefMDIChildProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) übergeben wird, werden höchst unerwünschte Ergebnisse erzeugt. |
| [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md)    | Verarbeitet Menübefehle für Fenster (früher als System bezeichnet): **SC \_ NEXTWINDOW,** **SC \_ PREVWINDOW,** **SC \_ MOVE,** **SC \_ SIZE** und **SC \_ MAXIMIZE**.                                                                                                        |



 

## <a name="creating-a-child-window"></a>Erstellen eines untergeordneten Fensters

Um ein untergeordnetes MDI-Fenster zu erstellen, kann eine Anwendung entweder die [**CreateMDIWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) aufrufen oder eine [**WM \_ MDICREATE-Nachricht**](wm-mdicreate.md) an das MDI-Clientfenster senden. (Die Anwendung kann die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) mit dem **WS \_ EX \_ MDICHILD-Stil** verwenden, um untergeordnete MDI-Fenster zu erstellen.) Eine Singlethread-MDI-Anwendung kann beide Methoden verwenden, um ein untergeordnetes Fenster zu erstellen. Ein Thread in einer Multithread-MDI-Anwendung muss die **Funktion CreateMDIWindow** oder **CreateWindowEx** verwenden, um ein untergeordnetes Fenster in einem anderen Thread zu erstellen.

Der *lParam-Parameter* einer [**WM \_ MDICREATE-Nachricht**](wm-mdicreate.md) ist ein far-Zeiger auf eine [**MDICREATESTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) Die -Struktur umfasst vier Dimensionsmitglieder: **x** und **y**, die die horizontale und vertikale Position des Fensters angeben, und **cx** und **cy**, die die horizontalen und vertikalen Ausdrungen des Fensters angeben. Jeder dieser Member kann explizit von der Anwendung zugewiesen werden, oder sie können auf **CW \_ USEDEFAULT** festgelegt werden. In diesem Fall wählt das System eine Position, Größe oder beides gemäß einem kaskadierenden Algorithmus aus. In jedem Fall müssen alle vier Member initialisiert werden. Multipad verwendet **CW \_ USEDEFAULT** für alle Dimensionen.

Der letzte Member der [**MDICREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) ist der Stil member, der Stilbits für das Fenster enthalten kann.  Um ein untergeordnetes MDI-Fenster zu erstellen, das eine beliebige Kombination aus Fensterformaten haben kann, geben Sie den **MDIS \_ ALLCHILDSTYLES-Fensterstil** an. Wenn dieses Format nicht angegeben wird, enthält ein untergeordnetes MDI-Fenster die Formate **WS \_ MINIMIZE,** **WS \_ MAXIMIZE,** **WS \_ HSCROLL** und **\_ WS VSCROLL** als Standardeinstellungen.

Multipad erstellt seine untergeordneten MDI-Fenster mithilfe der lokal definierten AddFile-Funktion (in der Quelldatei MPFILE). C). Die AddFile-Funktion legt den Titel des untergeordneten Fensters fest, indem das **szTitle-Member** der [**MDICREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) des Fensters entweder dem Namen der datei zugewiesen wird, die bearbeitet wird, oder auf "Unbearbeitet". Der **szClass-Member** wird auf den Namen der untergeordneten MDI-Fensterklasse festgelegt, die in der InitializeApplication-Funktion von Multipad registriert ist. Der **hOwner-Member** wird auf das Instanzhand handle der Anwendung festgelegt.

Das folgende Beispiel zeigt die AddFile-Funktion in Multipad.


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



Der im *lParam-Parameter* der [**WM \_ MDICREATE-Nachricht**](wm-mdicreate.md) übergebene Zeiger wird an die [**CreateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowa) übergeben und wird als erster Member in der [**CREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-createstructa) angezeigt, der in der [**WM \_ CREATE-Nachricht**](wm-create.md) übergeben wird. In Multipad initialisiert sich das untergeordnete Fenster während der **WM \_ CREATE-Nachrichtenverarbeitung** selbst, indem Dokumentvariablen in den zusätzlichen Daten initialisiert und das untergeordnete Fenster des Bearbeitungssteuerfelds erstellt wird.

 

 
