---
title: Verwenden von Dialog Feldern
description: Mithilfe von Dialogfeldern können Sie Informationen anzeigen und Eingabeaufforderung für den Benutzer eingeben.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Windows-Benutzeroberfläche, Fenster
- Windows-Benutzeroberfläche, Dialogfelder
- Fenster, Dialogfelder
- Dialogfelder, Info
- Dialogfelder, anzeigen
- Modale Dialogfelder
- Nicht modale Dialogfelder
- Dialogfelder, Modal
- Dialogfelder, ohne Modell
- Dialogfelder, initialisieren
- Dialogfeld Vorlagen
- Dialogfelder, Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039419"
---
# <a name="using-dialog-boxes"></a>Verwenden von Dialog Feldern

Mithilfe von Dialogfeldern können Sie Informationen anzeigen und Eingabeaufforderung für den Benutzer eingeben. Die Anwendung lädt und initialisiert das Dialogfeld, verarbeitet Benutzereingaben und zerstört das Dialogfeld, wenn der Benutzer die Aufgabe beendet. Der Prozess für die Behandlung von Dialogfeldern variiert abhängig davon, ob das Dialogfeld modal oder nicht modelliert ist. Ein modales Dialogfeld erfordert, dass der Benutzer das Dialogfeld schließt, bevor ein anderes Fenster in der Anwendung aktiviert wird. Der Benutzer kann jedoch Fenster in verschiedenen Anwendungen aktivieren. Ein nicht modalem Dialogfeld erfordert keine sofortige Antwort vom Benutzer. Es ähnelt einem Hauptfenster, das-Steuerelemente enthält.

In den folgenden Abschnitten wird erläutert, wie beide Arten von Dialogfeldern verwendet werden.

