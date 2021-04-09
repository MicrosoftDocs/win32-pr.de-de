---
title: Erstellen von Syslink-Steuerelementen
description: Sie implementieren die Hyperlinks des Syslink-Steuer Elements über das Markup in der Initialisierungs Zeichenfolge des Steuer Elements, oder indem Sie eine LM \_ SetItem-Nachricht senden.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730656"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="3287d-103">Erstellen von Syslink-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3287d-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="3287d-104">Sie implementieren die Hyperlinks des Syslink-Steuer Elements über das Markup in der Initialisierungs Zeichenfolge des Steuer Elements, oder indem Sie eine [**LM \_ SetItem**](lm-setitem.md) -Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="3287d-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="3287d-105">Bevor Sie Syslink-Steuerelemente erstellen, müssen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion mit Angabe der "ICC Link"- \_ Klasse abrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="3287d-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="3287d-106">Um einen Syslink zu erstellen, rufen Sie die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf, und geben Sie die Fenster Klasse " [**WC- \_ Link**](common-control-window-classes.md)</span><span class="sxs-lookup"><span data-stu-id="3287d-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="3287d-107">Der *lpWindowName* -Parameter, der diesen Funktionen gemeinsam ist, gibt einen Zeiger auf eine mit NULL endenden Zeichenfolge an, die den markierten Text enthält, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3287d-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="3287d-108">Informationen zu den in den Syslink-Steuerelementen spezifischen Fenster Formaten finden Sie unter [Syslink-Steuerelement Stile](syslink-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="3287d-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3287d-109">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3287d-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3287d-110">Technologien</span><span class="sxs-lookup"><span data-stu-id="3287d-110">Technologies</span></span>

-   [<span data-ttu-id="3287d-111">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3287d-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3287d-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3287d-112">Prerequisites</span></span>

-   <span data-ttu-id="3287d-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="3287d-113">C/C++</span></span>
-   <span data-ttu-id="3287d-114">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3287d-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3287d-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3287d-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="3287d-116">Erstellen eines Syslink-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="3287d-116">Create a SysLink Control</span></span>

<span data-ttu-id="3287d-117">Der folgende Beispielcode erstellt ein Syslink-Steuerelement, das zwei Hyperlinks anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3287d-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="3287d-118">Der erste Hyperlink ist eine Internet-URL, die zweite ist Anwendungs definiert.</span><span class="sxs-lookup"><span data-stu-id="3287d-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="3287d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3287d-119">Remarks</span></span>

<span data-ttu-id="3287d-120">Es wird davon ausgegangen, dass [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) bereits aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3287d-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="3287d-121">Durch Angeben des [**WS- \_ Tabstopps**](/windows/desktop/winmsg/window-styles) -Stils wird sichergestellt, dass der Benutzer einen Link auswählen kann, indem er die Tab-Taste gedrückt und die EINGABETASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="3287d-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="3287d-122">In Version 6 von ComCtl32.dll wird nur Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3287d-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="3287d-123">Daher können Sie keine ANSI-Versionen von Syslink-Steuerelementen erstellen – nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="3287d-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3287d-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3287d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3287d-125">Verwenden von Syslink-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="3287d-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="3287d-126">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3287d-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 