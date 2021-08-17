---
description: In den Beispielen in diesem Abschnitt wird beschrieben, wie Mithilfe von Fenstern verbundene Aufgaben ausgeführt werden.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Verwenden Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75681987a4bc012618135f666b3ff973880b8129d2ad1ee896bcdbed266d179d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436966"
---
# <a name="using-windows"></a>Verwenden Windows

In den Beispielen in diesem Abschnitt wird beschrieben, wie die folgenden Aufgaben auszuführen sind:

-   [Erstellen eines Hauptfensters](#creating-a-main-window)
-   [Erstellen, Aufzählen und Sizing child Windows](#creating-enumerating-and-sizing-child-windows)
-   [Zerstören eines Fensters](#destroying-a-window)
-   [Verwenden von mehrschichtigen Windows](#using-layered-windows)

## <a name="creating-a-main-window"></a>Erstellen eines Hauptfensters

Das erste Fenster, das eine Anwendung erstellt, ist in der Regel das Hauptfenster. Sie erstellen das Hauptfenster mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) und geben die Fensterklasse, den Fensternamen, Fensterstile, größe, position, menü handle, instanz handle und erstellungsdaten an. Ein Hauptfenster gehört zu einer anwendungsdefinierten Fensterklasse, daher müssen Sie die Fensterklasse registrieren und eine Fensterprozedur für die Klasse bereitstellen, bevor Sie das Hauptfenster erstellen.

Die meisten Anwendungen verwenden in der Regel den [**WS \_ OVERLAPPEDWINDOW-Stil,**](window-styles.md) um das Hauptfenster zu erstellen. Mit diesem Stil erhält das Fenster eine Titelleiste, ein Fenstermenü, einen Größenrahmen sowie Schaltflächen zum Minimieren und Maximieren. Die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) gibt ein Handle zurück, das das Fenster eindeutig identifiziert.

Im folgenden Beispiel wird ein Hauptfenster erstellt, das zu einer anwendungsdefinierten Fensterklasse gehört. Der Fenstername **Hauptfenster** wird in der Titelleiste des Fensters angezeigt. Durch kombinieren der [**WS \_ VSCROLL-**](window-styles.md) und **\_ WS HSCROLL-Stil** mit dem **WS \_ OVERLAPPEDWINDOW-Stil** erstellt die Anwendung zusätzlich zu den Komponenten, die vom **WS \_ OVERLAPPEDWINDOW-Stil** bereitgestellt werden, ein Hauptfenster mit horizontalen und vertikalen Scrollleisten. Die vier Vorkommen der **CW \_ USEDEFAULT-Konstante** legen die Anfangsgröße und -position des Fensters auf die systemdefinierten Standardwerte fest. Durch Angeben von **NULL** anstelle eines Menühandpunkts wird für das Fenster das Menü für die Fensterklasse definiert.


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



Beachten Sie, dass im vorherigen Beispiel die [**ShowWindow-Funktion nach**](/windows/win32/api/winuser/nf-winuser-showwindow) dem Erstellen des Hauptfensters aufruft. Dies geschieht, da das System das Hauptfenster nach der Erstellung nicht automatisch an angezeigt. Durch Übergeben des **SW \_ SHOWDEFAULT-Flags** an **ShowWindow** ermöglicht die Anwendung dem Programm, das die Anwendung gestartet hat, das Festlegen des anfänglichen Showzustands des Hauptfensters. Die [**UpdateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-updatewindow) sendet dem Fenster die erste [**WM \_ PAINT-Nachricht.**](../gdi/wm-paint.md)

## <a name="creating-enumerating-and-sizing-child-windows"></a>Erstellen, Aufzählen und Anpassen der Größe untergeordneter Windows

Sie können den Clientbereich eines Fensters mithilfe von untergeordneten Fenstern in verschiedene Funktionsbereiche unterteilen. Das Erstellen eines untergeordneten Fensters ist wie das Erstellen eines Hauptfensters. Sie verwenden die [**CreateWindowEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Um ein Fenster einer anwendungsdefinierten Fensterklasse zu erstellen, müssen Sie die Fensterklasse registrieren und eine Fensterprozedur bereitstellen, bevor Sie das untergeordnete Fenster erstellen. Sie müssen dem untergeordneten Fenster den [**WS \_ CHILD-Stil**](window-styles.md) geben und beim Erstellen ein übergeordnetes Fenster für das untergeordnete Fenster angeben.

Im folgenden Beispiel wird der Clientbereich des Hauptfensters einer Anwendung in drei Funktionsbereiche unterteilt, indem drei untergeordnete Fenster gleicher Größe erstellt werden. Jedes untergeordnete Fenster hat die gleiche Höhe wie der Clientbereich des Hauptfensters, aber jedes ist ein Drittel seiner Breite. Das Hauptfenster erstellt die untergeordneten Fenster als Reaktion auf die [**WM \_ CREATE-Nachricht,**](wm-create.md) die das Hauptfenster während seines eigenen Fenstererstellungsprozesses empfängt. Da jedes untergeordnete Fenster den [**Stil WS \_ BORDER**](window-styles.md) auf hat, verfügt jedes über einen schlanken Rahmen. Da der **WS \_ VISIBLE-Stil** nicht angegeben ist, wird jedes untergeordnete Fenster anfänglich ausgeblendet. Beachten Sie auch, dass jedem untergeordneten Fenster ein Untergeordneter Fensterbezeichner zugewiesen ist.

Das Hauptfenster wird als Reaktion auf die [**WM \_ SIZE-Meldung,**](wm-size.md) die das Hauptfenster empfängt, wenn sich seine Größe ändert, die Größe der untergeordneten Fenster ändert, und positioniert. Als Reaktion auf **WM \_ SIZE** ruft das Hauptfenster die Dimensionen seines Clientbereichs mithilfe der [**GetClientRect-Funktion**](/windows/win32/api/winuser/nf-winuser-getclientrect) ab und übergibt die Dimensionen dann an die [**EnumChildWindows-Funktion.**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) **EnumChildWindows** übergibt das Handle wiederum an jedes untergeordnete Fenster an die anwendungsdefinierte [**EnumChildProc-Rückruffunktion.**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) Diese Funktion größe und positioniert jedes untergeordnete Fenster durch Aufrufen der [**MoveWindow-Funktion.**](/windows/win32/api/winuser/nf-winuser-movewindow) Die Größe und Position basieren auf den Dimensionen des Clientbereichs des Hauptfensters und dem Bezeichner des untergeordneten Fensters. Anschließend ruft **EnumChildProc** die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) auf, um das Fenster sichtbar zu machen.


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

Sie können die [**DestroyWindow-Funktion verwenden,**](/windows/win32/api/winuser/nf-winuser-destroywindow) um ein Fenster zu zerstören. In der Regel sendet eine Anwendung die [**WM \_ CLOSE-Nachricht,**](wm-close.md) bevor ein Fenster zerstört wird, und gibt dem Fenster die Möglichkeit, den Benutzer zur Bestätigung aufforderungen, bevor das Fenster zerstört wird. Ein Fenster, das ein Fenstermenü enthält, empfängt automatisch  die **WM \_ CLOSE-Meldung,** wenn der Benutzer im Fenstermenü auf Schließen klickt. Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, ruft die Anwendung **DestroyWindow auf.** Das System sendet die [**WM \_ DESTROY-Nachricht**](wm-destroy.md) an das Fenster, nachdem es vom Bildschirm entfernt wurde. Als Reaktion auf **WM \_ DESTROY** speichert das Fenster seine Daten und gibt alle zugeordneten Ressourcen frei. Ein Hauptfenster beendet die Verarbeitung von **WM \_ DESTROY** durch Aufrufen der [**PostQuitMessage-Funktion,**](/windows/win32/api/winuser/nf-winuser-postquitmessage) um die Anwendung zu beenden.

Das folgende Beispiel zeigt, wie Sie zur Bestätigung des Benutzers auffordern, bevor Sie ein Fenster zerstören. Als Reaktion auf [**WM \_ CLOSE zeigt**](wm-close.md)das Beispiel ein Dialogfeld an, das die Schaltflächen Ja, **Nein** und **Abbrechen** enthält.  Wenn der Benutzer auf Ja **klickt,** [**wird DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) aufgerufen. Andernfalls wird das Fenster nicht zerstört. Da das zerstörte Fenster ein Hauptfenster ist, ruft das Beispiel [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) als Antwort auf [**WM DESTROY \_ auf.**](wm-destroy.md)


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



## <a name="using-layered-windows"></a>Verwenden von mehrschichtigen Windows

Damit ein Dialogfeld als durchscheinendes Fenster angezeigt wird, erstellen Sie den Dialog zunächst wie gewohnt. Legen Sie dann [**bei WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)das mehrschichtige Bit des erweiterten Stils des Fensters fest, und rufen Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) mit dem gewünschten Alphawert auf. Der Code könnte wie im folgenden Beispiel aussehen:


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



Beachten Sie, dass der dritte Parameter von [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ein Wert zwischen 0 und 255 ist, bei dem 0 das Fenster vollständig transparent und 255 vollständig deckend macht. Dieser Parameter imitiert die vielseitigeren [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) der [**AlphaBlend-Funktion.**](/windows/win32/api/wingdi/nf-wingdi-alphablend)

Um dieses Fenster wieder vollständig undurchsichtig zu machen, entfernen Sie das **WS \_ EX \_ LAYERED-Bit,** indem Sie [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und dann das Fenster bitten, sich neu zu erstellen. Das Entfernen des Bits soll das System darüber informieren, dass es Speicher frei geben kann, der mit Ebenen und Umleitungen verbunden ist. Der Code könnte wie im folgenden Beispiel aussehen:


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



Um übergeordnete untergeordnete Fenster zu verwenden, muss sich die Anwendung selbst Windows 8 im Manifest deklarieren.

 

 
