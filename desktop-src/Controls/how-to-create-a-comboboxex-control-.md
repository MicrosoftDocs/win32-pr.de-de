---
title: Erstellen eines ComboBoxEx-Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein ComboBoxEx-Steuerelement erstellt wird.
ms.assetid: E3D577AF-3290-431E-AA6C-1E9A9ED6448C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73989124982cb563fc008d7f3c543388cca685a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949258"
---
# <a name="how-to-create-a-comboboxex-control"></a><span data-ttu-id="7e9d0-103">Erstellen eines ComboBoxEx-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="7e9d0-103">How to Create a ComboBoxEx Control</span></span>

<span data-ttu-id="7e9d0-104">In diesem Thema wird veranschaulicht, wie ein ComboBoxEx-Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e9d0-104">This topic demonstrates how to create a ComboBoxEx control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7e9d0-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7e9d0-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="7e9d0-106">Technologies</span></span>

-   [<span data-ttu-id="7e9d0-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="7e9d0-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7e9d0-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-108">Prerequisites</span></span>

-   <span data-ttu-id="7e9d0-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7e9d0-109">C/C++</span></span>
-   <span data-ttu-id="7e9d0-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="7e9d0-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7e9d0-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-111">Instructions</span></span>


<span data-ttu-id="7e9d0-112">Um ein ComboBoxEx-Steuerelement zu erstellen, rufen Sie [**die Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ComboBoxEx" mithilfe von " [**WC \_ ComboBoxEx**](common-control-window-classes.md) " als Fenster Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="7e9d0-112">To create a ComboBoxEx control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, using [**WC\_COMBOBOXEX**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="7e9d0-113">Sie müssen zuerst die Fenster Klasse registrieren, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen, während Sie das Bit der Klasse "ICC \_ userex" \_ in der zugehörigen [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="7e9d0-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, while specifying the ICC\_USEREX\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

## <a name="complete-example"></a><span data-ttu-id="7e9d0-114">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e9d0-114">Complete example</span></span>

<span data-ttu-id="7e9d0-115">Die folgende Anwendungs definierte Funktion erstellt ein ComboBoxEx-Steuerelement mit [**dem \_ Dropdown**](combo-box-styles.md) -Stil CBS im Hauptfenster.</span><span class="sxs-lookup"><span data-stu-id="7e9d0-115">The following application-defined function creates a ComboBoxEx control with the [**CBS\_DROPDOWN**](combo-box-styles.md) style in the main window.</span></span>


```C++
// CreateComboEx - Registers the ComboBoxEx window class and creates
// a ComboBoxEx control in the client area of the main window.
//
// g_hwndMain - A handle to the main window.
// g_hinst    - A handle to the program instance.
HWND WINAPI CreateComboEx(void)
{
    HWND hwnd;
    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_USEREX_CLASSES;

    InitCommonControlsEx(&icex);

    hwnd = CreateWindowEx(0, WC_COMBOBOXEX, NULL,
                    WS_BORDER | WS_VISIBLE |
                    WS_CHILD | CBS_DROPDOWN,
                    // No size yet--resize after setting image list.
                    0,      // Vertical position of Combobox
                    0,      // Horizontal position of Combobox
                    0,      // Sets the width of Combobox
                    100,    // Sets the height of Combobox
                    g_hwndMain,
                    NULL,
                    g_hinst,
                    NULL);

    return (hwnd);
}
```



## <a name="related-topics"></a><span data-ttu-id="7e9d0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e9d0-117">Informationen zu ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-117">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="7e9d0-118">ComboBoxEx-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="7e9d0-118">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7e9d0-119">Verwenden von ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7e9d0-119">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="7e9d0-120">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="7e9d0-120">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 