---
title: Erstellen einer Tastaturschnittstelle für Standard Scrollleisten
description: Obwohl ein Schiebe leisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies für eine Standard Scrollleiste nicht der Standard.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858496"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="3cf0b-103">Erstellen einer Tastaturschnittstelle für Standard Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="3cf0b-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="3cf0b-104">Obwohl ein Schiebe leisten-Steuerelement eine integrierte Tastaturschnittstelle bereitstellt, ist dies für eine Standard Scrollleiste nicht der Standard.</span><span class="sxs-lookup"><span data-stu-id="3cf0b-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="3cf0b-105">Um eine Tastaturschnittstelle für eine Standard Scrollleiste zu implementieren, muss eine Fenster Prozedur die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht verarbeiten und den durch den *wParam* -Parameter angegebenen Code des virtuellen Schlüssels überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3cf0b-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="3cf0b-106">Wenn der Code des virtuellen Schlüssels einer Pfeiltaste entspricht, sendet die Fenster Prozedur selbst eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Nachricht, bei der das nieder wertige Wort des *wParam* -Parameters auf den entsprechenden Anforderungs Code der Schiebe Leiste festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3cf0b-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="3cf0b-107">Wenn der Benutzer z. b. die nach-oben-Taste drückt, empfängt die Fenster Prozedur eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht mit *wParam* , die der "VK up" entspricht \_ .</span><span class="sxs-lookup"><span data-stu-id="3cf0b-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="3cf0b-108">Als Antwort sendet die Fenster Prozedur eine WM- [**\_ VScroll**](wm-vscroll.md) -Nachricht, bei der das nieder wertige Wort von *wParam* auf den SB-Anstellungs Anforderungs Code festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="3cf0b-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3cf0b-109">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3cf0b-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3cf0b-110">Technologien</span><span class="sxs-lookup"><span data-stu-id="3cf0b-110">Technologies</span></span>

-   [<span data-ttu-id="3cf0b-111">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="3cf0b-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3cf0b-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3cf0b-112">Prerequisites</span></span>

-   <span data-ttu-id="3cf0b-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="3cf0b-113">C/C++</span></span>
-   <span data-ttu-id="3cf0b-114">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="3cf0b-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3cf0b-115">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3cf0b-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="3cf0b-116">Erstellen einer Tastaturschnittstelle für eine Standard Scrollleiste</span><span class="sxs-lookup"><span data-stu-id="3cf0b-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="3cf0b-117">Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Tastaturschnittstelle für eine Standard Scrollleiste einschließen.</span><span class="sxs-lookup"><span data-stu-id="3cf0b-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="3cf0b-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cf0b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf0b-119">Verwenden von Scrollleisten</span><span class="sxs-lookup"><span data-stu-id="3cf0b-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="3cf0b-120">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3cf0b-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 