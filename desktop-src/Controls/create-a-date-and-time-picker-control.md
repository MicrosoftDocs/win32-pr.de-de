---
title: Erstellen eines Steuer Elements für die Datums-und Zeitauswahl
description: In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für Datums-und Zeitauswahl (DTP) dynamisch erstellen.
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104209357"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="93310-103">Erstellen eines Steuer Elements für die Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="93310-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="93310-104">In diesem Thema wird veranschaulicht, wie Sie ein Steuerelement für Datums-und Zeitauswahl (DTP) dynamisch erstellen.</span><span class="sxs-lookup"><span data-stu-id="93310-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="93310-105">Das dazugehörige C++-Codebeispiel erstellt ein DTP-Steuerelement in einem nicht modalem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="93310-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="93310-106">Er verwendet den [**DTS- \_ shownone**](date-and-time-picker-control-styles.md) -Stil, um dem Benutzer zu ermöglichen, die Deaktivierung des Datums im Steuerelement zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="93310-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="93310-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="93310-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="93310-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="93310-108">Technologies</span></span>

-   [<span data-ttu-id="93310-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="93310-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="93310-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="93310-110">Prerequisites</span></span>

-   <span data-ttu-id="93310-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="93310-111">C/C++</span></span>
-   <span data-ttu-id="93310-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="93310-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="93310-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="93310-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="93310-114">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="93310-114">Step 1:</span></span>

<span data-ttu-id="93310-115">Registrieren Sie die Fenster Klasse, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen \_ und \_ in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur das Bit "ICC Date Classes" angeben.</span><span class="sxs-lookup"><span data-stu-id="93310-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="93310-116">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="93310-116">Step 2:</span></span>

<span data-ttu-id="93310-117">Um das DTP-Steuerelement zu erstellen, verwenden Sie die Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ".</span><span class="sxs-lookup"><span data-stu-id="93310-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="93310-118">Geben Sie die [**datetimepick- \_ Klasse**](common-control-window-classes.md) als Fenster Klasse an, und übergeben Sie das Handle an das übergeordnete Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="93310-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="93310-119">Im folgenden C++-Codebeispiel wird [**die Funktion "-Dialogfeld**](/windows/desktop/api/winuser/nf-winuser-createdialoga) " verwendet, um ein nicht modalem Dialogfeld zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93310-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="93310-120">Anschließend wird " **kreatewindowex** " aufgerufen, um das DTP-Steuerelement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93310-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="93310-121">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="93310-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="93310-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93310-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93310-123">Verwenden von Steuerelementen für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="93310-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="93310-124">Steuerelement Verweis für Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="93310-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="93310-125">Datums-und Zeitauswahl</span><span class="sxs-lookup"><span data-stu-id="93310-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 