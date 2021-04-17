---
title: Verwenden der Zwischenablage
description: 'Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:'
ms.assetid: 377fb2cc-5b46-481a-8222-9291e504ae2c
keywords:
- Zwischenablage, Daten werden abgeschnitten
- Zwischenablage, Kopieren von Daten
- Zwischenablage, Einfügen von Daten
- Zwischenablage, auswählen von Daten
- Zwischenablage, Menübefehle bearbeiten
- Zwischenablage, Viewer
- Zwischenablage, Viewer-Fenster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c7e7d6db6f25bc1016eefbcc5afc9f5e0db44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315459"
---
# <a name="using-the-clipboard"></a>Verwenden der Zwischenablage

Dieser Abschnitt enthält Codebeispiele für die folgenden Aufgaben:

-   [Implementieren der Befehle zum Ausschneiden, kopieren und Einfügen](#implementing-the-cut-copy-and-paste-commands)
    -   [Auswählen von Daten](#selecting-data)
    -   [Erstellen eines Bearbeitungs Menüs](#creating-an-edit-menu)
    -   [Verarbeiten der "WM \_ initmenupopup"-Meldung](#processing-the-wm_initmenupopup-message)
    -   [Verarbeiten der WM- \_ Befehls Meldung](#processing-the-wm_command-message)
    -   [Kopieren von Informationen in die Zwischenablage](#copying-information-to-the-clipboard)
    -   [Einfügen von Informationen aus der Zwischenablage](#pasting-information-from-the-clipboard)
    -   [Registrieren eines Zwischenablage Formats](#registering-a-clipboard-format)
    -   [Verarbeiten der \_ Nachrichten "WM Renderformat" und "WM \_ renderallformats"](#processing-the-wm_renderformat-and-wm_renderallformats-messages)
    -   [Verarbeiten der WM \_ destroyclipboard-Nachricht](#processing-the-wm_destroyclipboard-message)
    -   [Verwenden des Owner-Display-Zwischenablage Formats](#using-the-owner-display-clipboard-format)
-   [Überwachen der Zwischenablage](#monitoring-clipboard-contents)
-   [Abfragen der Zwischenablage-Sequenznummer](#querying-the-clipboard-sequence-number)
-   [Erstellen eines-Zwischenablage-formatlistener](#creating-a-clipboard-format-listener)
-   [Erstellen eines Zwischenablage-Viewer-Fensters](#creating-a-clipboard-viewer-window)
-   [Hinzufügen eines Fensters zur Zwischenablage-Viewer-Kette](#adding-a-window-to-the-clipboard-viewer-chain)
    -   [Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht](#processing-the-wm_changecbchain-message)
    -   [Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette](#removing-a-window-from-the-clipboard-viewer-chain)
    -   [Die WM- \_ drawclipboard-Nachricht wird verarbeitet.](#processing-the-wm_drawclipboard-message)
    -   [Beispiel für einen Zwischenablage-Viewer](#example-of-a-clipboard-viewer)

## <a name="implementing-the-cut-copy-and-paste-commands"></a>Implementieren der Befehle zum Ausschneiden, kopieren und Einfügen

In diesem Abschnitt wird beschrieben, wie Standard Befehle zum **Ausschneiden**, **Kopieren** und **Einfügen** in einer Anwendung implementiert werden. Das Beispiel in diesem Abschnitt verwendet diese Methoden, um Daten in der Zwischenablage mithilfe eines registrierten Zwischenablage Formats, des CF-Besitzer **\_ Anzeige** Formats und des **CF- \_ Text** Formats zu platzieren. Das registrierte Format wird verwendet, um rechteckige oder elliptische Textfenster darzustellen, die als Bezeichnungen bezeichnet werden.

### <a name="selecting-data"></a>Auswählen von Daten

Bevor Informationen in die Zwischenablage kopiert werden können, muss der Benutzer bestimmte Informationen auswählen, die kopiert oder ausgeschnitten werden. Eine Anwendung sollte dem Benutzer die Möglichkeit bieten, Informationen innerhalb eines Dokuments auszuwählen, und eine Art visuelles Feedback, um die ausgewählten Daten anzugeben.

### <a name="creating-an-edit-menu"></a>Erstellen eines Bearbeitungs Menüs

Eine Anwendung sollte eine Zugriffstasten Tabelle mit den Standard-Tastatur Acceleratoren für die Befehle Menü **Bearbeiten** laden. Die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion muss der Nachrichten Schleife der Anwendung hinzugefügt werden, damit die Accelerators wirksam werden. Weitere Informationen zu Tastatur Accelerators finden Sie unter [Tastaturbeschleuniger](/windows/desktop/menurc/keyboard-accelerators).

### <a name="processing-the-wm_initmenupopup-message"></a>Verarbeiten der "WM \_ initmenupopup"-Meldung

Nicht alle Zwischenablage Befehle stehen dem Benutzer zu einem bestimmten Zeitpunkt zur Verfügung. Eine Anwendung sollte die " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) "-Meldung verarbeiten, um die Menü Elemente für verfügbare Befehle zu aktivieren und nicht verfügbare Befehle zu deaktivieren.

Im folgenden finden Sie den Fall " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) " für eine Anwendung namens "Label".


```
case WM_INITMENUPOPUP:
    InitMenu((HMENU) wParam);
    break;
```



Die InitMenu-Funktion ist wie folgt definiert.


```
void WINAPI InitMenu(HMENU hmenu) 
{ 
    int  cMenuItems = GetMenuItemCount(hmenu); 
    int  nPos; 
    UINT id; 
    UINT fuFlags; 
    PLABELBOX pbox = (hwndSelected == NULL) ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    for (nPos = 0; nPos < cMenuItems; nPos++) 
    { 
        id = GetMenuItemID(hmenu, nPos); 
 
        switch (id) 
        { 
            case IDM_CUT: 
            case IDM_COPY: 
            case IDM_DELETE: 
                if (pbox == NULL || !pbox->fSelected) 
                    fuFlags = MF_BYCOMMAND | MF_GRAYED; 
                else if (pbox->fEdit) 
                    fuFlags = (id != IDM_DELETE && pbox->ichSel 
                            == pbox->ichCaret) ? 
                        MF_BYCOMMAND | MF_GRAYED : 
                        MF_BYCOMMAND | MF_ENABLED; 
                else 
                    fuFlags = MF_BYCOMMAND | MF_ENABLED; 
 
                EnableMenuItem(hmenu, id, fuFlags); 
                break; 
 
            case IDM_PASTE: 
                if (pbox != NULL && pbox->fEdit) 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable(CF_TEXT) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
                else 
                    EnableMenuItem(hmenu, id, 
                        IsClipboardFormatAvailable( 
                                uLabelFormat) ? 
                            MF_BYCOMMAND | MF_ENABLED : 
                            MF_BYCOMMAND | MF_GRAYED 
                    ); 
 
        } 
    } 
}
```



### <a name="processing-the-wm_command-message"></a>Verarbeiten der WM- \_ Befehls Meldung

Um Menübefehle zu verarbeiten, fügen Sie den [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Fall zur Hauptfenster Prozedur Ihrer Anwendung hinzu. Im folgenden finden Sie den **WM- \_ Befehls** Fall für die Fenster Prozedur der Bezeichnung Anwendung.


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_CUT: 
            if (EditCopy()) 
                EditDelete(); 
            break; 
 
        case IDM_COPY: 
            EditCopy(); 
            break; 
 
        case IDM_PASTE: 
            EditPaste(); 
            break; 
 
        case IDM_DELETE: 
            EditDelete(); 
            break; 
 
        case IDM_EXIT: 
            DestroyWindow(hwnd); 
    } 
    break; 
```



Um die Befehle zum **Kopieren** und **Ausschneiden** auszuführen, ruft die Fenster Prozedur die Anwendungs definierte EditCopy-Funktion auf. Weitere Informationen finden Sie unter [Kopieren von Informationen in die Zwischenablage](#copying-information-to-the-clipboard). Um den Befehl **Einfügen** auszuführen, ruft die Fenster Prozedur die Anwendungs definierte EditPaste-Funktion auf. Weitere Informationen zur EditPaste-Funktion finden Sie unter [Einfügen von Informationen aus der Zwischenablage](#pasting-information-from-the-clipboard).

### <a name="copying-information-to-the-clipboard"></a>Kopieren von Informationen in die Zwischenablage

In der Label-Anwendung kopiert die von der Anwendung definierte EditCopy-Funktion die aktuelle Auswahl in die Zwischenablage. Diese Funktion führt Folgendes aus:

1.  Öffnet die Zwischenablage durch Aufrufen der [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) -Funktion.
2.  Leert die Zwischenablage durch Aufrufen der [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) -Funktion.
3.  Ruft die [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion einmal für jedes Zwischenablage Format auf, das die Anwendung bereitstellt.
4.  Schließt die Zwischenablage, indem die [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) -Funktion aufgerufen wird.

Abhängig von der aktuellen Auswahl kopiert die EditCopy-Funktion entweder einen Textbereich oder kopiert eine Anwendungs definierte Struktur, die eine ganze Bezeichnung darstellt. Die Struktur namens "LabelBox" ist wie folgt definiert.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Im folgenden finden Sie die Funktion "EditCopy".


```
BOOL WINAPI EditCopy(VOID) 
{ 
    PLABELBOX pbox; 
    LPTSTR  lptstrCopy; 
    HGLOBAL hglbCopy; 
    int ich1, ich2, cch; 
 
    if (hwndSelected == NULL) 
        return FALSE; 
 
    // Open the clipboard, and empty it. 
 
    if (!OpenClipboard(hwndMain)) 
        return FALSE; 
    EmptyClipboard(); 
 
    // Get a pointer to the structure for the selected label. 
 
    pbox = (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If text is selected, copy it using the CF_TEXT format. 
 
    if (pbox->fEdit) 
    { 
        if (pbox->ichSel == pbox->ichCaret)     // zero length
        {   
            CloseClipboard();                   // selection 
            return FALSE; 
        } 
 
        if (pbox->ichSel < pbox->ichCaret) 
        { 
            ich1 = pbox->ichSel; 
            ich2 = pbox->ichCaret; 
        } 
        else 
        { 
            ich1 = pbox->ichCaret; 
            ich2 = pbox->ichSel; 
        } 
        cch = ich2 - ich1; 
 
        // Allocate a global memory object for the text. 
 
        hglbCopy = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglbCopy == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
 
        // Lock the handle and copy the text to the buffer. 
 
        lptstrCopy = GlobalLock(hglbCopy); 
        memcpy(lptstrCopy, &pbox->atchLabel[ich1], 
            cch * sizeof(TCHAR)); 
        lptstrCopy[cch] = (TCHAR) 0;    // null character 
        GlobalUnlock(hglbCopy); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglbCopy); 
    } 
 
    // If no text is selected, the label as a whole is copied. 
 
    else 
    { 
        // Save a copy of the selected label as a local memory 
        // object. This copy is used to render data on request. 
        // It is freed in response to the WM_DESTROYCLIPBOARD 
        // message. 
 
        pboxLocalClip = (PLABELBOX) LocalAlloc( 
            LMEM_FIXED, 
            sizeof(LABELBOX) 
        ); 
        if (pboxLocalClip == NULL) 
        { 
            CloseClipboard(); 
            return FALSE; 
        } 
        memcpy(pboxLocalClip, pbox, sizeof(LABELBOX)); 
        pboxLocalClip->fSelected = FALSE; 
        pboxLocalClip->fEdit = FALSE; 
 
        // Place a registered clipboard format, the owner-display 
        // format, and the CF_TEXT format on the clipboard using 
        // delayed rendering. 
 
        SetClipboardData(uLabelFormat, NULL); 
        SetClipboardData(CF_OWNERDISPLAY, NULL); 
        SetClipboardData(CF_TEXT, NULL); 
    } 
 
    // Close the clipboard. 
 
    CloseClipboard(); 
 
    return TRUE; 
}
```



### <a name="pasting-information-from-the-clipboard"></a>Einfügen von Informationen aus der Zwischenablage

In der Label-Anwendung fügt die von der Anwendung definierte EditPaste-Funktion den Inhalt der Zwischenablage ein. Diese Funktion führt Folgendes aus:

1.  Öffnet die Zwischenablage durch Aufrufen der [**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard) -Funktion.
2.  Bestimmt, welche der verfügbaren Zwischenablage Formate abgerufen werden sollen.
3.  Ruft das Handle für die Daten im ausgewählten Format ab, indem die [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) -Funktion aufgerufen wird.
4.  Fügt eine Kopie der Daten in das Dokument ein.

    Das von [**GetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata) zurückgegebene Handle befindet sich immer noch im Besitz der Zwischenablage, sodass eine Anwendung Sie nicht freigeben oder gesperrt bleiben darf.

5.  Schließt die Zwischenablage, indem die [**CloseClipboard**](/windows/desktop/api/Winuser/nf-winuser-closeclipboard) -Funktion aufgerufen wird.

Wenn eine Bezeichnung ausgewählt ist und eine Einfügemarke enthält, fügt die EditPaste-Funktion den Text aus der Zwischenablage an der Einfügemarke ein. Wenn keine Auswahl vorhanden ist oder eine Bezeichnung ausgewählt ist, erstellt die Funktion eine neue Bezeichnung und verwendet dabei die von der Anwendung definierte LabelBox-Struktur in der Zwischenablage. Die LabelBox-Struktur wird mithilfe eines registrierten Zwischenablage Formats in der Zwischenablage platziert.

Die Struktur namens "LabelBox" ist wie folgt definiert.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```



Im folgenden finden Sie die EditPaste-Funktion.


```
VOID WINAPI EditPaste(VOID) 
{ 
    PLABELBOX pbox; 
    HGLOBAL   hglb; 
    LPTSTR    lptstr; 
    PLABELBOX pboxCopy; 
    int cx, cy; 
    HWND hwnd; 
 
    pbox = hwndSelected == NULL ? NULL : 
        (PLABELBOX) GetWindowLong(hwndSelected, 0); 
 
    // If the application is in edit mode, 
    // get the clipboard text. 
 
    if (pbox != NULL && pbox->fEdit) 
    { 
        if (!IsClipboardFormatAvailable(CF_TEXT)) 
            return; 
        if (!OpenClipboard(hwndMain)) 
            return; 
 
        hglb = GetClipboardData(CF_TEXT); 
        if (hglb != NULL) 
        { 
            lptstr = GlobalLock(hglb); 
            if (lptstr != NULL) 
            { 
                // Call the application-defined ReplaceSelection 
                // function to insert the text and repaint the 
                // window. 
 
                ReplaceSelection(hwndSelected, pbox, lptstr); 
                GlobalUnlock(hglb); 
            } 
        } 
        CloseClipboard(); 
 
        return; 
    } 
 
    // If the application is not in edit mode, 
    // create a label window. 
 
    if (!IsClipboardFormatAvailable(uLabelFormat)) 
        return; 
    if (!OpenClipboard(hwndMain)) 
        return; 
 
    hglb = GetClipboardData(uLabelFormat); 
    if (hglb != NULL) 
    { 
        pboxCopy = GlobalLock(hglb); 
        if (pboxCopy != NULL) 
        { 
            cx = pboxCopy->rcText.right + CX_MARGIN; 
            cy = pboxCopy->rcText.top * 2 + cyText; 
 
            hwnd = CreateWindowEx( 
                WS_EX_NOPARENTNOTIFY | WS_EX_TRANSPARENT, 
                atchClassChild, NULL, WS_CHILD, 0, 0, cx, cy, 
                hwndMain, NULL, hinst, NULL 
            ); 
            if (hwnd != NULL) 
            { 
                pbox = (PLABELBOX) GetWindowLong(hwnd, 0); 
                memcpy(pbox, pboxCopy, sizeof(LABELBOX)); 
                ShowWindow(hwnd, SW_SHOWNORMAL); 
                SetFocus(hwnd); 
            } 
            GlobalUnlock(hglb); 
        } 
    } 
    CloseClipboard(); 
}
```



### <a name="registering-a-clipboard-format"></a>Registrieren eines Zwischenablage Formats

Fügen Sie zum Registrieren eines Zwischenablage Formats wie folgt einen aufzurufenden Befehl der [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion zur instanzinitialisierungs Funktion Ihrer Anwendung hinzu.


```
// Register a clipboard format. 
 
// We assume that atchTemp can contain the format name and
// a null-terminator, otherwise it is truncated.
//
LoadString(hinstCurrent, IDS_FORMATNAME, atchTemp, 
    sizeof(atchTemp)/sizeof(TCHAR)); 
uLabelFormat = RegisterClipboardFormat(atchTemp); 
if (uLabelFormat == 0) 
    return FALSE;
```



### <a name="processing-the-wm_renderformat-and-wm_renderallformats-messages"></a>Verarbeiten der \_ Nachrichten "WM Renderformat" und "WM \_ renderallformats"

Wenn ein Fenster ein **null** -Handle an die [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion übergibt, muss es die [**WM- \_ Renderformat**](wm-renderformat.md) -und [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachrichten verarbeiten, um Daten auf Anforderung zu Rendering.

Wenn ein Fenster das Rendern eines bestimmten Formats verzögert und dann eine andere Anwendung Daten in diesem Format anfordert, wird eine [**WM- \_ Renderformat**](wm-renderformat.md) -Meldung an das Fenster gesendet. Wenn ein Fenster außerdem das Rendern von einem oder mehreren Formaten verzögert und einige dieser Formate nicht gerendert bleiben, wenn das Fenster zerstört wird, wird eine WM- [**\_ renderallformats**](wm-renderallformats.md) -Nachricht vor deren Zerstörung an das Fenster gesendet.

Um ein Zwischenablage Format zu Renderen, sollte die Fenster Prozedur mithilfe der [**SetClipboardData**](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata) -Funktion ein Daten handle ungleich **null** in der Zwischenablage platzieren. Wenn die Fenster Prozedur ein Format in Reaktion auf die WM- [**\_ Renderformat**](wm-renderformat.md) -Nachricht rendert, darf die Zwischenablage vor dem Aufrufen von **SetClipboardData** nicht geöffnet werden. Wenn jedoch ein oder mehrere Formate als Antwort auf die [**WM- \_ renderallformats**](wm-renderallformats.md) -Nachricht gerendert werden, muss die Zwischenablage geöffnet werden, und es muss überprüft werden, ob das Fenster vor dem Aufrufen von **SetClipboardData** noch die Zwischenablage besitzt, und die Zwischenablage muss vor der Rückgabe geschlossen werden.

Die Label-Anwendung verarbeitet die [**WM- \_ Renderformat**](wm-renderformat.md) -und [**WM- \_ renderallformats**](wm-renderallformats.md) -Meldungen wie folgt.


```
case WM_RENDERFORMAT: 
    RenderFormat((UINT) wParam); 
    break; 
 
case WM_RENDERALLFORMATS:
    if (OpenClipboard(hwnd))
    {
        if (GetClipboardOwner() == hwnd)
        {
            RenderFormat(uLabelFormat);
            RenderFormat(CF_TEXT);
        }
        CloseClipboard();
    }
    break;
```



In beiden Fällen ruft die Fenster Prozedur die von der Anwendung definierte Renderformat-Funktion auf, die wie folgt definiert ist.

Die Struktur namens "LabelBox" ist wie folgt definiert.


```
#define BOX_ELLIPSE  0 
#define BOX_RECT     1 
 
#define CCH_MAXLABEL 80 
#define CX_MARGIN    12 
 
typedef struct tagLABELBOX {  // box 
    RECT rcText;    // coordinates of rectangle containing text 
    BOOL fSelected; // TRUE if the label is selected 
    BOOL fEdit;     // TRUE if text is selected 
    int nType;      // rectangular or elliptical 
    int ichCaret;   // caret position 
    int ichSel;     // with ichCaret, delimits selection 
    int nXCaret;    // window position corresponding to ichCaret 
    int nXSel;      // window position corresponding to ichSel 
    int cchLabel;   // length of text in atchLabel 
    TCHAR atchLabel[CCH_MAXLABEL]; 
} LABELBOX, *PLABELBOX;
```




```
void WINAPI RenderFormat(UINT uFormat) 
{ 
    HGLOBAL hglb; 
    PLABELBOX pbox; 
    LPTSTR  lptstr; 
    int cch; 
 
    if (pboxLocalClip == NULL) 
        return; 
 
    if (uFormat == CF_TEXT) 
    { 
        // Allocate a buffer for the text. 
 
        cch = pboxLocalClip->cchLabel; 
        hglb = GlobalAlloc(GMEM_MOVEABLE, 
            (cch + 1) * sizeof(TCHAR)); 
        if (hglb == NULL) 
            return; 
 
        // Copy the text from pboxLocalClip. 
 
        lptstr = GlobalLock(hglb); 
        memcpy(lptstr, pboxLocalClip->atchLabel, 
            cch * sizeof(TCHAR)); 
        lptstr[cch] = (TCHAR) 0; 
        GlobalUnlock(hglb); 
 
        // Place the handle on the clipboard. 
 
        SetClipboardData(CF_TEXT, hglb); 
    } 
    else if (uFormat == uLabelFormat) 
    { 
        hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(LABELBOX)); 
        if (hglb == NULL) 
            return; 
        pbox = GlobalLock(hglb); 
        memcpy(pbox, pboxLocalClip, sizeof(LABELBOX)); 
        GlobalUnlock(hglb); 
 
        SetClipboardData(uLabelFormat, hglb); 
    } 
}
```



### <a name="processing-the-wm_destroyclipboard-message"></a>Verarbeiten der WM \_ destroyclipboard-Nachricht

Die [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht kann von einem Fenster verarbeitet werden, um Ressourcen freizugeben, die für die Unterstützung des verzögerten Renderings reserviert wurden. Beispielsweise weist die Bezeichnung Anwendung beim Kopieren einer Bezeichnung in die Zwischenablage ein lokales Speicher Objekt zu. Anschließend wird dieses Objekt in Reaktion auf die **WM \_ destroyclipboard** -Nachricht wie folgt freigegeben.


```
case WM_DESTROYCLIPBOARD: 
    if (pboxLocalClip != NULL) 
    { 
        LocalFree(pboxLocalClip); 
        pboxLocalClip = NULL; 
    } 
    break;
```



### <a name="using-the-owner-display-clipboard-format"></a>Verwenden des Owner-Display-Zwischenablage Formats

Wenn ein Fenster Informationen in der Zwischenablage mithilfe des CF-in-Zwischenablage Formats **\_ anzeigt** , muss es folgende Aktionen ausführen:

-   Verarbeiten Sie die [**WM- \_ paintclipboard**](wm-paintclipboard.md) -Nachricht. Diese Nachricht wird an den Besitzer der Zwischenablage gesendet, wenn ein Teil des Zwischenablage-Viewer-Fensters neu gezeichnet werden muss.

-   Verarbeiten Sie die [**WM- \_ sizeclipboard**](wm-sizeclipboard.md) -Nachricht. Diese Nachricht wird an den Besitzer der Zwischenablage gesendet, wenn die Größe des Fensters der Zwischenablage Anzeige geändert wurde oder sich der Inhalt geändert hat.

    In der Regel antwortet ein Fenster auf diese Meldung, indem die scrollpositionen und-Bereiche für das Fenster der Zwischenablage Anzeige festgelegt werden. Als Antwort auf diese Nachricht aktualisiert die Bezeichnungs Anwendung auch eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur für das Fenster der Zwischenablage Anzeige.

-   Verarbeiten Sie die Nachrichten " [**WM \_ hscrollclipboard**](wm-hscrollclipboard.md) " und " [**WM \_ vscrollclipboard**](wm-vscrollclipboard.md) ". Diese Nachrichten werden an den Besitzer der Zwischenablage gesendet, wenn ein ScrollBar-Ereignis im Fenster der Zwischenablage Anzeige auftritt.

-   Verarbeiten Sie die [**WM- \_ askcbformatname**](wm-askcbformatname.md) -Nachricht. Das Fenster der Zwischenablage Anzeige sendet diese Nachricht an eine Anwendung, um den Namen des Besitzer Anzeige Formats abzurufen.

Die Fenster Prozedur für die Bezeichnungs Anwendung verarbeitet diese Nachrichten wie folgt.


```
LRESULT CALLBACK MainWindowProc(hwnd, msg, wParam, lParam) 
HWND hwnd; 
UINT msg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static RECT rcViewer; 
 
    RECT rc; 
    LPRECT lprc; 
    LPPAINTSTRUCT lpps; 
 
    switch (msg) 
    { 
        //
        // Handle other messages.
        //
        case WM_PAINTCLIPBOARD: 
            // Determine the dimensions of the label. 
 
            SetRect(&rc, 0, 0, 
                pboxLocalClip->rcText.right + CX_MARGIN, 
                pboxLocalClip->rcText.top * 2 + cyText 
            ); 
 
            // Center the image in the clipboard viewer window. 
 
            if (rc.right < rcViewer.right) 
            { 
                rc.left = (rcViewer.right - rc.right) / 2; 
                rc.right += rc.left; 
            } 
            if (rc.bottom < rcViewer.bottom) 
            { 
                rc.top = (rcViewer.bottom - rc.bottom) / 2; 
                rc.bottom += rc.top; 
            } 
 
            // Paint the image, using the specified PAINTSTRUCT 
            // structure, by calling the application-defined 
            // PaintLabel function. 
 
            lpps = (LPPAINTSTRUCT) GlobalLock((HGLOBAL) lParam); 
            PaintLabel(lpps, pboxLocalClip, &rc); 
            GlobalUnlock((HGLOBAL) lParam); 
            break; 
 
        case WM_SIZECLIPBOARD: 
            // Save the dimensions of the window in a static 
            // RECT structure. 
 
            lprc = (LPRECT) GlobalLock((HGLOBAL) lParam); 
            memcpy(&rcViewer, lprc, sizeof(RECT)); 
            GlobalUnlock((HGLOBAL) lParam); 
 
            // Set the scroll ranges to zero (thus eliminating 
            // the need to process the WM_HSCROLLCLIPBOARD and 
            // WM_VSCROLLCLIPBOARD messages). 
 
            SetScrollRange((HWND) wParam, SB_HORZ, 0, 0, TRUE); 
            SetScrollRange((HWND) wParam, SB_VERT, 0, 0, TRUE); 
 
            break; 
 
        case WM_ASKCBFORMATNAME: 
            LoadString(hinst, IDS_OWNERDISPLAY, 
                (LPSTR) lParam, wParam); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
}
```



## <a name="monitoring-clipboard-contents"></a>Überwachen der Zwischenablage

Es gibt drei Möglichkeiten, Änderungen in der Zwischenablage zu überwachen. Die älteste Methode ist die Erstellung eines Zwischenablage-Viewer-Fensters. Windows 2000 hat die Möglichkeit hinzugefügt, die Sequenznummer der Zwischenablage abzufragen, und Windows Vista hat Unterstützung für die slistenslistener Zwischenablage-Viewer-Fenster werden aus Gründen der Abwärtskompatibilität mit früheren Versionen von Windows unterstützt. In neuen Programmen sollten slistenslistener oder die Sequenznummer der Zwischenablage verwendet werden.

## <a name="querying-the-clipboard-sequence-number"></a>Abfragen der Zwischenablage-Sequenznummer

Bei jeder Änderung des Inhalts der Zwischenablage wird ein 32-Bit-Wert, der als Zwischenablage-Sequenznummer bezeichnet wird, inkrementiert. Ein Programm kann die aktuelle Zwischenablage Sequenznummer abrufen, indem die [**getclipboardsequencenenumber**](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber) -Funktion aufgerufen wird. Durch Vergleichen des Werts, der mit einem Wert zurückgegeben wird, der von einem vorherigen Befehl an **getclipboardsequencenumber** zurückgegeben wurde, kann ein Programm bestimmen, ob der Inhalt der Zwischenablage geändert wurde. Diese Methode eignet sich besser für Programme, die Ergebnisse basierend auf dem aktuellen Zwischenablage Inhalt zwischenspeichern und wissen müssen, ob die Berechnungen noch gültig sind, bevor die Ergebnisse aus diesem Cache verwendet werden. Beachten Sie, dass dies keine Benachrichtigungs Methode ist und nicht in einer Abruf Schleife verwendet werden sollte. Wenn Sie benachrichtigt werden möchten, wenn sich der Inhalt der Zwischenablage ändert, verwenden Sie einen Zwischenablage-formatlistener oder einen

## <a name="creating-a-clipboard-format-listener"></a>Erstellen eines-Zwischenablage-formatlistener

Ein Zwischenablage-formatlistener ist ein Fenster, das registriert wurde, um benachrichtigt zu werden, wenn sich der Inhalt der Zwischenablage geändert hat. Diese Methode wird bei der Erstellung eines Zwischenablage-Viewer-Fensters empfohlen, da es einfacher ist, Probleme zu implementieren und zu vermeiden, wenn Programme die Zwischenablage-Viewer-Kette nicht ordnungsgemäß beibehalten können oder wenn ein Fenster in der Zwischenablage-Viewer-Kette nicht mehr auf

Ein Fenster wird als Listener im Zwischenablage Format durch Aufrufen der [**addclipboardformatlistener**](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener) -Funktion registriert. Wenn sich der Inhalt der Zwischenablage ändert, wird dem Fenster eine [**WM- \_ clipboardupdate**](wm-clipboardupdate.md) -Nachricht gesendet. Die Registrierung bleibt gültig, bis die Registrierung des Fensters durch Aufrufen der [**removeclipboardformatlistener**](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener) -Funktion aufgehoben wird.

## <a name="creating-a-clipboard-viewer-window"></a>Erstellen eines Zwischenablage-Viewer-Fensters

Ein Fenster der Zwischenablage Anzeige zeigt den aktuellen Inhalt der Zwischenablage an und empfängt Nachrichten, wenn der Inhalt der Zwischenablage geändert wird. Um ein Fenster für die Zwischenablage Anzeige zu erstellen, muss Ihre Anwendung folgende Aktionen ausführen:

-   Fügen Sie das Fenster der Zwischenablage-Viewer-Kette hinzu.
-   Verarbeiten Sie die Meldung " [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) ".
-   Die [**WM- \_ drawclipboard**](wm-drawclipboard.md) -Nachricht verarbeiten.
-   Entfernen Sie das Fenster aus der Zwischenablage-Viewer-Kette, bevor es zerstört wird.

## <a name="adding-a-window-to-the-clipboard-viewer-chain"></a>Hinzufügen eines Fensters zur Zwischenablage-Viewer-Kette

Durch Aufrufen der [**setclipboardviewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) -Funktion wird ein Fenster zur Kette der Zwischenablage-Viewer hinzugefügt. Der Rückgabewert ist das Handle für das nächste Fenster in der Kette. Ein Fenster muss diesen Wert nachverfolgen können, z. –. durch Speichern in einer statischen Variablen namens *hwndnextviewer*.

Im folgenden Beispiel wird der Kette der Zwischenablage-Viewer als Reaktion auf die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung ein Fenster hinzugefügt.


```
case WM_CREATE: 
 
    // Add the window to the clipboard viewer chain. 
 
    hwndNextViewer = SetClipboardViewer(hwnd); 
    break;
```



Code Ausschnitte werden für die folgenden Aufgaben angezeigt:

-   [Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht](/windows)
-   [Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette](#removing-a-window-from-the-clipboard-viewer-chain)
-   [Die WM- \_ drawclipboard-Nachricht wird verarbeitet.](/windows)
-   [Beispiel für einen Zwischenablage-Viewer](#example-of-a-clipboard-viewer)

### <a name="processing-the-wm_changecbchain-message"></a>Verarbeiten der WM- \_ CHANGECBCHAIN-Nachricht

Ein Fenster der Zwischenablage Anzeige empfängt die [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht, wenn sich ein anderes Fenster selbst aus der Zwischenablage-Viewer-Kette entfernt. Wenn das zu entfernende Fenster das nächste Fenster in der Kette ist, muss das Fenster, in dem die Meldung empfangen wird, die Verknüpfung des nächsten Fensters von der Kette aufheben. Andernfalls sollte diese Nachricht an das nächste Fenster in der Kette weitergeleitet werden.

Das folgende Beispiel zeigt die Verarbeitung der [**WM- \_ CHANGECBCHAIN**](wm-changecbchain.md) -Nachricht.


```
case WM_CHANGECBCHAIN: 
 
    // If the next window is closing, repair the chain. 
 
    if ((HWND) wParam == hwndNextViewer) 
        hwndNextViewer = (HWND) lParam; 
 
    // Otherwise, pass the message to the next link. 
 
    else if (hwndNextViewer != NULL) 
        SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
    break;
```



### <a name="removing-a-window-from-the-clipboard-viewer-chain"></a>Entfernen eines Fensters aus der Zwischenablage-Viewer-Kette

Um sich selbst aus der Zwischenablage-Viewer-Kette zu entfernen, Ruft ein Fenster die [**changeclipboardchain**](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain) -Funktion auf. Im folgenden Beispiel wird ein Fenster aus der Kette der Zwischenablage-Viewer als Antwort auf die WM-Lösch Nachricht entfernt. [**\_**](/windows/desktop/winmsg/wm-destroy)


```
case WM_DESTROY: 
    ChangeClipboardChain(hwnd, hwndNextViewer); 
    PostQuitMessage(0); 
    break;
```



### <a name="processing-the-wm_drawclipboard-message"></a>Die WM- \_ drawclipboard-Nachricht wird verarbeitet.

Die " [**WM \_ drawclipboard**](wm-drawclipboard.md) "-Meldung benachrichtigt das Fenster der Zwischenablage-Viewer, dass sich der Inhalt der Zwischenablage geändert hat. Bei der Verarbeitung der **WM- \_ drawclipboard** -Nachricht sollte ein Fenster folgende Aktionen ausführen:

1.  Bestimmen Sie, welches der verfügbaren Zwischenablage Formate angezeigt werden soll.
2.  Rufen Sie die Zwischenablage Daten ab, und zeigen Sie Sie im Fenster an. Oder wenn das Zwischenablage Format **CF \_**-Besitzer Anzeige ist, senden Sie eine " [**WM \_ paintclipboard**](wm-paintclipboard.md) "-Meldung an den Besitzer der Zwischenablage.
3.  Sendet die Nachricht an das nächste Fenster in der Kette der Zwischenablage-Viewer.

Ein Beispiel für die Verarbeitung der " [**WM \_ drawclipboard**](wm-drawclipboard.md) "-Nachricht finden Sie in der Beispiel Auflistung im [Beispiel eines Zwischenablage-Viewers](#example-of-a-clipboard-viewer).

### <a name="example-of-a-clipboard-viewer"></a>Beispiel für einen Zwischenablage-Viewer

Das folgende Beispiel zeigt eine einfache Anwendung der Zwischenablage Anzeige.


```
HINSTANCE hinst; 
UINT uFormat = (UINT)(-1); 
BOOL fAuto = TRUE; 
 
LRESULT APIENTRY MainWndProc(hwnd, uMsg, wParam, lParam) 
HWND hwnd; 
UINT uMsg; 
WPARAM wParam; 
LPARAM lParam; 
{ 
    static HWND hwndNextViewer; 
 
    HDC hdc; 
    HDC hdcMem; 
    PAINTSTRUCT ps; 
    LPPAINTSTRUCT lpps; 
    RECT rc; 
    LPRECT lprc; 
    HGLOBAL hglb; 
    LPSTR lpstr; 
    HBITMAP hbm; 
    HENHMETAFILE hemf; 
    HWND hwndOwner; 
 
    switch (uMsg) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
 
            // Branch depending on the clipboard format. 
 
            switch (uFormat) 
            { 
                case CF_OWNERDISPLAY: 
                    hwndOwner = GetClipboardOwner(); 
                    hglb = GlobalAlloc(GMEM_MOVEABLE, 
                        sizeof(PAINTSTRUCT)); 
                    lpps = GlobalLock(hglb);
                    memcpy(lpps, &ps, sizeof(PAINTSTRUCT)); 
                    GlobalUnlock(hglb); 
 
                    SendMessage(hwndOwner, WM_PAINTCLIPBOARD, 
                        (WPARAM) hwnd, (LPARAM) hglb); 
 
                    GlobalFree(hglb); 
                    break; 
 
                case CF_BITMAP: 
                    hdcMem = CreateCompatibleDC(hdc); 
                    if (hdcMem != NULL) 
                    { 
                        if (OpenClipboard(hwnd)) 
                        { 
                            hbm = (HBITMAP) 
                                GetClipboardData(uFormat); 
                            SelectObject(hdcMem, hbm); 
                            GetClientRect(hwnd, &rc); 
 
                            BitBlt(hdc, 0, 0, rc.right, rc.bottom, 
                                hdcMem, 0, 0, SRCCOPY); 
                            CloseClipboard(); 
                        } 
                        DeleteDC(hdcMem); 
                    } 
                    break; 
 
                case CF_TEXT: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hglb = GetClipboardData(uFormat); 
                        lpstr = GlobalLock(hglb); 
 
                        GetClientRect(hwnd, &rc); 
                        DrawText(hdc, lpstr, -1, &rc, DT_LEFT); 
 
                        GlobalUnlock(hglb); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case CF_ENHMETAFILE: 
                    if (OpenClipboard(hwnd)) 
                    { 
                        hemf = GetClipboardData(uFormat); 
                        GetClientRect(hwnd, &rc); 
                        PlayEnhMetaFile(hdc, hemf, &rc); 
                        CloseClipboard(); 
                    } 
                    break; 
 
                case 0: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "The clipboard is empty.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
                    break; 
 
                default: 
                    GetClientRect(hwnd, &rc); 
                    DrawText(hdc, "Unable to display format.", -1, 
                        &rc, DT_CENTER | DT_SINGLELINE | 
                        DT_VCENTER); 
            } 
            EndPaint(hwnd, &ps); 
            break; 
 
        case WM_SIZE: 
            if (uFormat == CF_OWNERDISPLAY) 
            { 
                hwndOwner = GetClipboardOwner(); 
                hglb = GlobalAlloc(GMEM_MOVEABLE, sizeof(RECT)); 
                lprc = GlobalLock(hglb); 
                GetClientRect(hwnd, lprc); 
                GlobalUnlock(hglb); 
 
                SendMessage(hwndOwner, WM_SIZECLIPBOARD, 
                    (WPARAM) hwnd, (LPARAM) hglb); 
 
                GlobalFree(hglb); 
            } 
            break; 
 
        case WM_CREATE: 
 
            // Add the window to the clipboard viewer chain. 
 
            hwndNextViewer = SetClipboardViewer(hwnd); 
            break; 
 
        case WM_CHANGECBCHAIN: 
 
            // If the next window is closing, repair the chain. 
 
            if ((HWND) wParam == hwndNextViewer) 
                hwndNextViewer = (HWND) lParam; 
 
            // Otherwise, pass the message to the next link. 
 
            else if (hwndNextViewer != NULL) 
                SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
 
            break; 
 
        case WM_DESTROY: 
            ChangeClipboardChain(hwnd, hwndNextViewer); 
            PostQuitMessage(0); 
            break; 
 
        case WM_DRAWCLIPBOARD:  // clipboard contents changed. 
 
            // Update the window by using Auto clipboard format. 
 
            SetAutoView(hwnd); 
 
            // Pass the message to the next window in clipboard 
            // viewer chain. 
 
            SendMessage(hwndNextViewer, uMsg, wParam, lParam); 
            break; 
 
        case WM_INITMENUPOPUP: 
            if (!HIWORD(lParam)) 
                InitMenu(hwnd, (HMENU) wParam); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_EXIT: 
                    DestroyWindow(hwnd); 
                    break; 
 
                case IDM_AUTO: 
                    SetAutoView(hwnd); 
                    break; 
 
                default: 
                    fAuto = FALSE; 
                    uFormat = LOWORD(wParam); 
                    InvalidateRect(hwnd, NULL, TRUE); 
            } 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return (LRESULT) NULL; 
} 
 
void WINAPI SetAutoView(HWND hwnd) 
{ 
    static UINT auPriorityList[] = { 
        CF_OWNERDISPLAY, 
        CF_TEXT, 
        CF_ENHMETAFILE, 
        CF_BITMAP 
    }; 
 
    uFormat = GetPriorityClipboardFormat(auPriorityList, 4); 
    fAuto = TRUE; 
 
    InvalidateRect(hwnd, NULL, TRUE); 
    UpdateWindow(hwnd); 
} 
 
void WINAPI InitMenu(HWND hwnd, HMENU hmenu) 
{ 
    UINT uFormat; 
    char szFormatName[80]; 
    LPCSTR lpFormatName; 
    UINT fuFlags; 
    UINT idMenuItem; 
 
    // If a menu is not the display menu, no initialization is necessary. 
 
    if (GetMenuItemID(hmenu, 0) != IDM_AUTO) 
        return; 
 
    // Delete all menu items except the first. 
 
    while (GetMenuItemCount(hmenu) > 1) 
        DeleteMenu(hmenu, 1, MF_BYPOSITION); 
 
    // Check or uncheck the Auto menu item. 
 
    fuFlags = fAuto ? MF_BYCOMMAND | MF_CHECKED : 
        MF_BYCOMMAND | MF_UNCHECKED; 
    CheckMenuItem(hmenu, IDM_AUTO, fuFlags); 
 
    // If there are no clipboard formats, return. 
 
    if (CountClipboardFormats() == 0) 
        return; 
 
    // Open the clipboard. 
 
    if (!OpenClipboard(hwnd)) 
        return; 
 
    // Add a separator and then a menu item for each format. 
 
    AppendMenu(hmenu, MF_SEPARATOR, 0, NULL); 
    uFormat = EnumClipboardFormats(0); 
 
    while (uFormat) 
    { 
        // Call an application-defined function to get the name 
        // of the clipboard format. 
 
        lpFormatName = GetPredefinedClipboardFormatName(uFormat); 
 
        // For registered formats, get the registered name. 
 
        if (lpFormatName == NULL) 
        {

        // Note that, if the format name is larger than the
        // buffer, it is truncated. 
            if (GetClipboardFormatName(uFormat, szFormatName, 
                    sizeof(szFormatName))) 
                lpFormatName = szFormatName; 
            else 
                lpFormatName = "(unknown)"; 
        } 
 
        // Add a menu item for the format. For displayable 
        // formats, use the format ID for the menu ID. 
 
        if (IsDisplayableFormat(uFormat)) 
        { 
            fuFlags = MF_STRING; 
            idMenuItem = uFormat; 
        } 
        else 
        { 
            fuFlags = MF_STRING | MF_GRAYED; 
            idMenuItem = 0; 
        } 
        AppendMenu(hmenu, fuFlags, idMenuItem, lpFormatName); 
 
        uFormat = EnumClipboardFormats(uFormat); 
    } 
    CloseClipboard(); 
 
} 
 
BOOL WINAPI IsDisplayableFormat(UINT uFormat) 
{ 
    switch (uFormat) 
    { 
        case CF_OWNERDISPLAY: 
        case CF_TEXT: 
        case CF_ENHMETAFILE: 
        case CF_BITMAP: 
            return TRUE; 
    } 
    return FALSE; 
} 
```



 

 