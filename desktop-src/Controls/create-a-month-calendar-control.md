---
title: Erstellen eines Monatskalender-Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein Monatskalender-Steuerelement mithilfe der Funktion "die Funktion" "" "erstellt wird.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734913"
---
# <a name="how-to-create-a-month-calendar-control"></a>Erstellen eines Monatskalender-Steuer Elements

In diesem Thema wird veranschaulicht, wie ein Monatskalender-Steuerelement mithilfe [**der Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) "die Funktion" "" "erstellt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Um ein Monatskalender-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", wobei die [**monthcal- \_ Klasse**](common-control-window-classes.md) als Fenster Klasse angegeben wird. Sie müssen zuerst die Fenster Klasse registrieren, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und dabei das Bit der **ICC- \_ Datums \_ Klassen** in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angeben.

Im folgenden Beispiel wird veranschaulicht, wie ein Monatskalender-Steuerelement in einem vorhandenen nicht modalem Dialogfeld erstellt wird. Beachten Sie, dass die an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " über gebenden Größen Werte alle Nullen sind. Da die erforderliche Mindestgröße von der Schriftart abhängig ist, die das Steuerelement verwendet, verwendet das Beispiel das [**monthcal \_ getminreqrect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) -Makro, um Größen Informationen anzufordern, und ändert anschließend die Größe des Steuer Elements, indem [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)aufgerufen werden. Wenn Sie anschließend die Schriftart mit [**WM \_ setFont**](/windows/desktop/winmsg/wm-setfont)ändern, werden die Abmessungen des Steuer Elements nicht geändert. Sie müssen **monthcal \_ getminreqrect** erneut aufrufen und die Größe des Steuer Elements an die neue Schriftart anpassen.



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verweis für Monatskalender-Steuerelement](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informationen zu Monatskalender-Steuerelementen](month-calendar-controls.md)
</dt> <dt>

[Verwenden von Monatskalender-Steuerelementen](using-month-calendar-controls.md)
</dt> </dl>

 

 