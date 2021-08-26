---
title: Erstellen eines Dialogfelds im Registerkartenfenster
description: Im Beispiel in diesem Abschnitt wird veranschaulicht, wie ein Dialogfeld erstellt wird, das Registerkarten verwendet, um mehrere Seiten von Steuerelementen zur Verfügung zu stellen.
ms.assetid: DBF7FBDF-AADC-45CE-833E-F893C1129FC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa2ad8ba22c2972c6bdd502728af413d4800dabf0ab5c9196a4033a52267115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920710"
---
# <a name="how-to-create-a-tabbed-dialog-box"></a>Erstellen eines Dialogfelds im Registerkartenfenster

Im Beispiel in diesem Abschnitt wird veranschaulicht, wie ein Dialogfeld erstellt wird, das Registerkarten verwendet, um mehrere Seiten von Steuerelementen zur Verfügung zu stellen. Das Hauptdialogfeld ist ein modales Dialogfeld. Jede Seite von Steuerelementen wird durch eine Dialogfeldvorlage definiert, die über den [**WS \_ CHILD-Stil**](/windows/desktop/winmsg/window-styles) verfügt. Wenn eine Registerkarte ausgewählt ist, wird ein nicht modusloses Dialogfeld für die eingehende Seite erstellt, und das Dialogfeld für die ausgehende Seite wird zerstört.

> [!Note]  
> In vielen Fällen können Sie Dialogfelder mit mehreren Seiten einfacher implementieren, indem Sie Eigenschaftenblätter verwenden. Weitere Informationen zu Eigenschaftenblättern finden Sie unter [Informationen zu Eigenschaftenblättern.](property-sheets.md)

 

Die Vorlage für das Hauptdialogfeld definiert einfach zwei Schaltflächen-Steuerelemente. Beim Verarbeiten der [**WM \_ INITDIALOG-Meldung**](/windows/desktop/dlgbox/wm-initdialog) erstellt die Dialogfeldprozedur ein Registerkarten-Steuerelement und lädt die Vorlagenressourcen des Dialogfelds für jedes untergeordnete Dialogfeld.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="create-a-tabbed-dialog-box"></a>Dialogfeld "Erstellen eines Registerkarten"-Dialogfelds

Die Informationen werden in einer anwendungsdefinierten Struktur namens DLGHDR gespeichert. Ein Zeiger auf diese Struktur wird dem Dialogfeldfenster mithilfe der [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) zugeordnet. Die -Struktur wird wie folgt in der Headerdatei der Anwendung definiert.


```C++
#define C_PAGES 3 

typedef struct tag_dlghdr { 
    HWND hwndTab;       // tab control 
    HWND hwndDisplay;   // current child dialog box 
    RECT rcDisplay;     // display rectangle for the tab control 
    DLGTEMPLATEEX *apRes[C_PAGES]; 
} DLGHDR; 
```



Die folgende Funktion verarbeitet die [**WM \_ INITDIALOG-Meldung**](/windows/desktop/dlgbox/wm-initdialog) für das Hauptdialogfeld. Die Funktion ordnet die Struktur zu, lädt die Vorlagenressourcen des Dialogfelds für die untergeordneten Dialogfelder `DLGHDR` und erstellt das Registerkarten-Steuerelement.

Die Größe der einzelnen untergeordneten Dialogfelder wird von der [**DLGTEMPLATEEX-Struktur**](/windows/desktop/dlgbox/dlgtemplateex) angegeben. Die Funktion untersucht die Größe der einzelnen Dialogfelder und verwendet das Makro für die [**\_ TCM-Nachricht ADJUSTRECT,**](tcm-adjustrect.md) um eine geeignete Größe für das Registerkartensteuerfeld zu berechnen. Anschließend wird die Größe des Dialogfelds angepasst, und die beiden Schaltflächen werden entsprechend positioniert. In diesem Beispiel wird **TCM \_ ADJUSTRECT mithilfe** des [**TabCtrl-Makros \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) sendet.