-   [Anzeigen eines Meldungs Felds](#displaying-a-message-box)
-   [Erstellen eines modalen Dialog Felds](#creating-a-modal-dialog-box)
-   [Erstellen eines nicht modalem Dialog Felds](#creating-a-modeless-dialog-box)
-   [Initialisieren eines Dialog Felds](#initializing-a-dialog-box)
-   [Erstellen einer Vorlage im Speicher](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a>Anzeigen eines Meldungs Felds

Die einfachste Form eines modalen Dialog Felds ist das Meldungs Feld. Die meisten Anwendungen verwenden Meldungs Felder, um den Fehler des Benutzers zu warnen und Anweisungen einzugeben, wie nach einem Fehler fortgefahren werden kann. Sie erstellen ein Meldungs Feld mit der [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) -Funktion oder der [**messageboxex**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) -Funktion, indem Sie die Meldung sowie die Anzahl und den Typ der anzuzeigenden Schaltflächen angeben. Das System erstellt ein modales Dialogfeld, das eine eigene Dialogfeld Vorlage und eine eigene Prozedur bereitstellt. Nachdem der Benutzer das Meldungs Feld geschlossen hat, gibt **MessageBox** oder **messageboxex** einen Wert zurück, der die Schaltfläche identifiziert, die der Benutzer zum Schließen des Meldungs Felds ausgewählt hat.

Im folgenden Beispiel zeigt die Anwendung ein Meldungs Feld an, das den Benutzer zur Eingabe einer Aktion auffordert, nachdem ein Fehler aufgetreten ist. Im Meldungs Feld wird die Meldung angezeigt, in der der Fehlerzustand und die Lösung beschrieben werden. Das Format **MB \_ YesNo** weist [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) an, zwei Schaltflächen bereitzustellen, mit denen der Benutzer auswählen kann, wie der Vorgang fortgesetzt werden soll:


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



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Code Beispiels:

![Meldungs Feld](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a>Erstellen eines modalen Dialog Felds

Sie erstellen ein modales Dialogfeld mit der Funktion [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Sie müssen den Bezeichner oder den Namen einer Dialogfeld Vorlagen-Ressource und einen Zeiger auf die Dialogfeld Prozedur angeben. Die Funktion **Dialogbox** lädt die Vorlage, zeigt das Dialogfeld an und verarbeitet alle Benutzereingaben, bis der Benutzer das Dialogfeld schließt.

Im folgenden Beispiel zeigt die Anwendung ein modales Dialogfeld an, wenn der Benutzer im Anwendungsmenü auf **Element löschen** klickt. Das Dialogfeld enthält ein Bearbeitungs Steuerelement (in dem der Benutzer den Namen eines Elements eingibt) und die Schaltflächen " **OK** " und " **Abbrechen** ". Die Steuerelement Bezeichner für diese Steuerelemente sind ID \_ ItemName, IDOK bzw. IDCANCEL.

Der erste Teil des Beispiels besteht aus den Anweisungen, die das modale Dialogfeld erstellen. Diese Anweisungen erstellen Sie in der Fenster Prozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn das System eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht mit dem IDM \_ DeleteItem-Menü Bezeichner empfängt. Der zweite Teil des Beispiels ist die Dialogfeld Prozedur, die den Inhalt des Bearbeitungs Steuer Elements abruft und das Dialogfeld nach dem Empfang einer **WM- \_ Befehls** Meldung schließt.

Die folgenden Anweisungen erstellen das modale Dialogfeld. Die Dialogfeld Vorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcen Bezeichner DLG \_ DeleteItem.


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



In diesem Beispiel gibt die Anwendung das Hauptfenster als Besitzer Fenster für das Dialogfeld an. Wenn das System das Dialogfeld anfänglich anzeigt, ist seine Position relativ zur oberen linken Ecke des Client Bereichs des Besitzer Fensters. Die Anwendung verwendet den Rückgabewert aus [**Dialogbox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) , um zu bestimmen, ob der Vorgang fortgesetzt oder abgebrochen werden soll. Die folgenden Anweisungen definieren die Dialogfeld Prozedur.


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



In diesem Beispiel verwendet die Prozedur [**getdlgitemtext**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , um den aktuellen Text aus dem Bearbeitungs Steuerelement abzurufen, das durch ID \_ ItemName identifiziert wird. Die Prozedur ruft dann die [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) -Funktion auf, um den Rückgabewert des Dialog Felds abhängig von der empfangenen Nachricht entweder auf IDOK oder IDCANCEL festzulegen, und beginnt damit, das Dialogfeld zu schließen. Die IDOK-und IDCANCEL-Bezeichner entsprechen den Schaltflächen **OK** und **Abbrechen** . Nachdem die Prozedur **EndDialog** aufgerufen hat, sendet das System zusätzliche Meldungen an die Prozedur, um das Dialogfeld zu zerstören, und gibt den Rückgabewert des Dialog Felds zurück an die Funktion, die das Dialogfeld erstellt hat.

## <a name="creating-a-modeless-dialog-box"></a>Erstellen eines nicht modalem Dialog Felds

Sie erstellen ein nicht modalem Dialogfeld mithilfe der Funktion "up [**Dialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) ", indem Sie den Bezeichner oder den Namen einer Dialogfeld Vorlagen Ressource und einen Zeiger auf die Dialogfeld Prozedur angeben. Mit " **anatedialog** " wird die Vorlage geladen, das Dialogfeld erstellt und optional angezeigt. Die Anwendung ist für das Abrufen und Verteilen von Benutzereingabe Nachrichten an die Dialogfeld Prozedur zuständig.

Im folgenden Beispiel zeigt die Anwendung ein nicht modalem Dialogfeld an – wenn Sie nicht bereits angezeigt wird –, wenn der Benutzer in einem Anwendungsmenü **auf "Gehe zu** " klickt. Das Dialogfeld enthält ein Bearbeitungs Steuerelement, ein Kontrollkästchen und Schaltflächen " **OK** " und " **Abbrechen** ". Die Dialogfeld Vorlage ist eine Ressource in der ausführbaren Datei der Anwendung und verfügt über den Ressourcen Bezeichner DLG \_ goto. Der Benutzer gibt eine Zeilennummer in das Bearbeitungs Steuerelement ein und überprüft das Kontrollkästchen, um anzugeben, dass die Zeilennummer relativ zur aktuellen Zeile ist. Die Steuerelement-IDs sind ID- \_ Zeile, ID- \_ absrel, IDOK und IDCANCEL.

Mit den-Anweisungen im ersten Teil des Beispiels wird das nicht modante Dialogfeld erstellt. Diese Anweisungen erstellen Sie in der Fenster Prozedur für das Hauptfenster der Anwendung das Dialogfeld, wenn die Fenster Prozedur eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht mit dem IDM- \_ goto-Menü Bezeichner empfängt, aber nur, wenn die globale Variable nicht bereits ein gültiges Handle enthält. Der zweite Teil des Beispiels ist die Hauptnachrichten Schleife der Anwendung. Die-Schleife schließt die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion ein, um sicherzustellen, dass der Benutzer die Dialogfeld-Tastaturschnittstelle im Dialogfeld "nicht modess" verwenden kann. Der dritte Teil des Beispiels ist die Dialogfeld Prozedur. Die Prozedur ruft den Inhalt des Bearbeitungs Steuer Elements und des Kontrollkästchens ab, wenn der Benutzer auf die Schaltfläche **OK** klickt. Die Prozedur zerstört das Dialogfeld, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt.


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



In den vorangehenden Anweisungen wird " [**foratedialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) " nur aufgerufen, wenn kein `hwndGoto` gültiges Fenster Handle enthält. Dadurch wird sichergestellt, dass die Anwendung nicht gleichzeitig zwei Dialogfelder anzeigt. Zur Unterstützung dieser Überprüfungs Methode muss die Dialogfeld Prozedur auf **null** festgelegt werden, wenn das Dialogfeld zerstört wird.

Die Nachrichten Schleife für eine Anwendung besteht aus den folgenden Anweisungen.


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



Die-Schleife prüft die Gültigkeit des Fenster Handles auf das Dialogfeld und ruft nur die [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) -Funktion auf, wenn das Handle gültig ist. **IsDialogMessage** verarbeitet die Nachricht nur, wenn Sie zum Dialogfeld gehört. Andernfalls wird **false** zurückgegeben, und die Schleife sendet die Nachricht an das entsprechende Fenster.

Die folgenden Anweisungen definieren die Dialogfeld Prozedur.


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



In den vorangehenden Anweisungen verarbeitet die Prozedur die [**\_ Befehle**](/windows/desktop/menurc/wm-command) " [**WM \_ InitDialog**](wm-initdialog.md) " und "WM". Während der **WM \_ InitDialog** -Verarbeitung wird das Kontrollkästchen durch die Prozedur initialisiert, indem der aktuelle Wert der globalen Variablen an [**checkdlgbutton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx)übergeben wird. Die Prozedur gibt dann " **true** " zurück, um das System anzuweisen, den Standardeingabe Fokus festzulegen.

Während der [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Verarbeitung schließt die Prozedur das Dialogfeld nur dann, wenn der Benutzer auf die Schaltfläche **Abbrechen** klickt, d. –. auf die Schaltfläche mit dem IDCANCEL-Bezeichner. Die Prozedur muss [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) aufzurufen, um ein nicht modalem Dialogfeld zu schließen. Beachten Sie, dass die-Prozedur auch die-Variable auf **null** festlegt, um sicherzustellen, dass andere, von dieser Variable abhängige-Anweisungen ordnungsgemäß funktionieren.

Wenn der Benutzer auf die Schaltfläche **OK** klickt, ruft die Prozedur den aktuellen Zustand des Kontrollkästchens ab und weist Sie der **frelative** Variablen zu. Anschließend wird die-Variable verwendet, um die Zeilennummer aus dem Bearbeitungs Steuerelement abzurufen. [**Getdlgitemint**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) übersetzt den Text im Bearbeitungs Steuerelement in eine ganze Zahl. Der Wert von **frelative** bestimmt, ob die Funktion die Zahl als einen Wert mit oder ohne Vorzeichen interpretiert. Wenn der Bearbeitungs Steuerelement-Text keine gültige Zahl ist, legt **getdlgitemint** den Wert der **ferror** -Variable auf einen Wert ungleich 0 (null) fest. Die Prozedur überprüft diesen Wert, um zu bestimmen, ob eine Fehlermeldung angezeigt oder die Aufgabe durchgeführt werden soll. Wenn ein Fehler auftritt, sendet die Dialogfeld Prozedur eine Nachricht an das Bearbeitungs Steuerelement und leitet Sie an den Text im Steuerelement weiter, sodass der Benutzer Sie problemlos ersetzen kann. Wenn **getdlgitemint** keinen Fehler zurückgibt, kann die Prozedur entweder die angeforderte Aufgabe selbst ausführen oder eine Nachricht an das Besitzer Fenster senden, um den Vorgang auszuführen.

## <a name="initializing-a-dialog-box"></a>Initialisieren eines Dialog Felds

Beim Verarbeiten der " [**WM \_ InitDialog**](wm-initdialog.md) "-Nachricht initialisieren Sie das Dialogfeld und seinen Inhalt. Die häufigste Aufgabe besteht darin, die Steuerelemente zu initialisieren, um die aktuellen Dialogfeld Einstellungen widerzuspiegeln. Eine weitere häufige Aufgabe besteht darin, ein Dialogfeld auf dem Bildschirm oder innerhalb des Besitzer Fensters zu zentrieren. Eine nützliche Aufgabe für einige Dialogfelder besteht darin, den Eingabefokus auf ein angegebenes Steuerelement festzulegen, anstatt den Standardeingabe Fokus zu akzeptieren.

Im folgenden Beispiel zentriert die Dialogfeld Prozedur das Dialogfeld und legt den Eingabefokus bei der Verarbeitung der [**WM \_ InitDialog**](wm-initdialog.md) -Nachricht fest. Um das Dialogfeld zu zentrieren, ruft die Prozedur die Fenster Rechtecke für das Dialogfeld und das Besitzer Fenster ab und berechnet eine neue Position für das Dialogfeld. Um den Eingabefokus festzulegen, überprüft die Prozedur den *wParam* -Parameter, um den Bezeichner des Standardeingabe Fokus zu ermitteln.


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



In den vorangehenden Anweisungen verwendet die Prozedur die [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) -Funktion, um das Besitzer Fenster Handle in ein Dialogfeld abzurufen. Die-Funktion gibt das Besitzer Fenster Handle für Dialogfelder und das übergeordnete Fenster Handle für untergeordnete Fenster zurück. Da eine Anwendung ein Dialogfeld ohne Besitzer erstellen kann, prüft die Prozedur das zurückgegebene Handle und verwendet die [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) -Funktion, um das Desktop Fenster Handle bei Bedarf abzurufen. Nach der Berechnung der neuen Position verwendet die Prozedur die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion, um das Dialogfeld zu verschieben. dabei wird der erste HWND-Wert angegeben, \_ um sicherzustellen, dass das Dialogfeld oben im Besitzer Fenster bleibt.

Bevor der Eingabefokus festgelegt wird, überprüft die Prozedur den Steuerelement Bezeichner des Standardeingabe Fokus. Das System übergibt das Fenster Handle des Standardeingabe Fokus im *wParam* -Parameter. Die [**getdlgctrlid**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) -Funktion gibt den Bezeichner für das Steuerelement zurück, das durch das Fenster Handle identifiziert wird. Wenn der Bezeichner nicht mit dem richtigen Bezeichner identisch ist, verwendet die Prozedur die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion, um den Eingabefokus festzulegen. Die [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) -Funktion ist erforderlich, um das Fenster Handle des gewünschten Steuer Elements abzurufen.

## <a name="creating-a-template-in-memory"></a>Erstellen einer Vorlage im Speicher

Anwendungen passen oder ändern den Inhalt von Dialogfeldern abhängig vom aktuellen Status der verarbeiteten Daten. In solchen Fällen ist es nicht praktikabel, alle möglichen Dialogfeld Vorlagen als Ressourcen in der ausführbaren Datei der Anwendung bereitzustellen. Das Erstellen von Vorlagen im Arbeitsspeicher bietet der Anwendung jedoch mehr Flexibilität bei der Anpassung an jede Situation.

Im folgenden Beispiel erstellt die Anwendung eine Vorlage im Arbeitsspeicher für ein modales Dialogfeld, das die Schaltflächen Nachricht und **OK** und **Hilfe** enthält.

In einer Dialogfeld Vorlage müssen alle Zeichen folgen, z. b. das Dialogfeld und die Schaltflächen Titel, Unicode-Zeichen folgen sein. In diesem Beispiel werden diese Unicode-Zeichen folgen mithilfe der [**multibytetewidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) -Funktion generiert.

Die [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) -Strukturen in einer Dialogfeld Vorlage müssen an den **DWORD** -Grenzen ausgerichtet sein. Um diese Strukturen auszurichten, wird in diesem Beispiel eine Hilfsroutine verwendet, die einen Eingabe Zeiger annimmt und den nächstgelegenen Zeiger zurückgibt, der an einer **DWORD** -Grenze ausgerichtet ist.


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



 

 