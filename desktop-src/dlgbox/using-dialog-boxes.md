---
title: Verwenden von Dialogfeldern
description: Sie verwenden Dialogfelder, um Informationen anzuzeigen und eingabeaufforderungen des Benutzers anzuzeigen.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows Benutzeroberfläche,Windowing
- Windows Benutzeroberfläche,Dialogfelder
- Fenster, Dialogfelder
- Dialogfelder, Informationen
- Dialogfelder, anzeigen
- Modale Dialogfelder
- Nicht modale Dialogfelder
- Dialogfelder,modal
- Dialogfelder, moduslos
- Dialogfelder,initialisieren
- Dialogfeldvorlagen
- Dialogfelder,Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ec5e97060697388224ac92f60b6043a188d4259520aaf151fb188c43f6bb64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720793"
---
# <a name="using-dialog-boxes"></a>Verwenden von Dialogfeldern

Sie verwenden Dialogfelder, um Informationen anzuzeigen und eingabeaufforderungen des Benutzers anzuzeigen. Ihre Anwendung lädt und initialisiert das Dialogfeld, verarbeitet Benutzereingaben und zerstört das Dialogfeld, wenn der Benutzer die Aufgabe abgeschlossen hat. Der Prozess für die Behandlung von Dialogfeldern variiert abhängig davon, ob das Dialogfeld modal oder moduslos ist. Ein modales Dialogfeld erfordert, dass der Benutzer das Dialogfeld schließt, bevor er ein anderes Fenster in der Anwendung aktiviert. Der Benutzer kann jedoch Fenster in verschiedenen Anwendungen aktivieren. Für ein nicht modusloses Dialogfeld ist keine sofortige Antwort des Benutzers erforderlich. Sie ähnelt einem Hauptfenster mit Steuerelementen.

In den folgenden Abschnitten wird erläutert, wie beide Arten von Dialogfeldern verwendet werden.