```C++
// Handles the WM_INITDIALOG message for a dialog box that contains 
//   a tab control used to select among three child dialog boxes.
// Returns a result code.
// hwndDlg - handle of the dialog box.
// 
HRESULT OnTabbedDialogInit(HWND hwndDlg) 
{ 
    INITCOMMONCONTROLSEX iccex;
    DWORD dwDlgBase = GetDialogBaseUnits();
    int cxMargin = LOWORD(dwDlgBase) / 4; 
    int cyMargin = HIWORD(dwDlgBase) / 8; 

    TCITEM tie; 
    RECT rcTab; 
    HWND hwndButton; 
    RECT rcButton; 
    int i; 

    // Initialize common controls.
    iccex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    iccex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&iccex); 

    // Allocate memory for the DLGHDR structure. Remember to 
    // free this memory before the dialog box is destroyed.
    DLGHDR *pHdr = (DLGHDR *) LocalAlloc(LPTR, sizeof(DLGHDR)); 

    // Save a pointer to the DLGHDR structure in the window
    // data of the dialog box. 
    SetWindowLongPtr(hwndDlg, GWLP_USERDATA, (LONG_PTR) pHdr); 
 
    // Create the tab control. Note that g_hInst is a global 
    // instance handle. 
    pHdr->hwndTab = CreateWindow( 
        WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, 100, 100, 
        hwndDlg, NULL, g_hInst, NULL 
        ); 
    if (pHdr->hwndTab == NULL) 
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }
 
    // Add a tab for each of the three child dialog boxes. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = L"First"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 0, &tie); 
    tie.pszText = L"Second"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 1, &tie); 
    tie.pszText = L"Third"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 2, &tie); 

    // Lock the resources for the three child dialog boxes. 
    pHdr->apRes[0] = DoLockDlgRes(MAKEINTRESOURCE(IDD_FIRSTDLG)); 
    pHdr->apRes[1] = DoLockDlgRes(MAKEINTRESOURCE(IDD_SECONDDLG)); 
    pHdr->apRes[2] = DoLockDlgRes(MAKEINTRESOURCE(IDD_THIRDDLG)); 

    // Determine a bounding rectangle that is large enough to 
    // contain the largest child dialog box. 
    SetRectEmpty(&rcTab); 
    for (i = 0; i < C_PAGES; i++) 
    { 
        if (pHdr->apRes[i]->cx > rcTab.right) 
            rcTab.right = pHdr->apRes[i]->cx; 
        if (pHdr->apRes[i]->cy > rcTab.bottom) 
            rcTab.bottom = pHdr->apRes[i]->cy; 
    }

    // Map the rectangle from dialog box units to pixels.
    MapDialogRect(hwndDlg, &rcTab);
    
    // Calculate how large to make the tab control, so 
    // the display area can accommodate all the child dialog boxes. 
    TabCtrl_AdjustRect(pHdr->hwndTab, TRUE, &rcTab); 
    OffsetRect(&rcTab, cxMargin - rcTab.left, cyMargin - rcTab.top); 
 
    // Calculate the display rectangle. 
    CopyRect(&pHdr->rcDisplay, &rcTab); 
    TabCtrl_AdjustRect(pHdr->hwndTab, FALSE, &pHdr->rcDisplay); 
 
    // Set the size and position of the tab control, buttons, 
    // and dialog box. 
    SetWindowPos(pHdr->hwndTab, NULL, rcTab.left, rcTab.top, 
            rcTab.right - rcTab.left, rcTab.bottom - rcTab.top, 
            SWP_NOZORDER); 
 
    // Move the first button below the tab control. 
    hwndButton = GetDlgItem(hwndDlg, IDB_CLOSE); 
    SetWindowPos(hwndButton, NULL, 
            rcTab.left, rcTab.bottom + cyMargin, 0, 0, 
            SWP_NOSIZE | SWP_NOZORDER); 
 
    // Determine the size of the button. 
    GetWindowRect(hwndButton, &rcButton); 
    rcButton.right -= rcButton.left; 
    rcButton.bottom -= rcButton.top; 
 
    // Move the second button to the right of the first. 
    hwndButton = GetDlgItem(hwndDlg, IDB_TEST); 
    SetWindowPos(hwndButton, NULL, 
        rcTab.left + rcButton.right + cxMargin, 
        rcTab.bottom + cyMargin, 0, 0, 
        SWP_NOSIZE | SWP_NOZORDER); 
 
    // Size the dialog box. 
    SetWindowPos(hwndDlg, NULL, 0, 0, 
        rcTab.right + cyMargin + (2 * GetSystemMetrics(SM_CXDLGFRAME)), 
        rcTab.bottom + rcButton.bottom + (2 * cyMargin)
        + (2 * GetSystemMetrics(SM_CYDLGFRAME)) 
        + GetSystemMetrics(SM_CYCAPTION), 
        SWP_NOMOVE | SWP_NOZORDER); 
 
    // Simulate selection of the first item. 
    OnSelChanged(hwndDlg); 

    return S_OK;
} 

// Loads and locks a dialog box template resource. 
// Returns the address of the locked dialog box template resource. 
// lpszResName - name of the resource. 
//
DLGTEMPLATEEX* DoLockDlgRes(LPCTSTR lpszResName) 
{ 
    HRSRC hrsrc = FindResource(NULL, lpszResName, RT_DIALOG); 

    // Note that g_hInst is the global instance handle
    HGLOBAL hglb = LoadResource(g_hInst, hrsrc);  
    return (DLGTEMPLATEEX *) LockResource(hglb); 
} 
```



