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
# <a name="how-to-create-a-month-calendar-control"></a><span data-ttu-id="94f74-103">Erstellen eines Monatskalender-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="94f74-103">How to Create a Month Calendar Control</span></span>

<span data-ttu-id="94f74-104">In diesem Thema wird veranschaulicht, wie ein Monatskalender-Steuerelement mithilfe [**der Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) "die Funktion" "" "erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="94f74-104">This topic demonstrates how to dynamically create a month calendar control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="94f74-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="94f74-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="94f74-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="94f74-106">Technologies</span></span>

-   [<span data-ttu-id="94f74-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="94f74-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="94f74-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="94f74-108">Prerequisites</span></span>

-   <span data-ttu-id="94f74-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="94f74-109">C/C++</span></span>
-   <span data-ttu-id="94f74-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="94f74-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="94f74-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="94f74-111">Instructions</span></span>


<span data-ttu-id="94f74-112">Um ein Monatskalender-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", wobei die [**monthcal- \_ Klasse**](common-control-window-classes.md) als Fenster Klasse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="94f74-112">To create a month calendar control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**MONTHCAL\_CLASS**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="94f74-113">Sie müssen zuerst die Fenster Klasse registrieren, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und dabei das Bit der **ICC- \_ Datums \_ Klassen** in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="94f74-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the **ICC\_DATE\_CLASSES** bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="94f74-114">Im folgenden Beispiel wird veranschaulicht, wie ein Monatskalender-Steuerelement in einem vorhandenen nicht modalem Dialogfeld erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="94f74-114">The following example demonstrates how to create a month calendar control in an existing modeless dialog box.</span></span> <span data-ttu-id="94f74-115">Beachten Sie, dass die an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " über gebenden Größen Werte alle Nullen sind.</span><span class="sxs-lookup"><span data-stu-id="94f74-115">Note that the size values passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) are all zeros.</span></span> <span data-ttu-id="94f74-116">Da die erforderliche Mindestgröße von der Schriftart abhängig ist, die das Steuerelement verwendet, verwendet das Beispiel das [**monthcal \_ getminreqrect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) -Makro, um Größen Informationen anzufordern, und ändert anschließend die Größe des Steuer Elements, indem [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="94f74-116">Because the minimum required size depends on the font that the control uses, the example uses the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro to request size information and then resizes the control by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="94f74-117">Wenn Sie anschließend die Schriftart mit [**WM \_ setFont**](/windows/desktop/winmsg/wm-setfont)ändern, werden die Abmessungen des Steuer Elements nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="94f74-117">If you subsequently change the font with [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont), the dimensions of the control will not change.</span></span> <span data-ttu-id="94f74-118">Sie müssen **monthcal \_ getminreqrect** erneut aufrufen und die Größe des Steuer Elements an die neue Schriftart anpassen.</span><span class="sxs-lookup"><span data-stu-id="94f74-118">You must call **MonthCal\_GetMinReqRect** again and resize the control to fit the new font.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="94f74-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94f74-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f74-120">Verweis für Monatskalender-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="94f74-120">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="94f74-121">Informationen zu Monatskalender-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="94f74-121">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="94f74-122">Verwenden von Monatskalender-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="94f74-122">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 