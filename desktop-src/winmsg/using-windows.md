---
description: In den Beispielen in diesem Abschnitt wird beschrieben, wie mit Windows verbundene Aufgaben ausgeführt werden.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Verwenden von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867988"
---
# <a name="using-windows"></a>Verwenden von Windows

In den Beispielen in diesem Abschnitt wird beschrieben, wie die folgenden Aufgaben ausgeführt werden:

-   [Erstellen eines Hauptfensters](#creating-a-main-window)
-   [Erstellen, auflisten und Größenanpassung von untergeordneten Fenstern](#creating-enumerating-and-sizing-child-windows)
-   [Zerstören eines Fensters](#destroying-a-window)
-   [Verwenden von geschichteten Fenstern](#using-layered-windows)

## <a name="creating-a-main-window"></a>Erstellen eines Hauptfensters

Das erste Fenster, das eine Anwendung erstellt, ist in der Regel das Hauptfenster. Sie erstellen das Hauptfenster mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " und geben die Fenster Klasse, den Fensternamen, die Fenster Stile, die Größe, die Position, das Menü handle, das Instanzhandle und die Erstellungs Daten an. Ein Hauptfenster gehört zu einer von der Anwendung definierten Fenster Klasse, sodass Sie die Fenster Klasse registrieren und eine Fenster Prozedur für die Klasse bereitstellen müssen, bevor Sie das Hauptfenster erstellen.

Die meisten Anwendungen verwenden normalerweise den [**WS \_ overlappedwindow**](window-styles.md) -Stil, um das Hauptfenster zu erstellen. Dieser Stil gibt dem Fenster eine Titelleiste, ein Fenstermenü, einen Größen Anpassungsrahmen und Schaltflächen zum minimieren und maximieren. Die Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " gibt ein Handle zurück, das das Fenster eindeutig identifiziert.

Im folgenden Beispiel wird ein Hauptfenster erstellt, das zu einer Anwendungs definierten Fenster Klasse gehört. Der Fenster Name, das **Hauptfenster**, wird in der Titelleiste des Fensters angezeigt. Durch die Kombination der [**WS- \_ VScroll**](window-styles.md) -und **WS \_ HScroll** -Stile mit dem **WS \_ overlappedwindow** -Stil erstellt die Anwendung ein Hauptfenster mit horizontalen und vertikalen Schiebe leisten zusätzlich zu den Komponenten, die vom **WS \_ overlappedwindow** -Stil bereitgestellt werden. Die vier Vorkommen der **CW \_ usedefault** -Konstante legen die anfängliche Größe und Position des Fensters auf die vom System definierten Standardwerte fest. Wenn Sie anstelle eines Menü Handles **null** angeben, wird im Fenster das Menü für die Fenster Klasse definiert.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



Beachten Sie, dass im vorherigen Beispiel die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion aufgerufen wird, nachdem das Hauptfenster erstellt wurde. Dies geschieht, da das System nach dem Erstellen nicht automatisch das Hauptfenster anzeigt. Durch die Übergabe des " **SW \_ showdefault** "-Flags an **ShowWindow** ermöglicht die Anwendung dem Programm, das die Anwendung gestartet hat, den anfänglichen Anzeige Zustand des Hauptfensters festzulegen. Die [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) -Funktion sendet das Fenster als erste WM-Zeichnungs Nachricht. [**\_**](../gdi/wm-paint.md)

## <a name="creating-enumerating-and-sizing-child-windows"></a>Erstellen, auflisten und Größenanpassung von untergeordneten Fenstern

Mithilfe von untergeordneten Fenstern können Sie den Client Bereich eines Fensters in andere Funktionsbereiche aufteilen. Das Erstellen eines untergeordneten Fensters ähnelt dem Erstellen eines Hauptfensters – Sie verwenden die Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ". Wenn Sie ein Fenster einer Anwendungs definierten Fenster Klasse erstellen möchten, müssen Sie die Fenster Klasse registrieren und eine Fenster Prozedur bereitstellen, bevor Sie das untergeordnete Fenster erstellen. Sie müssen dem untergeordneten Fenster den untergeordneten [**WS \_**](window-styles.md) -Stil geben und ein übergeordnetes Fenster für das untergeordnete Fenster angeben, wenn Sie es erstellen.

Im folgenden Beispiel wird der Client Bereich des Hauptfensters einer Anwendung in drei Funktionsbereiche aufgeteilt, indem drei untergeordnete Fenster der gleichen Größe erstellt werden. Jedes untergeordnete Fenster hat dieselbe Höhe wie der Client Bereich des Hauptfensters, jede Breite ist jedoch ein Drittel. Im Hauptfenster werden die untergeordneten Fenster als Antwort auf die [**WM \_ Create**](wm-create.md) -Nachricht erstellt, die das Hauptfenster während des eigenen Fenster Erstellungs Prozesses empfängt. Da jedes untergeordnete Fenster die [**WS \_**](window-styles.md) -Rahmenart hat, weist jedes untergeordnete Fenster einen schmalen Linien Rahmen auf. Da der nicht **\_ sichtbare WS** -Stil nicht angegeben ist, wird jedes untergeordnete Fenster anfänglich ausgeblendet. Beachten Sie auch, dass jedes untergeordnete Fenster einem untergeordneten Fenster Bezeichner zugewiesen wird.

Im Hauptfenster werden die untergeordneten Fenster als Antwort auf die [**WM- \_ Größen**](wm-size.md) Nachricht angezeigt, die das Hauptfenster empfängt, wenn sich die Größe ändert. Als Antwort auf die **WM- \_ Größe** Ruft das Hauptfenster die Dimensionen seines Client Bereichs mithilfe der [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) -Funktion ab und übergibt dann die Dimensionen an die [**enumchildwindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) -Funktion. **Enumchildwindows** übergibt das Handle wiederum an jedes untergeordnete Fenster an die Anwendungs definierte [**enumchildproc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) -Rückruffunktion. Mit dieser Funktion wird jedes untergeordnete Fenster durch Aufrufen der Funktion " [**vwindow**](/windows/win32/api/winuser/nf-winuser-movewindow) " Größe und Position positioniert. Größe und Position basieren auf den Abmessungen des Client Bereichs des Hauptfensters und dem Bezeichner des untergeordneten Fensters. Danach ruft **enumchildproc** die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion auf, um das Fenster sichtbar zu machen.


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a>Zerstören eines Fensters

Sie können die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion verwenden, um ein Fenster zu zerstören. Normalerweise sendet eine Anwendung die " [**WM \_ Close**](wm-close.md) "-Nachricht, bevor ein Fenster zerstört wird, sodass dem Fenster die Möglichkeit gegeben wird, den Benutzer zur Bestätigung aufzufordern, bevor das Fenster zerstört wird. Ein Fenster, in dem ein Fenstermenü enthalten ist, erhält automatisch die Meldung zum **\_ Schließen der WM** , wenn der Benutzer im Menü Fenster auf **Schließen** klickt. Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, ruft die Anwendung **DestroyWindow** auf. Das System sendet die [**WM- \_ zerstörungsmeldung**](wm-destroy.md) an das Fenster, nachdem es vom Bildschirm entfernt wurde. Als Antwort auf **WM \_ Destroy** speichert das Fenster seine Daten und gibt alle zugeordneten Ressourcen frei. Ein Hauptfenster beendet die Verarbeitung von **WM- \_ Zerstörung** durch Aufrufen der [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion, um die Anwendung zu beenden.

Im folgenden Beispiel wird gezeigt, wie Sie vor dem Zerstören eines Fensters zur Bestätigung des Benutzers aufgefordert werden. Als Antwort auf [**" \_ WM close**](wm-close.md)" zeigt das Beispiel ein Dialogfeld an, das die Schaltflächen **Ja**, **Nein** und **Abbrechen** enthält. Wenn der Benutzer auf **Ja** klickt, wird [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) aufgerufen. Andernfalls wird das Fenster nicht zerstört. Da das Fenster, das zerstört wird, ein Hauptfenster ist, wird [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) im Beispiel als Antwort auf [**WM \_ Destroy**](wm-destroy.md)aufgerufen.


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a>Verwenden von geschichteten Fenstern

Wenn ein Dialogfeld als durchlässiges Fenster angezeigt werden soll, erstellen Sie zuerst das Dialogfeld wie üblich. Legen Sie dann bei [**WM \_ InitDialog**](../dlgbox/wm-initdialog.md)das geschichtete Bit des erweiterten Stils des Fensters fest, und nennen Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) mit dem gewünschten Alpha-Wert. Der Code könnte wie folgt aussehen:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Beachten Sie, dass der dritte Parameter von [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ein Wert zwischen 0 und 255 ist, wobei 0 das Fenster vollständig transparent ist und 255 vollständig deckend ist. Dieser Parameter imitiert die vielseitigere [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) der [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) -Funktion.

Um dieses Fenster wieder vollständig zu deinstallieren, entfernen Sie das überlappende **WS \_ Ex \_** -Bit, indem Sie [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und dann das Fenster zum Umzeichnen auffordern. Das Entfernen des Bits ist erwünscht, damit das System weiß, dass es Arbeitsspeicher freigeben kann, der mit der Schichtung und Umleitung verknüpft ist. Der Code könnte wie folgt aussehen:


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



Um untergeordnete Fenster mit Ebenen zu verwenden, muss die Anwendung Windows 8-fähig im Manifest deklarieren.

 

 
