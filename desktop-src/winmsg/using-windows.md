---
description: In den Beispielen in diesem Abschnitt wird beschrieben, wie Aufgaben im Zusammenhang mit der Verwendung von Fenstern ausgeführt werden.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Verwenden von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75681987a4bc012618135f666b3ff973880b8129d2ad1ee896bcdbed266d179d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436966"
---
# <a name="using-windows"></a>Verwenden von Windows

In den Beispielen in diesem Abschnitt wird beschrieben, wie die folgenden Aufgaben ausgeführt werden:

-   [Erstellen eines Hauptfensters](#creating-a-main-window)
-   [Erstellen, Aufzählen und Dimensionieren von untergeordneten Windows](#creating-enumerating-and-sizing-child-windows)
-   [Zerstören eines Fensters](#destroying-a-window)
-   [Verwenden von mehrstufigen Windows](#using-layered-windows)

## <a name="creating-a-main-window"></a>Erstellen eines Hauptfensters

Das erste Fenster, das eine Anwendung erstellt, ist in der Regel das Hauptfenster. Sie erstellen das Hauptfenster mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) und geben die Fensterklasse, den Fensternamen, die Fensterstile, die Größe, die Position, das Menühandle, das Instanzhandle und die Erstellungsdaten an. Ein Hauptfenster gehört zu einer von der Anwendung definierten Fensterklasse. Daher müssen Sie die Fensterklasse registrieren und eine Fensterprozedur für die Klasse bereitstellen, bevor Sie das Hauptfenster erstellen.

Die meisten Anwendungen verwenden in der Regel den [**WS \_ OVERLAPPEDWINDOW-Stil,**](window-styles.md) um das Hauptfenster zu erstellen. Dieser Stil bietet dem Fenster eine Titelleiste, ein Fenstermenü, einen Größenrahmen sowie Schaltflächen zum Minimieren und Maximieren. Die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) gibt ein Handle zurück, das das Fenster eindeutig identifiziert.

Im folgenden Beispiel wird ein Hauptfenster erstellt, das zu einer von der Anwendung definierten Fensterklasse gehört. Der Fenstername **Hauptfenster** wird in der Titelleiste des Fensters angezeigt. Durch kombinieren der [**WS \_ VSCROLL-**](window-styles.md) und **WS \_ HSCROLL-Stil** mit dem **WS \_ OVERLAPPEDWINDOW-Stil** erstellt die Anwendung ein Hauptfenster mit horizontalen und vertikalen Scrollleisten zusätzlich zu den Komponenten, die vom **WS \_ OVERLAPPEDWINDOW-Stil** bereitgestellt werden. Die vier Vorkommen der **CW \_ USEDEFAULT-Konstante** legen die Anfangsgröße und Position des Fensters auf die vom System definierten Standardwerte fest. Wenn **Sie NULL** anstelle eines Menühandle angeben, wird für das Fenster das Menü für die Fensterklasse definiert.


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



Beachten Sie, dass im vorherigen Beispiel die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) nach dem Erstellen des Hauptfensters aufruft. Dies geschieht, da das System das Hauptfenster nach der Erstellung nicht automatisch anzeigt. Durch Übergeben des **SW \_ SHOWDEFAULT-Flags** an **ShowWindow** ermöglicht die Anwendung dem Programm, das die Anwendung gestartet hat, den anfänglichen Showzustand des Hauptfensters festzulegen. Die [**UpdateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-updatewindow) sendet die erste [**WM \_ PAINT-Meldung**](../gdi/wm-paint.md) an das Fenster.

## <a name="creating-enumerating-and-sizing-child-windows"></a>Erstellen, Aufzählen und Dimensionieren von untergeordneten Windows

Sie können den Clientbereich eines Fensters mithilfe von untergeordneten Fenstern in verschiedene Funktionsbereiche unterteilen. Das Erstellen eines untergeordneten Fensters entspricht dem Erstellen eines Hauptfensters– Sie verwenden die [**CreateWindowEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Um ein Fenster einer anwendungsdefinierte Fensterklasse zu erstellen, müssen Sie die Fensterklasse registrieren und vor dem Erstellen des untergeordneten Fensters eine Fensterprozedur bereitstellen. Sie müssen dem untergeordneten Fenster das [**WS \_ CHILD-Format**](window-styles.md) geben und beim Erstellen ein übergeordnetes Fenster für das untergeordnete Fenster angeben.

Im folgenden Beispiel wird der Clientbereich des Hauptfensters einer Anwendung in drei Funktionsbereiche unterteilt, indem drei untergeordnete Fenster gleicher Größe erstellt werden. Jedes untergeordnete Fenster hat die gleiche Höhe wie der Clientbereich des Hauptfensters, aber jedes ist ein Drittel seiner Breite. Das Hauptfenster erstellt die untergeordneten Fenster als Reaktion auf die [**WM \_ CREATE-Meldung,**](wm-create.md) die das Hauptfenster während seines eigenen Fenstererstellungsprozesses empfängt. Da jedes untergeordnete Fenster den [**WS \_ BORDER-Stil**](window-styles.md) auf hat, verfügt jedes über einen schlanken Linienrahmen. Da der **WS \_ VISIBLE-Stil** nicht angegeben ist, wird jedes untergeordnete Fenster anfänglich ausgeblendet. Beachten Sie auch, dass jedem untergeordneten Fenster ein Bezeichner für untergeordnete Fenster zugewiesen wird.

Das Hauptfenster dimensioniert und positioniert die untergeordneten Fenster als Reaktion auf die [**WM \_ SIZE-Meldung,**](wm-size.md) die das Hauptfenster empfängt, wenn sich seine Größe ändert. Als Reaktion auf **WM \_ SIZE** ruft das Hauptfenster die Dimensionen seines Clientbereichs mithilfe der [**GetClientRect-Funktion**](/windows/win32/api/winuser/nf-winuser-getclientrect) ab und übergibt die Dimensionen dann an die [**EnumChildWindows-Funktion.**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) **EnumChildWindows** übergibt das Handle an jedes untergeordnete Fenster wiederum an die anwendungsdefinierte [**Rückruffunktion EnumChildProc.**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) Diese Funktion größent und positioniert jedes untergeordnete Fenster, indem die [**MoveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-movewindow) aufgerufen wird. Größe und Position basieren auf den Abmessungen des Clientbereichs des Hauptfensters und dem Bezeichner des untergeordneten Fensters. Anschließend ruft **EnumChildProc** die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) auf, um das Fenster sichtbar zu machen.


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

Sie können die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) verwenden, um ein Fenster zu zerstören. In der Regel sendet eine Anwendung die [**WM \_ CLOSE-Nachricht,**](wm-close.md) bevor ein Fenster zerstört wird, und gibt dem Fenster die Möglichkeit, den Benutzer zur Bestätigung aufzufordern, bevor das Fenster zerstört wird. Ein Fenster, das ein Fenstermenü enthält, empfängt automatisch die **WM \_ CLOSE-Meldung,** wenn der Benutzer im Fenstermenü auf **Schließen** klickt. Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, ruft die Anwendung **DestroyWindow** auf. Das System sendet die [**WM \_ DESTROY-Nachricht**](wm-destroy.md) an das Fenster, nachdem es sie vom Bildschirm entfernt hat. Als Reaktion auf **WM \_ DESTROY** speichert das Fenster seine Daten und gibt alle zugeordneten Ressourcen frei. Ein Hauptfenster schließt die Verarbeitung von **WM \_ DESTROY** ab, indem die [**PostQuitMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postquitmessage) aufgerufen wird, um die Anwendung zu beenden.