Die folgende Funktion verarbeitet den [TCN \_ SELCHANGE-Benachrichtigungscode](tcn-selchange.md) für das Hauptdialogfeld. Die -Funktion zerstört das Dialogfeld für die ausgehende Seite, falls dies der Fall ist. Anschließend wird die [**CreateDialogIndirect-Funktion**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) verwendet, um ein modusloses Dialogfeld für die eingehende Seite zu erstellen.


```C++
// Processes the TCN_SELCHANGE notification. 
// hwndDlg - handle to the parent dialog box. 
//
VOID OnSelChanged(HWND hwndDlg) 
{ 
    // Get the dialog header data.
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndDlg, GWLP_USERDATA); 

    // Get the index of the selected tab.
    int iSel = TabCtrl_GetCurSel(pHdr->hwndTab); 
 
    // Destroy the current child dialog box, if any. 
    if (pHdr->hwndDisplay != NULL) 
        DestroyWindow(pHdr->hwndDisplay); 
 
    // Create the new child dialog box. Note that g_hInst is the
    // global instance handle.
    pHdr->hwndDisplay = CreateDialogIndirect(g_hInst, 
        (DLGTEMPLATE *)pHdr->apRes[iSel], hwndDlg, ChildDialogProc); 

    return;
} 
```



Die folgende Funktion verarbeitet die [**WM \_ INITDIALOG-Nachricht**](/windows/desktop/dlgbox/wm-initdialog) für jedes der untergeordneten Dialogfelder. Sie können die Position eines Dialogfelds, das mit der [**CreateDialogIndirect-Funktion**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) erstellt wird, nicht angeben. Diese Funktion verwendet die [**SetWindowPos-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) um den untergeordneten Dialog im Anzeigebereich des Registerkartensteuerfelds zu positionieren.


```C++
// Positions the child dialog box to occupy the display area of the 
//   tab control. 
// hwndDlg - handle of the dialog box.
//
VOID WINAPI OnChildDialogInit(HWND hwndDlg) 
{ 
    HWND hwndParent = GetParent(hwndDlg);
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndParent, GWLP_USERDATA); 
    SetWindowPos(hwndDlg, NULL, pHdr->rcDisplay.left,
        pHdr->rcDisplay.top,//-2,
        (pHdr->rcDisplay.right - pHdr->rcDisplay.left),
        (pHdr->rcDisplay.bottom - pHdr->rcDisplay.top),
        SWP_SHOWWINDOW);
        
    return;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Registerkartensteuerelementen](using-tab-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 