-   [Anzeigen eines Meldungsfelds](#displaying-a-message-box)
-   [Erstellen eines modalen Dialogfelds](#creating-a-modal-dialog-box)
-   [Erstellen eines dialogfelds ohne Modus](#creating-a-modeless-dialog-box)
-   [Initialisieren eines Dialogfelds](#initializing-a-dialog-box)
-   [Erstellen einer Vorlage im Arbeitsspeicher](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Anzeigen eines Meldungsfelds

Die einfachste Form des modalen Dialogfelds ist das Meldungsfeld. Die meisten Anwendungen verwenden Meldungsfelder, um den Benutzer vor Fehlern zu warnen und anweisungen zur Vorgehensweise nach einem Fehler zu erhalten. Sie erstellen ein Meldungsfeld, indem Sie die [**MessageBox-**](/windows/desktop/api/Winuser/nf-winuser-messagebox) oder [**MessageBoxEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) verwenden und dabei die Nachricht sowie die Anzahl und den Typ der anzuzeigenden Schaltflächen angeben. Das System erstellt ein modales Dialogfeld und stellt eine eigene Dialogfeldvorlage und -prozedur zur Verfügung. Nachdem der Benutzer das Meldungsfeld geschlossen hat, gibt **MessageBox** oder **MessageBoxEx** einen Wert zurück, der die Schaltfläche identifiziert, die der Benutzer zum Schließen des Meldungsfelds ausgewählt hat.

Im folgenden Beispiel zeigt die Anwendung ein Meldungsfeld an, in dem der Benutzer nach einem Fehlerzustand zur Eingabe einer Aktion aufgefordert wird. Im Meldungsfeld wird die Meldung angezeigt, in der die Fehlerbedingung und deren Behebung beschrieben werden. Der **MB \_ YESNO-Stil** leitet [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) an, zwei Schaltflächen zur Verfügung zu stellen, mit denen der Benutzer auswählen kann, wie der Vorgang fortgesetzt werden soll:


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



Die folgende Abbildung zeigt die Ausgabe des vorherigen Codebeispiels:

![Meldungsfeld](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Erstellen eines modalen Dialogfelds

Sie erstellen ein modales Dialogfeld mithilfe der [**DialogBox-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) Sie müssen den Bezeichner oder Namen einer Dialogfeldvorlagenressource und einen Zeiger auf die Dialogfeldprozedur angeben. Die **DialogBox-Funktion** lädt die Vorlage, zeigt das Dialogfeld an und verarbeitet alle Benutzereingaben, bis der Benutzer das Dialogfeld schließt.

Im folgenden Beispiel zeigt die Anwendung ein modales  Dialogfeld an, wenn der Benutzer in einem Anwendungsmenü auf Element löschen klickt. Das Dialogfeld enthält ein Bearbeitungssteuerelement (in das der Benutzer den Namen eines Elements ein gibt) sowie die **Schaltflächen OK** und **Abbrechen.** Die Steuerelementbezeichner für diese Steuerelemente sind ID \_ ITEMNAME, IDOK bzw. IDCANCEL.

Der erste Teil des Beispiels besteht aus den Anweisungen, die das modale Dialogfeld erstellen. Diese Anweisungen erstellen in der Fensterprozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn das System eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit dem IDM \_ DELETEITEM-Menübezeichner empfängt. Der zweite Teil des Beispiels ist die Dialogfeldprozedur, die den Inhalt des Bearbeitungssteuerfelds abruft und das Dialogfeld schließt, wenn eine **WM \_ COMMAND-Meldung empfangen** wird.

Mit den folgenden Anweisungen wird das modale Dialogfeld erstellt. Die Dialogfeldvorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcenbezeichner DLG \_ DELETEITEM.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



In diesem Beispiel gibt die Anwendung das Hauptfenster als Besitzerfenster für das Dialogfeld an. Wenn das System das Dialogfeld anfänglich anzeigt, ist seine Position relativ zur oberen linken Ecke des Clientbereichs des Besitzerfensters. Die Anwendung verwendet den Rückgabewert von [**DialogBox,**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) um zu bestimmen, ob der Vorgang fortgesetzt oder abgebrochen werden soll. Die folgenden Anweisungen definieren die Dialogfeldprozedur.


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



In diesem Beispiel verwendet die Prozedur [**GetDlgItemText,**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) um den aktuellen Text aus dem Bearbeitungssteuerelement abzurufen, das durch ID \_ ITEMNAME identifiziert wird. Die Prozedur ruft dann die [**EndDialog-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enddialog) auf, um den Rückgabewert des Dialogfelds je nach empfangener Nachricht auf IDOK oder IDCANCEL zu setzen und mit dem Schließen des Dialogfelds zu beginnen. Die IDOK- und IDCANCEL-Bezeichner entsprechen den **Schaltflächen OK** **und Abbrechen.** Nachdem die Prozedur **EndDialog** aufruft, sendet das System zusätzliche Nachrichten an die Prozedur, um das Dialogfeld zu zerstören, und gibt den Rückgabewert des Dialogfelds an die Funktion zurück, die das Dialogfeld erstellt hat.

## <a name="creating-a-modeless-dialog-box"></a>Erstellen eines dialogfelds ohne Modus

Sie erstellen ein nicht modusloses Dialogfeld, indem Sie die [**CreateDialog-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) verwenden und dabei den Bezeichner oder Namen einer Dialogfeldvorlagenressource und einen Zeiger auf die Dialogfeldprozedur angeben. **CreateDialog** lädt die Vorlage, erstellt das Dialogfeld und zeigt sie optional an. Ihre Anwendung ist für das Abrufen und Senden von Benutzereingabenachrichten an die Dialogfeldprozedur verantwortlich.

Im folgenden Beispiel zeigt die Anwendung ein nicht modusloses Dialogfeld an , wenn es nicht bereits angezeigt wird, wenn der Benutzer in einem Anwendungsmenü auf **Gehe** zu klickt. Das Dialogfeld enthält ein Bearbeitungssteuerfeld, ein Kontrollkästchen sowie **die Schaltflächen OK** **und Abbrechen.** Die Dialogfeldvorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcenbezeichner DLG \_ GOTO. Der Benutzer gibt eine Zeilennummer in das Bearbeitungssteuerfeld ein und überprüft das Kontrollkästchen, um anzugeben, dass die Zeilennummer relativ zur aktuellen Zeile ist. Die Steuerelementbezeichner sind ID \_ LINE, ID \_ ABSREL, IDOK und IDCANCEL.

Die Anweisungen im ersten Teil des Beispiels erstellen das dialogfeld ohne Modus. Diese Anweisungen erstellen in der Fensterprozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn die Fensterprozedur eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit dem IDM GOTO-Menübezeichner empfängt, jedoch nur, wenn die globale Variable noch kein gültiges Handle \_ enthält. Der zweite Teil des Beispiels ist die Hauptnachrichtenschleife der Anwendung. Die -Schleife enthält die [**IsDialogMessage-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) um sicherzustellen, dass der Benutzer die Tastaturschnittstelle des Dialogfelds in diesem moduslosen Dialogfeld verwenden kann. Der dritte Teil des Beispiels ist die Dialogfeldprozedur. Die Prozedur ruft den Inhalt des Bearbeitungssteuerfelds ab und kontrollkästchen, wenn der Benutzer auf die Schaltfläche **OK** klickt. Die Prozedur zerstört das Dialogfeld, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



In den vorherigen Anweisungen wird [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) nur aufgerufen, `hwndGoto` wenn kein gültiges Fensterhand handle enthält. Dadurch wird sichergestellt, dass die Anwendung nicht zwei Dialogfelder gleichzeitig zeigt. Um diese Überprüfungsmethode zu unterstützen, muss die Dialogprozedur auf **NULL** festgelegt werden, wenn sie das Dialogfeld zerstört.

Die Meldungsschleife für eine Anwendung besteht aus den folgenden Anweisungen.


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



Die -Schleife überprüft die Gültigkeit des Fensterhandpunkts für das Dialogfeld und ruft nur dann die [**IsDialogMessage-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) auf, wenn das Handle gültig ist. **IsDialogMessage** verarbeitet die Nachricht nur, wenn sie zum Dialogfeld gehört. Andernfalls wird **FALSE zurückgegeben,** und die Schleife gibt die Nachricht an das entsprechende Fenster weiter.

Die folgenden Anweisungen definieren die Dialogfeldprozedur.


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



In den vorherigen Anweisungen verarbeitet die Prozedur die [**WM \_ INITDIALOG-**](wm-initdialog.md) und [**WM \_ COMMAND-Meldungen.**](/windows/desktop/menurc/wm-command) Während **der WM \_ INITDIALOG-Verarbeitung** initialisiert die Prozedur das Kontrollkästchen, indem der aktuelle Wert der globalen Variablen an [**CheckDlgButton übergeben wird.**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) Die Prozedur gibt dann **TRUE zurück,** damit das System den Standardeingabefokus festlegen kann.

During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier. Die Prozedur muss [**DestroyWindow aufrufen,**](/windows/desktop/api/winuser/nf-winuser-destroywindow) um ein nicht modusloses Dialogfeld zu schließen. Beachten Sie, dass die Prozedur auch die Variable auf **NULL setzt,** um sicherzustellen, dass andere Anweisungen, die von dieser Variablen abhängen, ordnungsgemäß funktionieren.

Wenn der Benutzer auf die Schaltfläche **OK** klickt, ruft die Prozedur den aktuellen Status des Kontrollkästchens ab und weist ihn der **Variablen fRelative** zu. Anschließend wird die Variable verwendet, um die Zeilennummer aus dem Bearbeitungssteuerzeichen abzurufen. [**GetDlgItemInt übersetzt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) den Text im Bearbeitungssteuerfeld in eine ganze Zahl. Der Wert von **fRelative bestimmt,** ob die Funktion die Zahl als Wert mit Vorzeichen oder ohne Vorzeichen interpretiert. Wenn der Bearbeitungssteuertext keine gültige Zahl ist, legt **GetDlgItemInt** den Wert der **fError-Variablen** auf ungleich 0 (null) fest. Die Prozedur überprüft diesen Wert, um zu bestimmen, ob eine Fehlermeldung angezeigt oder die Aufgabe durchgeführt werden soll. Im Falle eines Fehlers sendet die Dialogfeldprozedur eine Nachricht an das Bearbeitungssteuerfeld und leitet es an, den Text im Steuerelement auszuwählen, damit der Benutzer ihn problemlos ersetzen kann. Wenn **GetDlgItemInt** keinen Fehler zurücksendet, kann die Prozedur entweder die angeforderte Aufgabe selbst durchführen oder eine Nachricht an das Besitzerfenster senden, um den Vorgang auszuführen.

## <a name="initializing-a-dialog-box"></a>Initialisieren eines Dialogfelds

Sie initialisieren das Dialogfeld und dessen Inhalt während der Verarbeitung der [**WM \_ INITDIALOG-Nachricht.**](wm-initdialog.md) Die häufigste Aufgabe besteht darin, die Steuerelemente so zu initialisieren, dass sie die aktuellen Dialogfeldeinstellungen widerspiegeln. Eine weitere häufige Aufgabe besteht darin, ein Dialogfeld auf dem Bildschirm oder innerhalb des Besitzerfensters zu zentriert. Eine nützliche Aufgabe für einige Dialogfelder besteht darin, den Eingabefokus auf ein angegebenes Steuerelement festzulegen, anstatt den Standardeingabefokus zu akzeptieren.

Im folgenden Beispiel fokus die Dialogfeldprozedur das Dialogfeld und legt den Eingabefokus fest, während die [**WM \_ INITDIALOG-Nachricht verarbeitet**](wm-initdialog.md) wird. Um das Dialogfeld zu zentriert, ruft die Prozedur die Fensterrechtecke für das Dialogfeld und das Besitzerfenster ab und berechnet eine neue Position für das Dialogfeld. Um den Eingabefokus festzulegen, überprüft die Prozedur den *wParam-Parameter,* um den Bezeichner des Standardeingabefokus zu bestimmen.


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



In den vorherigen Anweisungen verwendet die Prozedur die [**GetParent-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getparent) um das Besitzerfensterhandl in ein Dialogfeld abzurufen. Die Funktion gibt das Besitzerfensterhand handle an Dialogfelder und das übergeordnete Fensterhand handle an untergeordnete Fenster zurück. Da eine Anwendung ein Dialogfeld erstellen kann, das keinen Besitzer hat, überprüft die Prozedur das zurückgegebene Handle und verwendet bei Bedarf die [**GetDesktopWindow-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) um das Desktopfensterhand handle abzurufen. Nach der Berechnung der neuen Position verwendet die Prozedur die [**SetWindowPos-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) um das Dialogfeld zu verschieben, und gibt den HWND TOP-Wert an, um sicherzustellen, dass das Dialogfeld über dem Besitzerfenster \_ verbleibt.

Vor dem Festlegen des Eingabefokus überprüft die Prozedur den Steuerelementbezeichner des Standardeingabefokus. Das System übergibt das Fensterhand handle des Standardeingabefokus im *wParam-Parameter.* Die [**GetDlgCtrlID-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) gibt den Bezeichner für das Steuerelement zurück, das vom Fensterhandle identifiziert wird. Stimmt der Bezeichner nicht mit dem richtigen Bezeichner überein, verwendet die Prozedur die [**SetFocus-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setfocus) um den Eingabefokus zu setzen. Die [**GetDlgItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) ist erforderlich, um das Fensterhandl des gewünschten Steuerelements abzurufen.

## <a name="creating-a-template-in-memory"></a>Erstellen einer Vorlage im Arbeitsspeicher

Anwendungen passen den Inhalt von Dialogfeldern manchmal abhängig vom aktuellen Status der verarbeiteten Daten an oder ändern diesen. In solchen Fällen ist es nicht praktikabel, alle möglichen Dialogfeldvorlagen als Ressourcen in der ausführbaren Datei der Anwendung zur Verfügung zu stellen. Das Erstellen von Vorlagen im Arbeitsspeicher bietet der Anwendung jedoch mehr Flexibilität bei der Anpassung an beliebige Umstände.

Im folgenden Beispiel erstellt die Anwendung eine Vorlage im Arbeitsspeicher für ein modales Dialogfeld, das eine Meldung sowie die **Schaltflächen OK** und **Hilfe** enthält.

In einer Dialogvorlage müssen alle Zeichenfolgen, z. B. das Dialogfeld und schaltflächentitel, Unicode-Zeichenfolgen sein. In diesem Beispiel wird die [**MultiByteToWideChar-Funktion**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) verwendet, um diese Unicode-Zeichenfolgen zu generieren.

Die [**DLGITEMTEMPLATE-Strukturen**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) in einer Dialogvorlage müssen an **DWORD-Grenzen ausgerichtet** werden. Um diese Strukturen auszurichten, verwendet dieses Beispiel eine Hilfsroutine, die einen Eingabezeiger verwendet und den nächstgelegenen Zeiger zurückgibt, der an einer **DWORD-Grenze ausgerichtet** ist.


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 