Das folgende Beispiel zeigt, wie Sie vor dem Zerstören eines Fensters zur Bestätigung des Benutzers auffordern. Als Reaktion auf [**WM \_ CLOSE**](wm-close.md)zeigt das Beispiel ein Dialogfeld an, das die Schaltflächen **Ja,** **Nein** und **Abbrechen** enthält. Wenn der Benutzer auf **Ja** klickt, wird [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) aufgerufen. Andernfalls wird das Fenster nicht zerstört. Da das zu zerstörende Fenster ein Hauptfenster ist, ruft das Beispiel [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) als Reaktion auf [**WM \_ DESTROY**](wm-destroy.md)auf.


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



## <a name="using-layered-windows"></a>Verwenden von mehrstufigen Windows

Damit ein Dialogfeld als durchscheinendes Fenster angezeigt wird, erstellen Sie den Dialog zunächst wie gewohnt. Legen Sie dann auf [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)das mehrstufige Bit des erweiterten Stils des Fensters fest, und rufen [**Sie SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) mit dem gewünschten Alphawert auf. Der Code könnte wie folgt aussehen:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Beachten Sie, dass der dritte Parameter von [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ein Wert ist, der zwischen 0 und 255 liegt. 0 macht das Fenster vollständig transparent und 255 macht es vollständig deckend. Dieser Parameter imitiert die vielseitigere [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) der [**AlphaBlend-Funktion.**](/windows/win32/api/wingdi/nf-wingdi-alphablend)

Um dieses Fenster wieder vollständig deckend zu gestalten, entfernen Sie das **WS \_ EX \_ LAYERED-Bit,** indem [**Sie SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und dann das Fenster zum erneuten Anstrich auffordern. Das Entfernen des Bits soll das System darüber informieren, dass es speicherplatzauflösen kann, der mit der Schichtung und Umleitung verbunden ist. Der Code könnte wie folgt aussehen:


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



Um mehrstufige untergeordnete Fenster verwenden zu können, muss sich die Anwendung Windows 8 im Manifest selbst deklarieren.

 

 
