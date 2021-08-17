---
title: Erstellen eines Monatskalender-Steuerelements
description: In diesem Thema wird veranschaulicht, wie ein Monatskalender-Steuerelement mithilfe der CreateWindowEx-Funktion dynamisch erstellt wird.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f0fbc819a79b05842db75c1871e8150b311444e6055d076a9831b0bc42486b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831816"
---
# <a name="how-to-create-a-month-calendar-control"></a>Erstellen eines Monatskalender-Steuerelements

In diesem Thema wird veranschaulicht, wie ein Monatskalender-Steuerelement mithilfe der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) dynamisch erstellt wird.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Verwenden Sie zum Erstellen eines Monatskalender-Steuerelements die [**CreateWindowEx-Funktion,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben Sie [**MONTHCAL \_ CLASS**](common-control-window-classes.md) als Fensterklasse an. Sie müssen zuerst die Fensterklasse registrieren, indem Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen und dabei das **BIT "DATE \_ \_ CLASSES"** in der zugehörigen [**INITCOMMONCONTROLSEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) angeben.

Im folgenden Beispiel wird veranschaulicht, wie sie ein Monatskalender-Steuerelement in einem vorhandenen moduslosen Dialogfeld erstellen. Beachten Sie, dass die an [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) übergebenen Größenwerte alle Nullen sind. Da die erforderliche Mindestgröße von der Schriftart abhängt, die das Steuerelement verwendet, wird im Beispiel das [**MonthCal \_ GetMinReqRect-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) verwendet, um Größeninformationen anzufordern, und anschließend wird die Größe des Steuerelements durch Aufrufen von [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)geändert. Wenn Sie anschließend die Schriftart mit [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont)ändern, ändern sich die Abmessungen des Steuerelements nicht. Sie müssen **MonthCal \_ GetMinReqRect** erneut aufrufen und die Größe des Steuerelements an die neue Schriftart anpassen.



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

[Monatskalender-Steuerelementreferenz](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informationen zu Monatskalender-Steuerelementen](month-calendar-controls.md)
</dt> <dt>

[Verwenden von Monatskalender-Steuerelementen](using-month-calendar-controls.md)
</dt> </dl>

 

 