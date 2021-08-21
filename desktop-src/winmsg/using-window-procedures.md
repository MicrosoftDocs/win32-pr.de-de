---
description: In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben im Zusammenhang mit Fensterverfahren durchgeführt werden.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Verwenden von Fenster-Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05e5999b216ad8c51be4de6fdec80b5f58ff94956f8c1129d74c3f7075a90eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028298"
---
# <a name="using-window-procedures"></a>Verwenden von Fenster-Prozeduren

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben im Zusammenhang mit Fensterverfahren durchgeführt werden.

-   [Entwerfen einer Fensterprozedur](#designing-a-window-procedure)
-   [Zuordnen einer Fensterprozedur zu einer Window-Klasse](#associating-a-window-procedure-with-a-window-class)
-   [Unterklassen eines Fensters](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Entwerfen einer Fensterprozedur

Das folgende Beispiel zeigt die Struktur einer typischen Fensterprozedur. Die Fensterprozedur verwendet das Meldungsargument in einer **switch-Anweisung** mit einzelnen Meldungen, die von separaten **Case-Anweisungen verarbeitet** werden. Beachten Sie, dass jeder Fall einen bestimmten Wert für jede Nachricht zurückgibt. Bei Nachrichten, die nicht von der Fensterprozedur verarbeiten werden, ruft die Fensterprozedur [**die DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf.


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



Die [**WM \_ NCCREATE-Nachricht**](wm-nccreate.md) wird direkt nach dem Erstellen des Fensters gesendet. Wenn eine Anwendung jedoch auf diese Nachricht antwortet, indem **false** zurückgegeben wird, schlägt die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) fehl. Die [**WM \_ CREATE-Nachricht**](wm-create.md) wird gesendet, nachdem Ihr Fenster bereits erstellt wurde.

Die [**WM \_ DESTROY-Nachricht**](wm-destroy.md) wird gesendet, wenn Ihr Fenster zerstört werden soll. Die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) kümmert sich darum, alle untergeordneten Fenster des zu zerstörenden Fensters zu zerstören. Die [**WM \_ NCDESTROY-Nachricht**](wm-ncdestroy.md) wird gesendet, kurz bevor ein Fenster zerstört wird.

Zumindest sollte eine Fensterprozedur die [**WM \_ PAINT-Nachricht**](../gdi/wm-paint.md) verarbeiten, um sich selbst zu zeichnen. In der Regel sollten auch Maus- und Tastaturmeldungen verarbeitet werden. Sehen Sie sich die Beschreibungen einzelner Meldungen an, um zu bestimmen, ob sie von der Fensterprozedur verarbeitet werden sollen.

Ihre Anwendung kann die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) im Rahmen der Verarbeitung einer Nachricht aufrufen. In einem solchen Fall kann die Anwendung die Nachrichtenparameter ändern, bevor die Nachricht an **DefWindowProc** übergeben wird, oder sie kann die Standardverarbeitung fortsetzen, nachdem sie eigene Vorgänge ausführen.

Eine Dialogfeldprozedur empfängt eine [**WM \_ INITDIALOG-Nachricht**](../dlgbox/wm-initdialog.md) anstelle einer [**WM \_ CREATE-Nachricht**](wm-create.md) und über gibt keine nicht verarbeiteten Nachrichten an die [**DefDlgProc-Funktion**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) weiter. Andernfalls ist eine Dialogfeldprozedur identisch mit einer Fensterprozedur.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Zuordnen einer Fensterprozedur zu einer Fensterklasse

Sie ordnen eine Fensterprozedur einer Fensterklasse zu, wenn Sie die Klasse registrieren. Sie müssen eine [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) mit Informationen zur -Klasse füllen, und der **lpfnWndProc-Member** muss die Adresse der Fensterprozedur angeben. Um die Klasse zu registrieren, übergeben Sie die Adresse der **WNDCLASS-Struktur** an die [**RegisterClass-Funktion.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Nachdem die Fensterklasse registriert wurde, wird die Fensterprozedur automatisch jedem neuen Fenster zugeordnet, das mit dieser Klasse erstellt wurde.

Das folgende Beispiel zeigt, wie die Fensterprozedur im vorherigen Beispiel einer Fensterklasse zugeordnet wird.


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a>Unterklassen eines Fensters

Um eine Instanz eines Fensters als Unterklasse zu verwenden, rufen Sie die [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) auf, und geben Sie das Handle für das Fenster an, um das GWL WNDPROC-Flag und einen Zeiger auf die Unterklassenprozedur zu \_ untergliedern. **SetWindowLong gibt** einen Zeiger auf die ursprüngliche Fensterprozedur zurück. Verwenden Sie diesen Zeiger, um Nachrichten an die ursprüngliche Prozedur zu übergeben. Die Unterklassenfensterprozedur muss die [**CallWindowProc-Funktion**](/windows/win32/api/winuser/nf-winuser-callwindowproca) verwenden, um die ursprüngliche Fensterprozedur auf aufruft.

> [!Note]  
> Um Code zu schreiben, der sowohl mit 32-Bit- als auch mit 64-Bit-Versionen von Windows kompatibel ist, verwenden Sie die [**SetWindowLongPtr-Funktion.**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

 

Im folgenden Beispiel wird gezeigt, wie eine Instanz eines Bearbeitungssteuerfelds in einem Dialogfeld untergliedert wird. Mit der Unterklassenfensterprozedur kann das Bearbeitungssteuerfeld alle Tastatureingaben empfangen, einschließlich der EINGABETASTE und DER TAB-TASTE, wenn das Steuerelement den Eingabefokus besitzt.


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
