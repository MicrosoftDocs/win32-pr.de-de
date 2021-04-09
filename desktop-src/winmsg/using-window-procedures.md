---
description: In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben für Fenster Prozeduren ausgeführt werden.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Verwenden von Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867991"
---
# <a name="using-window-procedures"></a>Verwenden von Window

In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben für Fenster Prozeduren ausgeführt werden.

-   [Entwerfen einer Fenster Prozedur](#designing-a-window-procedure)
-   [Zuordnen einer Fenster Prozedur zu einer Fenster Klasse](#associating-a-window-procedure-with-a-window-class)
-   [Unterklassen eines Fensters](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a>Entwerfen einer Fenster Prozedur

Das folgende Beispiel zeigt die Struktur einer typischen Fenster Prozedur. Die Fenster Prozedur verwendet das Message-Argument in einer **Switch** -Anweisung mit einzelnen Nachrichten, die von separaten **Case** -Anweisungen verarbeitet werden. Beachten Sie, dass jeder Fall einen bestimmten Wert für jede Nachricht zurückgibt. Bei Nachrichten, die nicht verarbeitet werden, ruft die Fenster Prozedur die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf.


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



Die [**WM- \_ nccreate**](wm-nccreate.md) -Nachricht wird gesendet, nachdem das Fenster erstellt wurde. Wenn jedoch eine Anwendung auf diese Meldung antwortet, indem Sie **false** zurückgibt, schlägt die Funktion " [**deatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " fehl. Die [**WM \_ Create**](wm-create.md) -Nachricht wird gesendet, nachdem das Fenster bereits erstellt wurde.

Die [**WM- \_ zerstörungsmeldung**](wm-destroy.md) wird gesendet, wenn das Fenster zerstört wird. Mit der [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion werden alle untergeordneten Fenster des Fensters zerstört, das zerstört wird. Die [**WM \_ ncdestroy**](wm-ncdestroy.md) -Nachricht wird gesendet, kurz bevor ein Fenster zerstört wird.

Eine Fenster Prozedur sollte mindestens die WM-Zeichnungs Nachricht verarbeiten [**, \_**](../gdi/wm-paint.md) um sich selbst zu zeichnen. In der Regel sollten auch Maus-und Tastatur Meldungen behandelt werden. Überprüfen Sie die Beschreibungen einzelner Nachrichten, um zu bestimmen, ob Sie von ihrer Fenster Prozedur behandelt werden sollen.

Die Anwendung kann die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Teil der Verarbeitung einer Nachricht aufzurufen. In einem solchen Fall kann die Anwendung die Nachrichten Parameter ändern, bevor Sie die Nachricht an **defwindowproc** übergibt, oder Sie kann mit der Standard Verarbeitung fortfahren, nachdem Sie Ihre eigenen Vorgänge ausgeführt hat.

Eine Dialogfeld Prozedur empfängt eine [**WM- \_ InitDialog**](../dlgbox/wm-initdialog.md) -Nachricht anstelle einer [**WM \_ Create**](wm-create.md) -Meldung und übergibt keine nicht verarbeiteten Nachrichten an die [**defdlgproc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) -Funktion. Andernfalls ist eine Dialogfeld Prozedur genauso wie eine Fenster Prozedur.

## <a name="associating-a-window-procedure-with-a-window-class"></a>Zuordnen einer Fenster Prozedur zu einer Fenster Klasse

Beim Registrieren der Klasse wird eine Fenster Prozedur mit einer Fenster Klasse verknüpft. Sie müssen eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur mit Informationen über die-Klasse ausfüllen, und das **lpfnwndproc** -Element muss die Adresse der Fenster Prozedur angeben. Übergeben Sie die Adresse der **WNDCLASS** -Struktur an die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion, um die Klasse zu registrieren. Nachdem die Fenster Klasse registriert wurde, wird die Fenster Prozedur automatisch jedem neuen Fenster zugeordnet, das mit dieser Klasse erstellt wird.

Im folgenden Beispiel wird gezeigt, wie Sie die Fenster Prozedur im vorherigen Beispiel einer Fenster Klasse zuordnen.


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

Um eine Unterklasse einer Instanz eines Fensters zu unterteilen, müssen Sie die Funktion [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und das Handle für das Fenster angeben, um das GWL \_ -WndProc-Flag zu unterteilen, und einen Zeiger auf die Unterklassen Prozedur. **SetWindowLong** gibt einen Zeiger auf die ursprüngliche Fenster Prozedur zurück. Verwenden Sie diesen Zeiger, um Meldungen an die ursprüngliche Prozedur zu übergeben. Die Unterklassen Fenster-Prozedur muss die [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion verwenden, um die ursprüngliche Fenster Prozedur aufzurufen.

> [!Note]  
> Verwenden Sie die [**setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) -Funktion, um Code zu schreiben, der sowohl mit der 32-Bit-als auch mit der 64-Bit-Version von Windows kompatibel ist.

 

Im folgenden Beispiel wird gezeigt, wie eine Instanz eines Bearbeitungs Steuer Elements in einem Dialogfeld unterteilt wird. Mithilfe der Prozedur des untergeordneten Klassen Fensters kann das Bearbeitungs Steuerelement alle Tastatureingaben einschließlich der Eingabe-und Tab-Taste empfangen, wenn das Steuerelement den Eingabefokus besitzt.


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



 

 
