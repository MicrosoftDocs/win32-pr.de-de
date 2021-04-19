---
description: In diesem Abschnitt wird erläutert, wie mit der Multiple Document-Schnittstelle verknüpfte Aufgaben ausgeführt werden.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Verwenden der Multiple Document-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362936"
---
# <a name="using-the-multiple-document-interface"></a>Verwenden der Multiple Document-Schnittstelle

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben ausgeführt werden:

-   [Registrieren von untergeordneten und Rahmen Fenster Klassen](#registering-child-and-frame-window-classes)
-   [Erstellen von Frame-und untergeordneten Fenstern](#creating-frame-and-child-windows)
-   [Schreiben der Hauptnachrichten Schleife](#writing-the-main-message-loop)
-   [Schreiben der Rahmen Fenster Prozedur](#writing-the-frame-window-procedure)
-   [Schreiben der Prozedur für das untergeordnete Fenster](#writing-the-child-window-procedure)
-   [Erstellen eines untergeordneten Fensters](#creating-a-child-window)

Um diese Aufgaben zu veranschaulichen, enthält dieser Abschnitt Beispiele aus MULTIPAD, einer typischen MDI-Anwendung (Multiple Document Interface).

## <a name="registering-child-and-frame-window-classes"></a>Registrieren von untergeordneten und Rahmen Fenster Klassen

Eine typische MDI-Anwendung muss zwei Fenster Klassen registrieren: eine für das Rahmen Fenster und eine für die untergeordneten Fenster. Wenn eine Anwendung mehr als einen Dokumenttyp unterstützt (z. b. eine Kalkulations Tabelle und ein Diagramm), muss für jeden Typ eine Fenster Klasse registriert werden.

Die Klassenstruktur für das Rahmen Fenster ähnelt der-Klassenstruktur für das Hauptfenster von nicht-–-MDI-Anwendungen. Die Klassenstruktur für die untergeordneten MDI-Fenster unterscheidet sich geringfügig von der Struktur für untergeordnete Fenster in nicht –-MDI-Anwendungen wie folgt:

-   Die Klassenstruktur sollte ein Symbol aufweisen, da der Benutzer ein untergeordnetes MDI-Fenster minimieren kann, als ob es sich um ein normales Anwendungsfenster handelt.
-   Der Menüname sollte **null** sein, da ein untergeordnetes MDI-Fenster nicht über ein eigenes Menü verfügen kann.
-   Die Klassenstruktur sollte zusätzlichen Platz in der Fenster Struktur reservieren. Bei diesem Bereich kann die Anwendung Daten, z. b. einen Dateinamen, einem bestimmten untergeordneten Fenster zuordnen.

Das folgende Beispiel zeigt, wie das MULTIPAD seine Frame-und untergeordneten Fenster Klassen registriert.


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



## <a name="creating-frame-and-child-windows"></a>Erstellen von Frame-und untergeordneten Fenstern

Nachdem die Fenster Klassen registriert wurden, kann eine MDI-Anwendung Ihre Fenster erstellen. Zuerst wird das Rahmen Fenster mithilfe der Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder der Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " erstellt. Nachdem das Rahmen Fenster erstellt wurde, erstellt die Anwendung das Client Fenster, und zwar mithilfe von " **kreatewindow** " oder " **kreatewindowex**". Die Anwendung sollte MdiClient als Klassennamen für den Client Fenster angeben. **MdiClient** ist eine vorab übergeordnete Fenster Klasse, die vom System definiert wurde. Der *lpvparam* -Parameter von " **foratewindow** " oder " **foratewindowex** " sollte auf eine [**clientkreatestruct**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) -Struktur zeigen. Diese Struktur enthält die in der folgenden Tabelle beschriebenen Elemente:



| Member           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **hwindowmenu**  | Handle für das Fenstermenü, das zum Steuern untergeordneter MDI-Fenster verwendet wird. Wenn untergeordnete Fenster erstellt werden, fügt die Anwendung ihre Titel im Menü Fenster als Menü Elemente hinzu. Der Benutzer kann dann ein untergeordnetes Fenster aktivieren, indem er im Menü Fenster auf seinen Titel klickt.                                                               |
| **idfirstchild** | Gibt den Bezeichner des ersten untergeordneten MDI-Fensters an. Das erste erstellte untergeordnete MDI-Fenster wird diesem Bezeichner zugewiesen. Mit inkrementierten Fenster Bezeichner werden weitere Fenster erstellt. Wenn ein untergeordnetes Fenster zerstört wird, werden die Fenster Bezeichner sofort von dem System neu zugewiesen, um den Bereich zusammenhängend zu halten. |



 

Wenn der Titel eines untergeordneten Fensters dem Menü Fenster hinzugefügt wird, weist das System dem untergeordneten Fenster einen Bezeichner zu. Wenn der Benutzer auf den Titel eines untergeordneten Fensters klickt, empfängt das Rahmen Fenster eine [**WM- \_ Befehls**](../menurc/wm-command.md) Meldung mit dem Bezeichner im *wParam* -Parameter. Sie sollten einen Wert für das **idfirstchild** -Element angeben, das nicht mit Menü Element bezeichaten im Menü des Rahmen Fensters in Konflikt steht.

Die Rahmen Fenster Prozedur von MULTIPAD erstellt bei der Verarbeitung der [**WM \_ Create**](wm-create.md) -Meldung das MDI-Client Fenster. Im folgenden Beispiel wird gezeigt, wie das Client Fenster erstellt wird.


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



Am unteren Rand des Menü Fensters werden Titel von untergeordneten Fenstern hinzugefügt. Wenn die Anwendung dem Menü Fenster mithilfe der [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) -Funktion Zeichen folgen hinzufügt, können diese Zeichen folgen durch die Titel der untergeordneten Fenster überschrieben werden, wenn das Fenstermenü neu gezeichnet wird (wenn ein untergeordnetes Fenster erstellt oder zerstört wird). Eine MDI-Anwendung, die Ihrem Fenstermenü Zeichen folgen hinzufügt, sollte die [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) -Funktion verwenden und sicherstellen, dass die Titel der untergeordneten Fenster diese neuen Zeichen folgen nicht überschrieben haben.

Verwenden Sie das Format **WS \_ clipchildren** , um das MDI-Client Fenster zu erstellen, um zu verhindern, dass das Fenster über seine untergeordneten Fenster gezeichnet wird.

## <a name="writing-the-main-message-loop"></a>Schreiben der Hauptnachrichten Schleife

Die Hauptnachrichten Schleife einer MDI-Anwendung ähnelt der Verwendung einer Zugriffstaste für nicht-MDI-Anwendungen. Der Unterschied besteht darin, dass die MDI-Nachrichten Schleife die [**translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) -Funktion aufruft, bevor Sie auf Anwendungs definierte Zugriffstasten oder vor der Übermittlung der Nachricht überprüfen.

Das folgende Beispiel zeigt die Nachrichten Schleife einer typischen MDI-Anwendung. Beachten Sie, dass [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -1 zurückgeben kann, wenn ein Fehler vorliegt.


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



Die [**translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) -Funktion übersetzt [**WM- \_ KeyDown**](../inputdev/wm-keydown.md) -Nachrichten in [**WM- \_ syscommand**](../menurc/wm-syscommand.md) -Nachrichten und sendet Sie an das aktive untergeordnete MDI-Fenster. Wenn es sich bei der Nachricht nicht um eine MDI-Zugriffstaste handelt, gibt die Funktion **false** zurück. in diesem Fall verwendet die Anwendung die [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) -Funktion, um zu bestimmen, ob eine der Anwendungs definierten Zugriffstasten gedrückt wurde. Wenn dies nicht der gibt, sendet die-Schleife die Meldung an die entsprechende Fenster Prozedur.

## <a name="writing-the-frame-window-procedure"></a>Schreiben der Rahmen Fenster Prozedur

Die Fenster Prozedur für ein MDI-Rahmen Fenster ähnelt dem Hauptfenster einer MDI-Anwendung (Non – MDI). Der Unterschied besteht darin, dass eine Rahmen Fenster Prozedur alle Nachrichten, die nicht verarbeitet werden, an die [**defframeproc**](/windows/win32/api/winuser/nf-winuser-defframeproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt. Außerdem muss die Rahmen Fenster Prozedur auch einige Nachrichten übergeben, die Sie verarbeitet, einschließlich der in der folgenden Tabelle aufgeführten Nachrichten.



| `Message`                                  | Antwort                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ Befehl**](../menurc/wm-command.md)     | Aktiviert das untergeordnete MDI-Fenster, das der Benutzer auswählt. Diese Meldung wird gesendet, wenn der Benutzer ein untergeordnetes MDI-Fenster im Menü Fenster des MDI-Frame Fensters auswählt. Die Fenster Kennung, die diese Meldung begleitet, identifiziert das untergeordnete MDI-Fenster, das aktiviert werden soll. |
| [**WM- \_ menuchar**](../menurc/wm-menuchar.md)   | Öffnet das Fenstermenü des aktiven untergeordneten MDI-Fensters, wenn der Benutzer die Tastenkombination Alt + – (minus) drückt.                                                                                                                                                      |
| [**WM- \_ SetFocus**](../inputdev/wm-setfocus.md) | Übergibt den Tastaturfokus an das MDI-Client Fenster, das wiederum an das aktive untergeordnete MDI-Fenster übergibt.                                                                                                                                                         |
| [**WM- \_ Größe**](wm-size.md)              | Ändert die Größe des MDI-Client Fensters an den Client Bereich des neuen Rahmen Fensters. Wenn die Rahmen Fenster Prozedur das MDI-Client Fenster auf eine andere Größe anpasst, sollte die Nachricht nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden.                   |



 

Die Rahmen Fenster Prozedur im MULTIPAD heißt mpframewndproc. Die Verarbeitung anderer Nachrichten durch mpframewndproc ähnelt der von nicht-–-MDI-Anwendungen. [**WM \_ Befehls**](../menurc/wm-command.md) Meldungen im MULTIPAD werden von der lokal definierten CommandHandler-Funktion verarbeitet. Für Befehls Meldungen, die von MULTIPAD nicht verarbeitet werden, ruft CommandHandler die [**defframeproc**](/windows/win32/api/winuser/nf-winuser-defframeproca) -Funktion auf. Wenn MULTIPAD standardmäßig **defframeproc** nicht verwendet, kann der Benutzer ein untergeordnetes Fenster nicht über das Fenstermenü aktivieren, da die durch Klicken auf das Menü Element des Fensters gesendete **WM- \_ Befehls** Nachricht verloren gehen würde.

## <a name="writing-the-child-window-procedure"></a>Schreiben der Prozedur für das untergeordnete Fenster

Wie bei der Rahmen Fenster Prozedur verwendet eine untergeordnete MDI-Fenster Prozedur eine spezielle Funktion für die Verarbeitung von Nachrichten standardmäßig. Alle Nachrichten, die von der untergeordneten Fenster Prozedur nicht behandelt werden, müssen an die [**defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden. Außerdem müssen einige Fenster Verwaltungs Meldungen an **defmdichildproc** übergeben werden, selbst wenn die Anwendung die Nachricht verarbeitet, damit MDI ordnungsgemäß funktioniert. Im folgenden finden Sie die Nachrichten, die von der Anwendung an **defmdichildproc** übergeben werden müssen.



| `Message`                                       | Antwort                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ childaktivierungs**](wm-childactivate.md) | Führt die Aktivierungs Verarbeitung aus, wenn untergeordnete MDI-Fenster verkleinert, verschoben oder angezeigt werden. Diese Nachricht muss übermittelt werden.                                                                                                                                        |
| [**WM \_ getminmaxinfo**](wm-getminmaxinfo.md) | Berechnet die Größe eines untergeordneten MDI-Fensters basierend auf der aktuellen Größe des MDI-Client Fensters.                                                                                                                                                  |
| [**WM- \_ menuchar**](../menurc/wm-menuchar.md)        | Übergibt die Nachricht an das MDI-Rahmen Fenster.                                                                                                                                                                                                               |
| [**WM \_ verschieben**](wm-move.md)                   | Berechnet die MDI-Client Scrollleisten neu, wenn Sie vorhanden sind.                                                                                                                                                                                                 |
| [**WM- \_ SetFocus**](../inputdev/wm-setfocus.md)      | Aktiviert das untergeordnete Fenster, wenn es sich nicht um das aktive untergeordnete MDI-Fenster handelt.                                                                                                                                                                                     |
| [**WM- \_ Größe**](wm-size.md)                   | Führt Vorgänge aus, die zum Ändern der Größe eines Fensters erforderlich sind, insbesondere zum Maximieren oder Wiederherstellen eines untergeordneten MDI-Fensters. Wenn diese Nachricht nicht an die [**defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) -Funktion übergeben wird, entstehen sehr unerwünschte Ergebnisse. |
| [**WM ( \_ syscommand)**](../menurc/wm-syscommand.md)    | Handles (früher als System bezeichnet) Menübefehle: **SC \_ NextWindow**, **SC \_ prevwindow**, **SC \_ Move**, **SC \_ size** und **SC \_ maximi.**                                                                                                        |



 

## <a name="creating-a-child-window"></a>Erstellen eines untergeordneten Fensters

Zum Erstellen eines untergeordneten MDI-Fensters kann eine Anwendung entweder die Funktion " [**anatemdiwindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) " aufrufen oder eine " [**WM \_ mdicreate**](wm-mdicreate.md) "-Meldung an das MDI-Client Fenster senden. (Die Anwendung kann die Funktion "- [**Editor**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " mit dem " **WS \_ Ex \_ MDIChild** "-Stil verwenden, um untergeordnete MDI-Fenster zu erstellen.) In einer MDI-Anwendung mit einem Thread kann eine der beiden Methoden zum Erstellen eines untergeordneten Fensters verwendet werden. Ein Thread in einer Multithread-MDI-Anwendung muss die Funktion " **anatemdiwindow** " oder " **kreatewindowex** " verwenden, um ein untergeordnetes Fenster in einem anderen Thread zu erstellen.

Der *LPARAM* -Parameter einer [**WM- \_ mdicreate**](wm-mdicreate.md) -Meldung ist ein weitaus Zeiger auf eine [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur. Die Struktur enthält vier Dimensions Elemente: **x** und **y**, die die horizontale und vertikale Position des Fensters angeben, sowie **CX** und **CY**, die die horizontalen und vertikalen Blöcke des Fensters angeben. Diese Member können explizit von der Anwendung zugewiesen werden, oder Sie können auf **CW \_ usedefault** festgelegt werden. in diesem Fall wählt das System eine Position, Größe oder beides gemäß einem kaskadierenden Algorithmus aus. In jedem Fall müssen alle vier Member initialisiert werden. MULTIPAD verwendet **CW \_ usedefault** für alle Dimensionen.

Das letzte Element der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur ist der **stilmember** , der möglicherweise stilbits für das Fenster enthält. Zum Erstellen eines untergeordneten MDI-Fensters, das eine beliebige Kombination von Fenster Stilen aufweisen kann, geben Sie den Fenster Stil " **MDIS \_ allchildstyles** " an. Wenn dieses Format nicht angegeben wird, hat ein untergeordnetes MDI-Fenster die Stile " **WS- \_ minimieren**", " **WS \_ maximieren**", " **WS \_ HScroll**" und " **WS \_ VScroll** " als Standardeinstellungen

MULTIPAD erstellt mithilfe der lokal definierten AddFile-Funktion (in der Quelldatei mpfile) die untergeordneten MDI-Fenster. C). Die AddFile-Funktion legt den Titel des untergeordneten Fensters fest, indem der **sztitle** -Member der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur des Fensters entweder dem Namen der bearbeiteten Datei oder der "unbenannten"-Struktur zugewiesen wird. Der **szclass** -Member wird auf den Namen der untergeordneten MDI-Fenster Klasse festgelegt, die in der initializeapplication-Funktion von MULTIPAD registriert ist. Das **howner** -Element wird auf das Instanzhandle der Anwendung festgelegt.

Das folgende Beispiel zeigt die AddFile-Funktion im MULTIPAD.


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



Der Zeiger, der im *LPARAM* -Parameter der [**WM- \_ mdicreate**](wm-mdicreate.md) -Nachricht übergeben wird, wird an die Funktion " [**foratewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " übergeben und als erstes Element in der Struktur "Struktur erstellen" angezeigt, das [**in der "**](/windows/win32/api/winuser/ns-winuser-createstructa) [**WM \_ Create**](wm-create.md) "-Nachricht übergeben wird. Im MULTIPAD initialisiert das untergeordnete Fenster während der **WM \_** die Nachrichtenverarbeitung, indem Dokument Variablen in den zusätzlichen Daten initialisiert werden und das untergeordnete Fenster des Bearbeitungs Steuer Elements erstellt wird.

 

 
