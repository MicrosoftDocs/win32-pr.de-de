---
title: Verwenden von Tastatur Accelerators
description: In diesem Abschnitt werden Aufgaben beschrieben, die mit Tastatur Accelerators verknüpft sind.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- Benutzereingabe, Tastaturbeschleuniger
- Erfassen von Benutzereingaben, Tastatur Accelerators
- Tastaturbeschleuniger
- Accelerators
- Zugriffstasten Tabellen
- Zugriffstasten-Tabellen Ressourcen
- Übersetzen der Beschleunigungs Funktion
- WM_COMMAND Meldung
- WM_SYS Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038977"
---
# <a name="using-keyboard-accelerators"></a>Verwenden von Tastatur Accelerators

In diesem Abschnitt werden Aufgaben beschrieben, die mit Tastatur Accelerators verknüpft sind.

-   [Verwenden einer Zugriffstasten-Tabellen Ressource](#using-an-accelerator-table-resource)
    -   [Erstellen der Zugriffstasten-Tabellen Ressource](#creating-the-accelerator-table-resource)
    -   [Laden der Zugriffstasten-Tabellen Ressource](#loading-the-accelerator-table-resource)
    -   [Aufrufen der Translation Accelerator-Funktion](#calling-the-translate-accelerator-function)
    -   [Verarbeiten von WM- \_ Befehls Meldungen](/windows)
    -   [Zerstören der Zugriffstasten-Tabellen Ressource](#destroying-the-accelerator-table-resource)
    -   [Erstellen von Accelerators für Schriftart Attribute](#creating-accelerators-for-font-attributes)
-   [Verwenden einer Zugriffstasten Tabelle, die zur Laufzeit erstellt wird](#using-an-accelerator-table-created-at-run-time)
    -   [Erstellen einer Run-Time Accelerator-Tabelle](#creating-a-run-time-accelerator-table)
    -   [Verarbeiten von Accelerators](#processing-accelerators)
    -   [Zerstören einer Run-Time Accelerator-Tabelle](#destroying-a-run-time-accelerator-table)
    -   [Erstellen von Benutzer bearbeitbaren Acceleratoren](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Verwenden einer Zugriffstasten-Tabellen Ressource

Die gängigste Methode zum Hinzufügen von Zugriffstasten für eine Anwendung ist das Einschließen einer Zugriffstasten-Tabellen Ressource mit der ausführbaren Datei der Anwendung und das anschließende Laden der Ressource zur Laufzeit.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Erstellen der Zugriffstasten-Tabellen Ressource](#creating-the-accelerator-table-resource)
-   [Laden der Zugriffstasten-Tabellen Ressource](#loading-the-accelerator-table-resource)
-   [Aufrufen der Translation Accelerator-Funktion](#calling-the-translate-accelerator-function)
-   [Verarbeiten von WM- \_ Befehls Meldungen](/windows)
-   [Zerstören der Zugriffstasten-Tabellen Ressource](#destroying-the-accelerator-table-resource)
-   [Erstellen von Accelerators für Schriftart Attribute](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Erstellen der Zugriffstasten-Tabellen Ressource

Sie erstellen eine Accelerator-Table-Ressource, indem Sie die [Accelerators](./accelerators-resource.md) -Anweisung in der Ressourcen Definitionsdatei Ihrer Anwendung verwenden. Sie müssen der Zugriffstasten Tabelle einen Namen oder Ressourcen Bezeichner zuweisen, vorzugsweise im Gegensatz zu allen anderen Ressourcen. Das System verwendet diesen Bezeichner, um die Ressource zur Laufzeit zu laden.

Jede Zugriffstaste, die Sie definieren, erfordert einen separaten Eintrag in der Zugriffstasten Tabelle. In jedem Eintrag definieren Sie den Tastatur Schlag (entweder einen ASCII-Zeichencode oder einen Code für den virtuellen Schlüssel), der die Zugriffstaste und den Bezeichner der Zugriffstaste generiert. Außerdem müssen Sie angeben, ob der Tastatur Strich in einer Kombination mit der alt-, UMSCHALT-oder STRG-Taste verwendet werden muss. Weitere Informationen zu virtuellen Schlüsseln finden Sie unter [Tastatureingabe](/windows/desktop/inputdev/keyboard-input).

Ein ASCII-Tastatur Strich wird entweder durch Einschließen des ASCII-Zeichens in doppelte Anführungszeichen oder durch Verwendung des ganzzahligen Werts des Zeichens in Kombination mit dem ASCII-Flag angegeben. In den folgenden Beispielen wird gezeigt, wie Sie ASCII-Beschleuniger definieren.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Eine Tastenkombination für den Code eines virtuellen Schlüssels wird unterschiedlich angegeben, je nachdem, ob es sich bei der Tastatureingabe um einen alphanumerischen Schlüssel oder um einen nicht alphanumerischen Schlüssel handelt. Bei einem alphanumerischen Schlüssel wird der Buchstabe oder die Zahl des Schlüssels, der in doppelte Anführungszeichen eingeschlossen ist, mit dem **VIRTKEY** -Flag kombiniert. Bei einem nicht alphanumerischen Schlüssel wird der Code für den virtuellen Schlüssel für den jeweiligen Schlüssel mit dem **VIRTKEY** -Flag kombiniert. In den folgenden Beispielen wird veranschaulicht, wie Sie Code Accelerators für virtuelle Schlüssel definieren.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

Das folgende Beispiel zeigt eine Zugriffstaste für eine Ressource, die Accelerators für Datei Vorgänge definiert. Der Name der Ressource ist " *fileaccel*".

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Wenn Sie möchten, dass der Benutzer die Alt-Taste, die UMSCHALTTASTE oder die STRG-Taste in einer Kombination mit der Zugriffstaste drücken, geben Sie die alt-, UMSCHALT-und steuerungflags in der Zugriffstasten Definition an. Hier einige Beispiele.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Wenn eine Zugriffstaste einem Menü Element entspricht, hebt das System standardmäßig das Menü Element hervor. Sie können das **noinvert** -Flag verwenden, um die Hervorhebung für eine einzelne Zugriffstaste zu verhindern. Im folgenden Beispiel wird gezeigt, wie das **noinvert** -Flag verwendet wird:

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Zum Definieren von Accelerators, die Menü Elementen in der Anwendung entsprechen, fügen Sie die Zugriffstasten in den Text der Menü Elemente ein. Im folgenden Beispiel wird gezeigt, wie Acceleratoren in Menü Element Text in eine Ressourcen Definitionsdatei eingeschlossen werden.

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a>Laden der Zugriffstasten-Tabellen Ressource

Eine Anwendung lädt eine Accelerator-Table-Ressource, indem Sie die [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion aufruft und den Instanzhandle für die Anwendung angibt, deren ausführbare Datei die Ressource und den Namen oder Bezeichner der Ressource enthält. **Loadaccelerators** lädt die angegebene Zugriffstasten Tabelle in den Arbeitsspeicher und gibt das Handle an die Zugriffstasten Tabelle zurück.

Eine Anwendung kann jederzeit eine Accelerator-Table-Ressource laden. Normalerweise lädt eine Single Thread-Anwendung die Zugriffstasten Tabelle, bevor Sie die Hauptnachrichten Schleife eingibt. Eine Anwendung, die mehrere Threads verwendet, lädt in der Regel die Zugriffstasten-Tabellen Ressource für einen Thread, bevor die Nachrichten Schleife für den Thread eingegeben wird. Eine Anwendung oder ein Thread kann auch mehrere Zugriffstasten Tabellen verwenden, die jeweils einem bestimmten Fenster in der Anwendung zugeordnet sind. Eine solche Anwendung lädt die Zugriffstasten Tabelle für das Fenster jedes Mal, wenn der Benutzer das Fenster aktiviert hat. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Aufrufen der Translation Accelerator-Funktion

Zum Verarbeiten von Accelerators muss die Nachrichten Schleife einer Anwendung (oder des Threads) einen aufrufsvorgang der [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion enthalten. **TranslateAccelerator** vergleicht Tastatureingaben mit einer Zugriffstasten Tabelle und übersetzt die Tastatureingaben in eine [**WM- \_ Befehls**](wm-command.md) Meldung (oder eine [**WM- \_ syscommand**](wm-syscommand.md)-Meldung), wenn eine Entsprechung gefunden wird. Die-Funktion sendet die Nachricht dann an eine Fenster Prozedur. Die Parameter der **TranslateAccelerator** -Funktion enthalten das Handle für das Fenster, das die WM- **\_ Befehls** Meldungen empfängt, das Handle für die Zugriffstasten Tabelle, die zum Übersetzen von Acceleratoren verwendet wird, und einen Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die eine Nachricht aus der Warteschlange enthält. Im folgenden Beispiel wird gezeigt, wie Sie **TranslateAccelerator** aus einer Nachrichten Schleife heraus abrufen können.


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a>Verarbeiten von WM- \_ Befehls Meldungen

Wenn eine Zugriffstaste verwendet wird, empfängt das in der [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion angegebene Fenster einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht. Das nieder wertige Wort des *wParam* -Parameters enthält den Bezeichner der Zugriffstaste. Die Fenster Prozedur überprüft den Bezeichner, um die Quelle der **WM- \_ Befehls** Nachricht zu bestimmen und die Nachricht entsprechend zu verarbeiten.

Wenn eine Zugriffstaste einem Menü Element in der Anwendung entspricht, wird in der Regel die Zugriffstaste und das Menü Element dem gleichen Bezeichner zugewiesen. Wenn Sie wissen möchten, ob eine [**WM- \_ Befehls**](wm-command.md) Nachricht von einer Zugriffstaste oder einem Menü Element generiert wurde, können Sie das höchst wertige Wort des *wParam* -Parameters überprüfen. Wenn eine Zugriffstaste die Meldung generiert hat, ist das höchst wertige Wort 1. Wenn ein Menü Element die Meldung generiert hat, ist das höchst wertige Wort 0.

### <a name="destroying-the-accelerator-table-resource"></a>Zerstören der Zugriffstasten-Tabellen Ressource

Das System zerstört die von der [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion geladenen acceleratortabellenressourcen automatisch und entfernt die Ressource nach dem Schließen der Anwendung aus dem Arbeitsspeicher.

### <a name="creating-accelerators-for-font-attributes"></a>Erstellen von Accelerators für Schriftart Attribute

Das Beispiel in diesem Abschnitt zeigt, wie die folgenden Aufgaben ausgeführt werden:

-   Erstellen Sie eine Zugriffstaste für eine Ressource.
-   Lädt die Zugriffstasten Tabelle zur Laufzeit.
-   Übersetzen Sie Accelerators in einer Nachrichten Schleife.
-   Prozess [**WM- \_ Befehls**](wm-command.md) Meldungen, die von den Accelerators generiert werden.

Diese Aufgaben werden im Kontext einer Anwendung veranschaulicht, die ein **Zeichen** Menü und entsprechende Acceleratoren enthält, mit denen der Benutzerattribute der aktuellen Schriftart auswählen kann.

Der folgende Teil einer Ressourcen Definitionsdatei definiert das **Zeichen** Menü und die zugehörige Zugriffstasten Tabelle. Beachten Sie, dass die Menü Elemente die Tastenkombinationen anzeigen und dass jede Zugriffstaste denselben Bezeichner wie das zugehörige Menü Element aufweist.


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



Die folgenden Abschnitte aus der Quelldatei der Anwendung veranschaulichen, wie die Accelerators implementiert werden.


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a>Verwenden einer Zugriffstasten Tabelle, die zur Laufzeit erstellt wird

In diesem Thema wird die Verwendung von Zugriffstasten Tabellen erläutert, die zur Laufzeit erstellt werden.

-   [Erstellen einer Run-Time Accelerator-Tabelle](#creating-a-run-time-accelerator-table)
-   [Verarbeiten von Accelerators](#processing-accelerators)
-   [Zerstören einer Run-Time Accelerator-Tabelle](#destroying-a-run-time-accelerator-table)
-   [Erstellen von Benutzer bearbeitbaren Acceleratoren](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Erstellen einer Run-Time Accelerator-Tabelle

Der erste Schritt beim Erstellen einer Zugriffstasten Tabelle zur Laufzeit ist das Auffüllen eines Arrays von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen. Jede Struktur im Array definiert eine Zugriffstaste in der Tabelle. Die Definition eines Zugriffstasten enthält die Flags, den Schlüssel und den Bezeichner. Die **Accel** -Struktur hat die folgende Form.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Sie definieren eine Tastenkombination einer Zugriffstaste, indem Sie einen ASCII-Zeichencode oder einen Code für den virtuellen Schlüssel im **Schlüssel** Element der [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Struktur angeben. Wenn Sie einen Code für den virtuellen Schlüssel angeben, müssen Sie zunächst das **fvirtkey** -Flag in das **fvirt** -Member einschließen. Andernfalls interpretiert das System den Code als ASCII-Zeichencode. Sie können das **Fcontrol** **-, das**-oder das **fshift** -Flag oder alle drei einschließen, um die STRG-Taste, die Alt-Taste oder die UMSCHALTTASTE mit dem Tastatur Strich zu kombinieren.

Um die Zugriffstasten Tabelle zu erstellen, übergeben Sie einen Zeiger auf das Array von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen an [**die Funktion "**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) -Funktion". " **Kreateacceleratortable** " erstellt die Zugriffstasten Tabelle und gibt das Handle für die Tabelle zurück.

### <a name="processing-accelerators"></a>Verarbeiten von Accelerators

Das Laden und Aufrufen von Acceleratoren, die von einer zur Laufzeit erstellten Zugriffstasten-Tabelle bereitgestellt werden, ist identisch mit der Verarbeitung von Zugriffstasten, die von einer Zugriffstasten-Tabelle bereitgestellt werden Weitere Informationen finden Sie unter [Laden der](#loading-the-accelerator-table-resource) Zugriffstasten-Tabellen Ressource durch [Verarbeitung von WM- \_ befehlsnachrichten](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Zerstören einer Run-Time Accelerator-Tabelle

Das System zerstört schnell Zugriffs Tabellen, die zur Laufzeit erstellt werden, und entfernt die Ressourcen nach dem Schließen der Anwendung aus dem Arbeitsspeicher. Sie können eine Zugriffstasten Tabelle zerstören und Sie zuvor aus dem Arbeitsspeicher entfernen, indem Sie das Handle der Tabelle an die [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) -Funktion übergeben.

### <a name="creating-user-editable-accelerators"></a>Erstellen von Benutzer bearbeitbaren Acceleratoren

In diesem Beispiel wird gezeigt, wie ein Dialogfeld erstellt wird, das es dem Benutzer ermöglicht, die einem Menü Element zugeordnete Zugriffstaste zu ändern. Das Dialogfeld besteht aus einem Kombinations Feld mit Menü Elementen, einem Kombinations Feld mit den Namen der Schlüssel und Kontrollkästchen zum Auswählen der Tasten STRG, alt und UMSCHALT. Die folgende Abbildung zeigt das Dialogfeld.

![Dialogfeld mit Kombinations Feldern und Kontrollkästchen](images/useredit.gif)

Im folgenden Beispiel wird gezeigt, wie das Dialogfeld in der Ressourcen Definitionsdatei definiert ist.

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

Die Menüleiste der Anwendung enthält ein Untermenü des **Zeichens** , dessen Elemente mit Zugriffstasten verknüpft sind.

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

Die Menü Element Werte für die Menüvorlage sind Konstanten, die wie folgt in der Header Datei der Anwendung definiert sind.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

Im Dialogfeld wird ein Array von Anwendungs definierten VKey-Strukturen verwendet, von denen jedes eine Keystroke-Text Zeichenfolge und eine Zugriffs Text Zeichenfolge enthält. Wenn das Dialogfeld erstellt wird, wird das Array analysiert, und jede Keystroke-Text Zeichenfolge wird dem Kombinations Feld **KeyStroke auswählen** hinzugefügt. Wenn der Benutzer auf die Schaltfläche **OK** klickt, wird das Dialogfeld die ausgewählte Keystroke-Text Zeichenfolge nachschlagen und die entsprechende Zugriffstasten-Text Zeichenfolge abrufen. Das Dialogfeld fügt die Zugriffstasten-Text Zeichenfolge an den Text des Menü Elements an, das der Benutzer ausgewählt hat. Das folgende Beispiel zeigt das Array von VKey-Strukturen:


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



Die Initialisierungs Prozedur des Dialog Felds füllt die Kombinations Felder **Select Item** und **KeyStroke** aus. Nachdem der Benutzer ein Menü Element und eine zugeordnete Zugriffstaste ausgewählt hat, überprüft das Dialogfeld die Steuerelemente im Dialogfeld, um die Benutzer Auswahl zu erhalten, aktualisiert den Text des Menü Elements und erstellt dann eine neue Zugriffstasten Tabelle, die die benutzerdefinierte neue Zugriffstaste enthält. Das folgende Beispiel zeigt die-Dialogfeld Prozedur. Beachten Sie, dass Sie in der Fenster Prozedur initialisieren müssen.


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 