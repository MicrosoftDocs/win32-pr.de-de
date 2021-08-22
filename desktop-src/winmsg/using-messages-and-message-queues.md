---
description: In den folgenden Codebeispielen wird veranschaulicht, wie sie die folgenden Aufgaben ausführen, die Windows Nachrichten und Nachrichtenwarteschlangen zugeordnet sind.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Verwenden von Nachrichten und Nachrichtenwarteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee617f2c48325eccf5a2fdb07741bb88b47738dea812d372acda1454c9dd3d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028338"
---
# <a name="using-messages-and-message-queues"></a>Verwenden von Nachrichten und Nachrichtenwarteschlangen

In den folgenden Codebeispielen wird veranschaulicht, wie sie die folgenden Aufgaben ausführen, die Windows Nachrichten und Nachrichtenwarteschlangen zugeordnet sind.

-   [Erstellen einer Nachrichtenschleife](#creating-a-message-loop)
-   [Untersuchen einer Nachrichtenwarteschlange](#examining-a-message-queue)
-   [Posten einer Nachricht](#posting-a-message)
-   [Senden einer Nachricht](#sending-a-message)

## <a name="creating-a-message-loop"></a>Erstellen einer Nachrichtenschleife

Das System erstellt nicht automatisch eine Nachrichtenwarteschlange für jeden Thread. Stattdessen erstellt das System eine Nachrichtenwarteschlange nur für Threads, die Vorgänge ausführen, die eine Nachrichtenwarteschlange erfordern. Wenn der Thread ein oder mehrere Fenster erstellt, muss eine Meldungsschleife bereitgestellt werden. Diese Nachrichtenschleife ruft Nachrichten aus der Nachrichtenwarteschlange des Threads ab und gibt sie an die entsprechenden Fensterverfahren weiter.

Da das System Nachrichten an einzelne Fenster in einer Anwendung weiter leitet, muss ein Thread mindestens ein Fenster erstellen, bevor die Nachrichtenschleife gestartet wird. Die meisten Anwendungen enthalten einen einzelnen Thread, der Fenster erstellt. Eine typische Anwendung registriert die Fensterklasse für ihr Hauptfenster, erstellt und zeigt das Hauptfenster an und startet dann die Meldungsschleife – alles in der [**WinMain-Funktion.**](/windows/win32/api/winbase/nf-winbase-winmain)

Sie erstellen eine Nachrichtenschleife mithilfe der [**Funktionen GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) Wenn Ihre Anwendung Zeicheneingaben vom Benutzer abrufen muss, schließen Sie die [**TranslateMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-translatemessage) in die Schleife ein. **TranslateMessage** übersetzt Nachrichten virtueller Schlüssel in Zeichennachrichten. Das folgende Beispiel zeigt die Meldungsschleife in der [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) einer einfachen Windows-basierten Anwendung.


```
HINSTANCE hinst; 
HWND hwndMain; 
 
int PASCAL WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, 
    LPSTR lpszCmdLine, int nCmdShow) 
{ 
    MSG msg;
    BOOL bRet; 
    WNDCLASS wc; 
    UNREFERENCED_PARAMETER(lpszCmdLine); 
 
    // Register the window class for the main window. 
 
    if (!hPrevInstance) 
    { 
        wc.style = 0; 
        wc.lpfnWndProc = (WNDPROC) WndProc; 
        wc.cbClsExtra = 0; 
        wc.cbWndExtra = 0; 
        wc.hInstance = hInstance; 
        wc.hIcon = LoadIcon((HINSTANCE) NULL, 
            IDI_APPLICATION); 
        wc.hCursor = LoadCursor((HINSTANCE) NULL, 
            IDC_ARROW); 
        wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
        wc.lpszMenuName =  "MainMenu"; 
        wc.lpszClassName = "MainWndClass"; 
 
        if (!RegisterClass(&wc)) 
            return FALSE; 
    } 
 
    hinst = hInstance;  // save instance handle 
 
    // Create the main window. 
 
    hwndMain = CreateWindow("MainWndClass", "Sample", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, (HWND) NULL, 
        (HMENU) NULL, hinst, (LPVOID) NULL); 
 
    // If the main window cannot be created, terminate 
    // the application. 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Show the window and paint its contents. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Start the message loop. 
 
    while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
    { 
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
 
    // Return the exit code to the system. 
 
    return msg.wParam; 
} 
```



Das folgende Beispiel zeigt eine Meldungsschleife für einen Thread, der Zugriffstasten verwendet und ein nicht modusloses Dialogfeld anzeigt. Wenn [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) oder [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) **TRUE** zurückgibt (was angibt, dass die Nachricht verarbeitet wurde), werden [**TranslateMessage**](/windows/win32/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nicht aufgerufen. Der Grund dafür ist, dass **TranslateAccelerator** und **IsDialogMessage** alle erforderlichen Übersetzungs- und Verteilerübersetzungen von Nachrichten durchführen.


```
HWND hwndMain; 
HWND hwndDlgModeless = NULL; 
MSG msg;
BOOL bRet; 
HACCEL haccel; 
// 
// Perform initialization and create a main window. 
// 
 
while( (bRet = GetMessage( &msg, NULL, 0, 0 )) != 0)
{ 
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else
    {
        if (hwndDlgModeless == (HWND) NULL || 
                !IsDialogMessage(hwndDlgModeless, &msg) && 
                !TranslateAccelerator(hwndMain, haccel, 
                    &msg)) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        }
    } 
} 
```



## <a name="examining-a-message-queue"></a>Untersuchen einer Nachrichtenwarteschlange

Gelegentlich muss eine Anwendung den Inhalt der Nachrichtenwarteschlange eines Threads außerhalb der Nachrichtenschleife des Threads untersuchen. Wenn beispielsweise die Fensterprozedur einer Anwendung einen längeren Zeichnungsvorgang ausführt, möchten Sie möglicherweise, dass der Benutzer den Vorgang unterbrechen kann. Sofern ihre Anwendung die Nachrichtenwarteschlange während des Vorgangs nicht regelmäßig auf Maus- und Tastaturmeldungen überprüft, reagiert sie erst nach Abschluss des Vorgangs auf Benutzereingaben. Der Grund dafür ist, dass die [**DispatchMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) in der Nachrichtenschleife des Threads erst dann zurückkehrt, wenn die Fensterprozedur die Verarbeitung einer Nachricht beendet hat.

Sie können die [**PeekMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-peekmessagea) verwenden, um eine Nachrichtenwarteschlange während eines längeren Vorgangs zu untersuchen. **PeekMessage** ähnelt der [**GetMessage-Funktion.**](/windows/win32/api/winuser/nf-winuser-getmessage) Überprüfen Sie eine Nachrichtenwarteschlange auf eine Nachricht, die den Filterkriterien entspricht, und kopieren Sie die Nachricht dann in eine [**MSG-Struktur.**](/windows/win32/api/winuser/ns-winuser-msg) Der Hauptunterschied zwischen den beiden Funktionen besteht in der Rückgabe von **GetMessage,** bis eine Nachricht, die den Filterkriterien entspricht, in der Warteschlange platziert wird, während **PeekMessage** unabhängig davon, ob sich eine Nachricht in der Warteschlange befindet, sofort zurückgibt.

Das folgende Beispiel zeigt, wie [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) verwendet wird, um eine Nachrichtenwarteschlange während eines längeren Vorgangs auf Mausklicks und Tastatureingaben zu untersuchen.


```
HWND hwnd; 
BOOL fDone; 
MSG msg; 
 
// Begin the operation and continue until it is complete 
// or until the user clicks the mouse or presses a key. 
 
fDone = FALSE; 
while (!fDone) 
{ 
    fDone = DoLengthyOperation(); // application-defined function 
 
    // Remove any messages that may be in the queue. If the 
    // queue contains any mouse or keyboard 
    // messages, end the operation. 
 
    while (PeekMessage(&msg, hwnd,  0, 0, PM_REMOVE)) 
    { 
        switch(msg.message) 
        { 
            case WM_LBUTTONDOWN: 
            case WM_RBUTTONDOWN: 
            case WM_KEYDOWN: 
                // 
                // Perform any required cleanup. 
                // 
                fDone = TRUE; 
        } 
    } 
} 
```



Mit anderen Funktionen, einschließlich [**GetQueueStatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) und [**GetInputState,**](/windows/win32/api/winuser/nf-winuser-getinputstate)können Sie auch den Inhalt der Nachrichtenwarteschlange eines Threads untersuchen. **GetQueueStatus gibt** ein Array von Flags zurück, das die Nachrichtentypen in der Warteschlange angibt. mithilfe dieser Methode können Sie am schnellsten feststellen, ob die Warteschlange Nachrichten enthält. **GetInputState gibt** **TRUE zurück,** wenn die Warteschlange Maus- oder Tastaturmeldungen enthält. Beide Funktionen können verwendet werden, um zu bestimmen, ob die Warteschlange Nachrichten enthält, die verarbeitet werden müssen.

## <a name="posting-a-message"></a>Posten einer Nachricht

Sie können eine Nachricht mithilfe der [**PostMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postmessagea) in einer Nachrichtenwarteschlange posten. **PostMessage** platziert eine Nachricht am Ende der Nachrichtenwarteschlange eines Threads und kehrt sofort zurück, ohne auf die Verarbeitung der Nachricht durch den Thread zu warten. Die Parameter der Funktion umfassen ein Fensterhand handle, einen Nachrichtenbezeichner und zwei Meldungsparameter. Das System kopiert diese Parameter in eine  [**MSG-Struktur,**](/windows/win32/api/winuser/ns-winuser-msg) füllt die Zeit- und **PT-Member** der Struktur aus und platziert die Struktur in der Nachrichtenwarteschlange.

Das System verwendet das mit der [**PostMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postmessagea) übergebene Fensterhand handle, um zu bestimmen, welche Threadnachrichtenwarteschlange die Nachricht empfangen soll. Wenn das Handle **HWND \_ TOPMOST** ist, übermittelt das System die Nachricht an die Threadnachrichtenwarteschlangen aller Fenster der obersten Ebene.

Sie können die [**PostThreadMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) verwenden, um eine Nachricht an eine bestimmte Threadnachrichtenwarteschlange zu senden. **PostThreadMessage** ähnelt [**PostMessage,**](/windows/win32/api/winuser/nf-winuser-postmessagea)mit der Ausnahme, dass der erste Parameter ein Threadbezeichner und kein Fensterhandles ist. Sie können den Threadbezeichner abrufen, indem Sie die [**GetCurrentThreadId-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) aufrufen.

Verwenden Sie die [**PostQuitMessage-Funktion,**](/windows/win32/api/winuser/nf-winuser-postquitmessage) um eine Nachrichtenschleife zu beenden. **PostQuitMessage überträgt** die [**WM \_ QUIT-Nachricht**](wm-quit.md) an den aktuell ausgeführten Thread. Die Meldungsschleife des Threads wird beendet und gibt die Steuerung an das System zurück, wenn die **WM \_ QUIT-Nachricht angezeigt** wird. Eine Anwendung ruft **postQuitMessage** in der Regel als Antwort auf die [**WM \_ DESTROY-Nachricht**](wm-destroy.md) auf, wie im folgenden Beispiel gezeigt.


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Senden einer Nachricht

Die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) wird verwendet, um eine Nachricht direkt an eine Fensterprozedur zu senden. **SendMessage** ruft eine Fensterprozedur auf und wartet, bis diese Prozedur die Nachricht verarbeiten und ein Ergebnis zurückgeben kann.

Eine Nachricht kann an ein beliebiges Fenster im System gesendet werden. Alles, was erforderlich ist, ist ein Fensterhand handle. Das System verwendet das Handle, um zu bestimmen, welche Fensterprozedur die Nachricht empfangen soll.

Vor der Verarbeitung einer Nachricht, die möglicherweise von einem anderen Thread gesendet wurde, sollte eine Fensterprozedur zuerst die [**InSendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-insendmessage) aufrufen. Wenn diese Funktion **TRUE zurückgibt,** sollte die Fensterprozedur [**ReplyMessage**](/windows/win32/api/winuser/nf-winuser-replymessage) vor jeder Funktion aufrufen, die bewirkt, dass der Thread die Steuerung ergibt, wie im folgenden Beispiel gezeigt.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



Eine Reihe von Nachrichten kann an Steuerelemente in einem Dialogfeld gesendet werden. Diese Steuerungsmeldungen legen die Darstellung, das Verhalten und den Inhalt von Steuerelementen fest oder rufen Informationen zu Steuerelementen ab. Beispielsweise kann die [**CB \_ ADDSTRING-Nachricht**](../controls/cb-addstring.md) einem Kombinationsfeld eine Zeichenfolge hinzufügen, und die [**BM \_ SETCHECK-Meldung**](../controls/bm-setcheck.md) kann den Überprüfungszustand eines Kontrollkästchens oder Optionsfelds festlegen.

Verwenden Sie [**die SendDlgItemMessage-Funktion,**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) um eine Nachricht an ein Steuerelement zu senden, und geben Sie dabei den Bezeichner des Steuerelements und das Handle des Dialogfeldfensters an, das das Steuerelement enthält. Im folgenden Beispiel aus einer Dialogfeldprozedur wird eine Zeichenfolge aus dem Bearbeitungssteuerfeld eines Kombinationsfelds in das Listenfeld kopiert. Im Beispiel wird **SendDlgItemMessage** verwendet, um eine [**CB \_ ADDSTRING-Nachricht**](../controls/cb-addstring.md) an das Kombinationsfeld zu senden.


```
HWND hwndCombo; 
int cTxtLen; 
PSTR pszMem; 
 
switch (uMsg) 
{ 
    case WM_COMMAND: 
        switch (LOWORD(wParam)) 
        { 
            case IDD_ADDCBITEM: 
                // Get the handle of the combo box and the 
                // length of the string in the edit control 
                // of the combo box. 
 
                hwndCombo = GetDlgItem(hwndDlg, IDD_COMBO); 
                cTxtLen = GetWindowTextLength(hwndCombo); 
 
                // Allocate memory for the string and copy 
                // the string into the memory. 
 
                pszMem = (PSTR) VirtualAlloc((LPVOID) NULL, 
                    (DWORD) (cTxtLen + 1), MEM_COMMIT, 
                    PAGE_READWRITE); 
                GetWindowText(hwndCombo, pszMem, 
                    cTxtLen + 1); 
 
                // Add the string to the list box of the 
                // combo box and remove the string from the 
                // edit control of the combo box. 
 
                if (pszMem != NULL) 
                { 
                    SendDlgItemMessage(hwndDlg, IDD_COMBO, 
                        CB_ADDSTRING, 0, 
                        (DWORD) ((LPSTR) pszMem)); 
                    SetWindowText(hwndCombo, (LPSTR) NULL); 
                } 
 
                // Free the memory and return. 
 
                VirtualFree(pszMem, 0, MEM_RELEASE); 
                return TRUE; 
            // 
            // Process other dialog box commands. 
            // 
 
        } 
    // 
    // Process other dialog box messages. 
    // 
 
}
```



 

 
