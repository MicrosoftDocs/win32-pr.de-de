---
description: Die folgenden Codebeispiele veranschaulichen, wie die folgenden Aufgaben ausgeführt werden, die Windows-Meldungen und Nachrichten Warteschlangen zugeordnet sind.
ms.assetid: 62b4616c-37bf-4d9f-8891-7010c7035d18
title: Verwenden von Meldungen und Nachrichten Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a33f422a1a7c77f2c2fcd5913f931168a350a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373057"
---
# <a name="using-messages-and-message-queues"></a>Verwenden von Meldungen und Nachrichten Warteschlangen

Die folgenden Codebeispiele veranschaulichen, wie die folgenden Aufgaben ausgeführt werden, die Windows-Meldungen und Nachrichten Warteschlangen zugeordnet sind.

-   [Erstellen einer Nachrichten Schleife](#creating-a-message-loop)
-   [Überprüfen einer Nachrichten Warteschlange](#examining-a-message-queue)
-   [Veröffentlichen einer Nachricht](#posting-a-message)
-   [Senden einer Nachricht](#sending-a-message)

## <a name="creating-a-message-loop"></a>Erstellen einer Nachrichten Schleife

Das System erstellt nicht automatisch eine Nachrichten Warteschlange für jeden Thread. Stattdessen erstellt das System eine Nachrichten Warteschlange nur für Threads, die Vorgänge ausführen, für die eine Nachrichten Warteschlange erforderlich ist. Wenn der Thread ein oder mehrere Fenster erstellt, muss eine Nachrichten Schleife bereitgestellt werden. Diese Nachrichten Schleife ruft Nachrichten aus der Nachrichten Warteschlange des Threads ab und sendet Sie an die entsprechenden Fenster Prozeduren.

Da das System Nachrichten an einzelne Fenster in einer Anwendung weiterleitet, muss ein Thread vor dem Starten der Nachrichten Schleife mindestens ein Fenster erstellen. Die meisten Anwendungen enthalten einen einzelnen Thread, der Windows erstellt. Eine typische Anwendung registriert die Fenster Klasse für das Hauptfenster, erstellt und zeigt das Hauptfenster an und startet dann die Nachrichten Schleife – alles in der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion.

Sie erstellen eine Nachrichten Schleife mithilfe der Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) . Wenn die Anwendung Zeichen Eingaben vom Benutzer abrufen muss, schließen Sie die [**translatemess**](/windows/win32/api/winuser/nf-winuser-translatemessage) -Funktion in die-Schleife ein. **Translatemess** übersetzt die Nachrichten von virtuellen Schlüsseln in Zeichen Nachrichten. Das folgende Beispiel zeigt die Nachrichten Schleife in der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion einer einfachen Windows-basierten Anwendung.


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



Das folgende Beispiel zeigt eine Meldungs Schleife für einen Thread, der Accelerators verwendet und ein nicht modalem Dialogfeld anzeigt. Wenn [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) oder [**IsDialogMessage**](/windows/win32/api/winuser/nf-winuser-isdialogmessagea) **true** zurückgibt (gibt an, dass die Nachricht verarbeitet wurde), werden [**translatemmeage**](/windows/win32/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) nicht aufgerufen. Der Grund hierfür ist, dass **TranslateAccelerator** und **IsDialogMessage** alle notwendigen Übersetzungen und die Weiterleitung von Nachrichten durchführen.


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



## <a name="examining-a-message-queue"></a>Überprüfen einer Nachrichten Warteschlange

Gelegentlich muss eine Anwendung den Inhalt der Nachrichten Warteschlange eines Threads von außerhalb der Nachrichten Schleife des Threads untersuchen. Wenn z. b. die Fenster Prozedur einer Anwendung einen langwierigen Zeichnungs Vorgang ausführt, kann es sein, dass der Benutzer in der Lage sein soll, den Vorgang zu unterbrechen. Wenn die Anwendung die Nachrichten Warteschlange während des Vorgangs für Maus-und Tastatur Meldungen nicht regelmäßig überprüft, antwortet sie erst nach Abschluss des Vorgangs auf Benutzereingaben. Der Grund hierfür ist, dass die [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) -Funktion in der Nachrichten Schleife des Threads erst dann zurückgegeben wird, wenn die Verarbeitung einer Nachricht durch die Fenster Prozedur abgeschlossen ist.

Sie können die Funktion " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) " verwenden, um eine Nachrichten Warteschlange während eines langen Vorgangs zu untersuchen. " **Peer Message** " ähnelt der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion. Beide überprüfen eine Meldungs Warteschlange auf eine Nachricht, die den Filterkriterien entspricht, und kopieren dann die Nachricht in eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur. Der Hauptunterschied zwischen den beiden Funktionen besteht darin, dass **GetMessage** nicht **zurückgibt,** bis eine Nachricht, die mit den Filterkriterien übereinstimmt, in der Warteschlange platziert wird.

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) " eine Meldungs Warteschlange für Mausklicks und Tastatureingaben während eines langen Vorgangs untersuchen können.


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



Andere Funktionen, einschließlich [**getqueuestatus**](/windows/win32/api/winuser/nf-winuser-getqueuestatus) und [**getinputstate**](/windows/win32/api/winuser/nf-winuser-getinputstate), ermöglichen es Ihnen außerdem, den Inhalt der Nachrichten Warteschlange eines Threads zu untersuchen. **Getqueuestatus** gibt ein Array von Flags zurück, das die Nachrichten Typen in der Warteschlange angibt. die Verwendung ist die schnellste Möglichkeit, um zu ermitteln, ob die Warteschlange Nachrichten enthält. **Getinputstate** gibt **true** zurück, wenn die Warteschlange Maus-oder Tastatur Meldungen enthält. Beide Funktionen können verwendet werden, um zu bestimmen, ob die Warteschlange Nachrichten enthält, die verarbeitet werden müssen.

## <a name="posting-a-message"></a>Veröffentlichen einer Nachricht

Mithilfe der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion können Sie eine Nachricht in einer Nachrichten Warteschlange veröffentlichen. Nach **richten** platziert eine Nachricht am Ende der Nachrichten Warteschlange eines Threads und gibt sofort zurück, ohne darauf zu warten, dass der Thread die Nachricht verarbeitet. Die Parameter der Funktion enthalten ein Fenster Handle, eine Nachrichten-ID und zwei Nachrichten Parameter. Das System kopiert diese Parameter in eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, füllt die **Zeit** -und **PT** -Member der Struktur aus und platziert die Struktur in der Nachrichten Warteschlange.

Das System verwendet das mit der [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) -Funktion über gegebene Fenster Handle, um zu bestimmen, welche Thread Nachrichten Warteschlange die Nachricht empfangen soll. Wenn das Handle das **\_ oberste HWND** ist, stellt das System die Nachricht an die Thread Nachrichten Warteschlangen aller Fenster der obersten Ebene.

Sie können die [**PostThreadMessage**](/windows/win32/api/winuser/nf-winuser-postthreadmessagea) -Funktion verwenden, um eine Nachricht an eine bestimmte Thread Nachrichten Warteschlange zu senden. **PostThreadMessage** ist " [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)" ähnlich, außer der erste Parameter ist ein Thread Bezeichner und kein Fenster handle. Sie können den Thread Bezeichner abrufen, indem Sie die [**GetCurrentThreadID**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid) -Funktion aufrufen.

Verwenden Sie die [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion, um eine Nachrichten Schleife zu beenden. **PostQuitMessage sendet** die [**WM \_**](wm-quit.md) -beendenden Nachricht an den derzeit ausgeführten Thread. Die Nachrichten Schleife des Threads wird beendet, und die Steuerung wird an das System zurückgegeben, wenn die **WM- \_** Beendungs Meldung erkannt wird. Eine Anwendung ruft in der Regel **PostQuitMessage** als Antwort auf die WM-Lösch Meldung auf, wie im folgenden Beispiel gezeigt. [**\_**](wm-destroy.md)


```
case WM_DESTROY: 
 
    // Perform cleanup tasks. 
 
    PostQuitMessage(0); 
    break; 
```



## <a name="sending-a-message"></a>Senden einer Nachricht

Die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion wird verwendet, um eine Nachricht direkt an eine Fenster Prozedur zu senden. **SendMessage** Ruft eine Fenster Prozedur auf und wartet darauf, dass diese Prozedur die Nachricht verarbeitet und ein Ergebnis zurückgibt.

Eine Nachricht kann an jedes Fenster im System gesendet werden. alles, was erforderlich ist, ist ein Fenster handle. Das System verwendet das Handle, um zu bestimmen, welche Fenster Prozedur die Nachricht empfangen soll.

Vor dem Verarbeiten einer Nachricht, die möglicherweise von einem anderen Thread gesendet wurde, sollte eine Fenster Prozedur zuerst die [**insendmessage**](/windows/win32/api/winuser/nf-winuser-insendmessage) -Funktion aufzurufen. Wenn diese Funktion " **true**" zurückgibt, sollte die Fenster Prozedur " [**replymess Age**](/windows/win32/api/winuser/nf-winuser-replymessage) " vor jeder Funktion aufgerufen werden, die bewirkt, dass der Thread die Steuerung übernimmt, wie im folgenden Beispiel gezeigt.


```
case WM_USER + 5: 
    if (InSendMessage()) 
        ReplyMessage(TRUE); 
 
    DialogBox(hInst, "MyDialogBox", hwndMain, (DLGPROC) MyDlgProc); 
    break; 
```



An Steuerelemente in einem Dialogfeld können eine Reihe von Nachrichten gesendet werden. Diese Steuerungs Meldungen legen die Darstellung, das Verhalten und den Inhalt von Steuerelementen fest oder rufen Informationen zu Steuerelementen ab. Beispielsweise kann die [**CB \_ AddString**](../controls/cb-addstring.md) -Nachricht eine Zeichenfolge zu einem Kombinations Feld hinzufügen, und die [**BM- \_ setcheck**](../controls/bm-setcheck.md) -Nachricht kann den Prüf Zustand eines Kontrollkästchens oder Options Felds festlegen.

Verwenden Sie die [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea) -Funktion, um eine Nachricht an ein Steuerelement zu senden, und geben Sie dabei den Bezeichner des Steuer Elements und das Handle des Dialogfeld Fensters an, das das Steuerelement enthält. Im folgenden Beispiel, das aus einer Dialogfeld Prozedur stammt, wird eine Zeichenfolge aus dem Bearbeitungs Steuerelement eines Kombinations Felds in das Listenfeld kopiert. Das Beispiel verwendet **SendDlgItemMess** , um eine [**CB \_ AddString**](../controls/cb-addstring.md) -Nachricht an das Kombinations Feld zu senden.


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



 

 
