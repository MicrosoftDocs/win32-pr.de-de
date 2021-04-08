---
title: Erstellen von Grund leisten-Steuerelementen
description: Eine Anwendung erstellt durch Aufrufen der CreateWindowEx-Funktion ein Grund leisten-Steuerelement, wobei rebarclassname als Fenster Klasse angegeben wird.
ms.assetid: F17CC2A4-BDC6-48A6-9AF5-19FCF65CC39A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b38cd49e8e6016dafad5ec07c77be570a5a430
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730441"
---
# <a name="how-to-create-rebar-controls"></a>Erstellen von Grund leisten-Steuerelementen

Eine Anwendung erstellt durch Aufrufen der [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion ein Grund leisten-Steuerelement, wobei [**rebarclassname**](common-control-window-classes.md) als Fenster Klasse angegeben wird. Die Anwendung muss zuerst die Fenster Klasse registrieren, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und \_ dabei den Wert für das cool-Klassen- \_ Bit in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angibt.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-rebar-control"></a>Erstellen eines Grund leisten-Steuer Elements

Im folgenden Beispiel wird ein Grund leisten-Steuerelement mit zwei Bändern erstellt – eines mit einem Kombinations Feld und ein weiteres, das eine Symbolleiste enthält. (Weitere Informationen finden Sie in der Abbildung unter [Informationen zu](rebar-controls.md)Grund leisten-Steuerelementen Diese Steuerelemente werden separat erstellt und als Parameter an die Beispiel Funktion übermittelt.


```C++
#define NUMBUTTONS 3

HWND CreateRebar(HWND hwndOwner, HWND hwndToolbar, HWND hwndCombo)
{
    // Check parameters.
    if ((hwndToolbar == NULL) || (hwndCombo == NULL))
    {
        return NULL;
    }

    // Initialize common controls.
    INITCOMMONCONTROLSEX icex;
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC   = ICC_COOL_CLASSES | ICC_BAR_CLASSES;
    InitCommonControlsEx(&icex);

    // Create the rebar.
    HWND hwndRebar = CreateWindowEx(WS_EX_TOOLWINDOW,
        REBARCLASSNAME,
        NULL,
        WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS |
        WS_CLIPCHILDREN | RBS_VARHEIGHT |
        CCS_NODIVIDER | RBS_BANDBORDERS,
        0,0,0,0,
        hwndOwner,
        NULL,
        g_hInst, // global instance handle
        NULL);

    if(!hwndRebar)
    {
        return NULL;
    }

    // Initialize band info used by both bands.
    REBARBANDINFO rbBand = { sizeof(REBARBANDINFO) };
    rbBand.fMask  = 
          RBBIM_STYLE       // fStyle is valid.
        | RBBIM_TEXT        // lpText is valid.
        | RBBIM_CHILD       // hwndChild is valid.
        | RBBIM_CHILDSIZE   // child size members are valid.
        | RBBIM_SIZE;       // cx is valid
    rbBand.fStyle = RBBS_CHILDEDGE | RBBS_GRIPPERALWAYS;  

    // Get the height of the toolbar.
    DWORD dwBtnSize = (DWORD)SendMessage(hwndToolbar, TB_GETBUTTONSIZE, 0,0);

    // Set values unique to the band with the toolbar.
    rbBand.lpText = TEXT("");
    rbBand.hwndChild = hwndToolbar;
    rbBand.cyChild = LOWORD(dwBtnSize);
    rbBand.cxMinChild = NUMBUTTONS * HIWORD(dwBtnSize);
    rbBand.cyMinChild = LOWORD(dwBtnSize);
    // The default width is the width of the buttons.
    rbBand.cx = 0;

    // Add the band that has the toolbar.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);

    // Set values unique to the band with the combo box.
    RECT rc;
    GetWindowRect(hwndCombo, &rc);
    rbBand.lpText = TEXT("Font");
    rbBand.hwndChild = hwndCombo;
    rbBand.cxMinChild = 0;
    rbBand.cyMinChild = rc.bottom - rc.top;
    // The default width should be set to some value wider than the text. The combo 
    // box itself will expand to fill the band.
    rbBand.cx = 100;

    // Add the band that has the combo box.
    SendMessage(hwndRebar, RB_INSERTBAND, (WPARAM)-1, (LPARAM)&rbBand);
    
    return (hwndRebar);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Grund leisten-Steuerelementen](using-rebar-controls.md)
</dt> <dt>

[Informationen über Grund leisten-Steuerelemente](rebar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 