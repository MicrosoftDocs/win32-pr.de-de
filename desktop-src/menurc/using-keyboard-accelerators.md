---
title: Verwenden von Tastenkombinationen
description: In diesem Abschnitt werden Aufgaben behandelt, die Tastenkombinationen zugeordnet sind.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- Benutzereingabe,Tastenkombinationen
- Erfassen von Benutzereingaben, Tastenkombinationen
- Tastenkombinationen
- Beschleuniger
- Zugriffstastentabellen
- Accelerator-Table-Ressourcen
- Translate Accelerator-Funktion
- WM_COMMAND-Nachricht
- WM_SYS COMMAND-Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecbb16c92b986cbe73aababc7edc24518cf59ce5009322e3a006bac827427c45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886564"
---
# <a name="using-keyboard-accelerators"></a>Verwenden von Tastenkombinationen

In diesem Abschnitt werden Aufgaben behandelt, die Tastenkombinationen zugeordnet sind.

-   [Verwenden einer Accelerator-Tabellenressource](#using-an-accelerator-table-resource)
    -   [Erstellen der Accelerator-Tabellenressource](#creating-the-accelerator-table-resource)
    -   [Laden der Accelerator-Tabellenressource](#loading-the-accelerator-table-resource)
    -   [Aufrufen der Translate Accelerator-Funktion](#calling-the-translate-accelerator-function)
    -   [Verarbeiten von WM \_ COMMAND-Nachrichten](/windows)
    -   [Zerstören der Accelerator-Tabellenressource](#destroying-the-accelerator-table-resource)
    -   [Erstellen von Zugriffstasten für Schriftartattribute](#creating-accelerators-for-font-attributes)
-   [Verwenden einer zur Laufzeit erstellten Zugriffstastentabelle](#using-an-accelerator-table-created-at-run-time)
    -   [Erstellen einer Run-Time Accelerator-Tabelle](#creating-a-run-time-accelerator-table)
    -   [Processing Accelerators](#processing-accelerators)
    -   [Zerstören einer Run-Time Accelerator-Tabelle](#destroying-a-run-time-accelerator-table)
    -   [Erstellen bearbeitbarer Accelerators für Benutzer](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a>Verwenden einer Accelerator-Tabellenressource

Die häufigste Methode zum Hinzufügen von Zugriffstastenunterstützung zu einer Anwendung ist das Hinzufügen einer Accelerator-Table-Ressource in die ausführbare Datei der Anwendung und das anschließende Laden der Ressource zur Laufzeit.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Erstellen der Accelerator-Tabellenressource](#creating-the-accelerator-table-resource)
-   [Laden der Accelerator-Tabellenressource](#loading-the-accelerator-table-resource)
-   [Aufrufen der Translate Accelerator-Funktion](#calling-the-translate-accelerator-function)
-   [Verarbeiten von WM \_ COMMAND-Nachrichten](/windows)
-   [Zerstören der Accelerator-Tabellenressource](#destroying-the-accelerator-table-resource)
-   [Erstellen von Zugriffstasten für Schriftartattribute](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a>Erstellen der Accelerator-Tabellenressource

Sie erstellen eine Accelerator-Table-Ressource mithilfe der [ACCELERATORS-Anweisung](./accelerators-resource.md) in der Ressourcendefinitionsdatei Ihrer Anwendung. Sie müssen der Zugriffstastentabelle einen Namen oder Ressourcenbezeichner zuweisen, vorzugsweise im Gegensatz zu anderen Ressourcen. Das System verwendet diesen Bezeichner, um die Ressource zur Laufzeit zu laden.

Jede von Ihnen definierte Zugriffstaste erfordert einen separaten Eintrag in der Zugriffstastentabelle. In jedem Eintrag definieren Sie die Tastatureingabe (entweder ein ASCII-Zeichencode oder virtueller Schlüsselcode), der die Zugriffstaste und den Bezeichner des Zugriffstasten generiert. Sie müssen auch angeben, ob die Tastatureingabe in einer Kombination mit den TASTEN ALT, UMSCHALT ODER STRG verwendet werden muss. Weitere Informationen zu virtuellen Tasten finden Sie unter [Tastatureingabe.](/windows/desktop/inputdev/keyboard-input)

Eine ASCII-Tastatureingabe wird entweder angegeben, indem das ASCII-Zeichen in doppelte Anführungszeichen eingeschlossen wird oder indem der ganzzahlige Wert des Zeichens in Kombination mit dem ASCII-Flag verwendet wird. In den folgenden Beispielen wird gezeigt, wie ASCII-Zugriffstasten definiert werden.

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

Eine Tastatureingabe mit virtuellem Schlüsselcode wird unterschiedlich angegeben, je nachdem, ob es sich bei der Tastatureingabe um einen alphanumerischen Schlüssel oder um einen nicht alphanumerischen Schlüssel handelt. Bei einem alphanumerischen Schlüssel wird der Buchstabe oder die Zahl des Schlüssels in doppelten Anführungszeichen mit dem **VIRTKEY-Flag** kombiniert. Bei einem nicht alphanumerischen Schlüssel wird der virtuelle Schlüsselcode für den spezifischen Schlüssel mit dem **VIRTKEY-Flag** kombiniert. In den folgenden Beispielen wird gezeigt, wie Sie Code Accelerators für virtuelle Schlüssel definieren.

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

Das folgende Beispiel zeigt eine Accelerator-Table-Ressource, die Zugriffstasten für Dateivorgänge definiert. Der Name der Ressource ist *FileAccel.*

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

Wenn der Benutzer die TASTEN ALT, UMSCHALT ODER STRG in einer Kombination mit der Tastenkombination drücken soll, geben Sie die Flags ALT, UMSCHALT und STRG in der Definition des Zugriffstastenbeschleunigers an. Hier einige Beispiele.

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

Wenn eine Zugriffstaste einem Menüelement entspricht, hebt das System das Menüelement standardmäßig hervor. Sie können das **NOINVERT-Flag** verwenden, um die Hervorhebung für einen einzelnen Accelerator zu verhindern. Im folgenden Beispiel wird die Verwendung des **NOINVERT-Flags** veranschaulicht:

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

Um Zugriffstasten zu definieren, die Menüelementen in Ihrer Anwendung entsprechen, schließen Sie die Zugriffstasten in den Text der Menüelemente ein. Das folgende Beispiel zeigt, wie Zugriffstasten in Menüelementtext in eine Ressourcendefinitionsdatei eingefügt werden.

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

### <a name="loading-the-accelerator-table-resource"></a>Laden der Accelerator-Tabellenressource

Eine Anwendung lädt eine Accelerator-Table-Ressource, indem sie die [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) aufruft und das Instanzhandler für die Anwendung anknübe, deren ausführbare Datei die Ressource und den Namen oder Bezeichner der Ressource enthält. **LoadAccelerators lädt** die angegebene Zugriffstastentabelle in den Arbeitsspeicher und gibt das Handle an die Zugriffstastentabelle zurück.

Eine Anwendung kann eine Zugriffstastentabellenressource jederzeit laden. In der Regel lädt eine Singlethreadanwendung ihre Zugriffstastentabelle, bevor sie in die Hauptnachrichtenschleife eintritt. Eine Anwendung, die mehrere Threads verwendet, lädt in der Regel die Accelerator-Table-Ressource für einen Thread, bevor sie in die Meldungsschleife für den Thread eintritt. Eine Anwendung oder ein Thread kann auch mehrere Zugriffstastentabellen verwenden, die jeweils einem bestimmten Fenster in der Anwendung zugeordnet sind. Eine solche Anwendung würde die Zugriffstastentabelle für das Fenster jedes Mal laden, wenn der Benutzer das Fenster aktiviert hat. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](/windows/desktop/ProcThread/processes-and-threads).

### <a name="calling-the-translate-accelerator-function"></a>Aufrufen der Translate Accelerator-Funktion

Um Zugriffstasten zu verarbeiten, muss die Meldungsschleife einer Anwendung (oder eines Threads) einen Aufruf der [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) enthalten. **TranslateAccelerator** vergleicht Tastatureingaben mit einer Zugriffstastentabelle und übersetzt, wenn eine Übereinstimmung gefunden wird, die Tastatureingaben in eine [**WM \_ COMMAND-Nachricht**](wm-command.md) (oder [**WM \_ SYSCOMMAND).**](wm-syscommand.md) Die Funktion sendet dann die Nachricht an eine Fensterprozedur. Die Parameter der **TranslateAccelerator-Funktion** umfassen das Handle für das Fenster, das **die WM \_ COMMAND-Nachrichten** empfangen soll, das Handle für die Zugriffstastentabelle, die zum Übersetzen von Zugriffstasten verwendet wird, und einen Zeiger auf eine [**MSG-Struktur,**](/windows/win32/api/winuser/ns-winuser-msg) die eine Nachricht aus der Warteschlange enthält. Das folgende Beispiel zeigt, wie **TranslateAccelerator** innerhalb einer Meldungsschleife aufruft.


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



### <a name="processing-wm_command-messages"></a>Verarbeiten von WM \_ COMMAND-Nachrichten

Wenn eine Zugriffstaste verwendet wird, empfängt das in der [**TranslateAccelerator-Funktion**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) angegebene Fenster eine [**WM \_ COMMAND-**](wm-command.md) oder [**WM \_ SYSCOMMAND-Meldung.**](wm-syscommand.md) Das niedrige Wort des *wParam-Parameters* enthält den Bezeichner der Zugriffstaste. Die Fensterprozedur untersucht den Bezeichner, um die Quelle der **WM \_ COMMAND-Nachricht** zu bestimmen und die Nachricht entsprechend zu verarbeiten.

Wenn eine Zugriffstaste einem Menüelement in der Anwendung entspricht, wird der Zugriffstaste und dem Menüelement in der Regel der gleiche Bezeichner zugewiesen. Wenn Sie wissen müssen, ob eine [**WM \_ COMMAND-Nachricht**](wm-command.md) von einer Zugriffstaste oder einem Menüelement generiert wurde, können Sie das obere Wort des *wParam-Parameters* untersuchen. Wenn eine Zugriffstaste die Nachricht generiert hat, ist das obere Wort 1. Wenn ein Menüelement die Nachricht generiert hat, ist das hohe Wort 0.

### <a name="destroying-the-accelerator-table-resource"></a>Zerstören der Accelerator-Tabellenressource

Das System zerstört automatisch accelerator-table-Ressourcen, die von der [**LoadAccelerators-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) geladen wurden, und entfernt die Ressource aus dem Arbeitsspeicher, nachdem die Anwendung geschlossen wurde.

### <a name="creating-accelerators-for-font-attributes"></a>Erstellen von Zugriffstasten für Schriftartattribute

Das Beispiel in diesem Abschnitt zeigt, wie sie die folgenden Aufgaben ausführen:

-   Erstellen Sie eine Accelerator-Table-Ressource.
-   Laden Sie die Zugriffstastentabelle zur Laufzeit.
-   Übersetzen von Zugriffstasten in einer Nachrichtenschleife.
-   Verarbeiten Von den Zugriffstasten generierte [**WM \_ COMMAND-Meldungen.**](wm-command.md)

Diese Aufgaben werden im Kontext einer Anwendung  gezeigt, die ein Zeichenmenü und entsprechende Zugriffstasten enthält, mit denen der Benutzer Attribute der aktuellen Schriftart auswählen kann.

Der folgende Teil einer Ressourcendefinitionsdatei definiert das **Menü Zeichen** und die zugeordnete Zugriffstastentabelle. Beachten Sie, dass die Menüelemente die Tastenkombinationen anzeigen und dass jede Zugriffstaste denselben Bezeichner wie das zugeordnete Menüelement hat.


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



In den folgenden Abschnitten der Quelldatei der Anwendung wird gezeigt, wie die Zugriffstasten implementiert werden.


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



## <a name="using-an-accelerator-table-created-at-run-time"></a>Verwenden einer zur Laufzeit erstellten Zugriffstastentabelle

In diesem Thema wird erläutert, wie Zugriffstastentabellen verwendet werden, die zur Laufzeit erstellt wurden.

-   [Erstellen einer Run-Time Accelerator-Tabelle](#creating-a-run-time-accelerator-table)
-   [Processing Accelerators](#processing-accelerators)
-   [Zerstören einer Run-Time Accelerator-Tabelle](#destroying-a-run-time-accelerator-table)
-   [Erstellen bearbeitbarer Accelerators für Benutzer](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a>Erstellen einer Run-Time Accelerator-Tabelle

Der erste Schritt beim Erstellen einer Zugriffstastentabelle zur Laufzeit ist das Füllen eines Arrays von [**ACCEL-Strukturen.**](/windows/win32/api/winuser/ns-winuser-accel) Jede Struktur im Array definiert einen Accelerator in der Tabelle. Die Definition eines Zugriffstasten enthält seine Flags, seinen Schlüssel und seinen Bezeichner. Die **ACCEL-Struktur** weist das folgende Format auf.

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

Sie definieren die Tastatureingabe einer Zugriffstaste, indem Sie einen ASCII-Zeichencode oder einen Code für virtuelle Schlüssel im **Schlüsselmember** der [**ACCEL-Struktur**](/windows/win32/api/winuser/ns-winuser-accel) angeben. Wenn Sie einen Virtuellen Schlüsselcode angeben, müssen Sie zuerst das **FVIRTKEY-Flag** in den **fVirt-Member** einschließen. Andernfalls interpretiert das System den Code als ASCII-Zeichencode. Sie können das **FCONTROL-,** **FALT-** oder **FSHIFT-Flag** oder alle drei einschließen, um die STRG-, ALT- oder UMSCHALTTASTE mit der Tastatureingabe zu kombinieren.

Um die Zugriffstastentabelle zu erstellen, übergeben Sie einen Zeiger auf das Array von [**ACCEL-Strukturen**](/windows/win32/api/winuser/ns-winuser-accel) an die [**CreateAcceleratorTable-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) **CreateAcceleratorTable** erstellt die Zugriffstastentabelle und gibt das Handle an die Tabelle zurück.

### <a name="processing-accelerators"></a>Verarbeitungsbeschleuniger

Das Laden und Aufrufen von Zugriffstasten, die von einer zur Laufzeit erstellten Zugriffstastentabelle bereitgestellt werden, entspricht der Verarbeitung derjenigen, die von einer Zugriffstastentabellenressource bereitgestellt werden. Weitere Informationen finden Sie unter [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through Processing WM COMMAND [ \_ Messages](/windows).

### <a name="destroying-a-run-time-accelerator-table"></a>Zerstören einer Run-Time Accelerator-Tabelle

Das System zerstört zur Laufzeit erstellte Zugriffstastentabellen automatisch und entfernt die Ressourcen aus dem Arbeitsspeicher, nachdem die Anwendung geschlossen wurde. Sie können eine Zugriffstastentabelle zuvor zerstören und aus dem Arbeitsspeicher entfernen, indem Sie das Handle der Tabelle an die [**DestroyAcceleratorTable-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) übergeben.

### <a name="creating-user-editable-accelerators"></a>Erstellen von bearbeitbaren Zugriffstasten für Benutzer

In diesem Beispiel wird gezeigt, wie Sie ein Dialogfeld erstellen, das es dem Benutzer ermöglicht, die einem Menüelement zugeordnete Zugriffstaste zu ändern. Das Dialogfeld besteht aus einem Kombinationsfeld mit Menüelementen, einem Kombinationsfeld mit den Namen der Schlüssel und Kontrollkästchen zum Auswählen der Tasten STRG, ALT und UMSCHALT. Die folgende Abbildung zeigt das Dialogfeld.

![Dialogfeld mit Kombinationsfeldern und Kontrollkästchen](images/useredit.gif)

Das folgende Beispiel zeigt, wie das Dialogfeld in der Ressourcendefinitionsdatei definiert wird.

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

Die Menüleiste der Anwendung  enthält ein Zeichenuntermenü, dessen Elementen Zugriffstasten zugeordnet sind.

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

Die Menüelementwerte für die Menüvorlage sind Konstanten, die in der Headerdatei der Anwendung wie folgt definiert sind.

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

Das Dialogfeld verwendet ein Array von anwendungsdefinierte VKEY-Strukturen, die jeweils eine Tastatureingabetextzeichenfolge und eine Accelerator-Textzeichenfolge enthalten. Wenn das Dialogfeld erstellt wird, analysiert es das Array und fügt jede Tastatureingabetextzeichenfolge dem Kombinationsfeld **Tastatureingabe auswählen** hinzu. Wenn der Benutzer auf die Schaltfläche **OK** klickt, sucht das Dialogfeld nach der ausgewählten Tastatureingabetextzeichenfolge und ruft die entsprechende Zugriffstastentextzeichenfolge ab. Das Dialogfeld fügt die Zeichenfolge accelerator-text an den Text des Menüelements an, das der Benutzer ausgewählt hat. Das folgende Beispiel zeigt das Array von VKEY-Strukturen:


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



Die Initialisierungsprozedur des Dialogfelds füllt die Kombinationsfelder **Element auswählen** und **Tastatureingabe auswählen** aus. Nachdem der Benutzer ein Menüelement und eine zugeordnete Zugriffstaste ausgewählt hat, überprüft das Dialogfeld die Steuerelemente im Dialogfeld, um die Auswahl des Benutzers abzurufen, aktualisiert den Text des Menüelements und erstellt dann eine neue Zugriffstastentabelle, die die benutzerdefinierte neue Zugriffstaste enthält. Das folgende Beispiel zeigt die Dialogfeldprozedur. Beachten Sie, dass Sie in der Fensterprozedur initialisieren müssen.


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



 

 