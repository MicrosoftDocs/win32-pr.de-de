---
title: Vorgehensweise beim unterstützen von Rückruf Elementen
description: In diesem Thema wird veranschaulicht, wie Rückruf Elemente unterstützt werden.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 056f64c086aeda94ccf928d93ae2c5db5e2187a4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949228"
---
# <a name="how-to-support-callback-items"></a><span data-ttu-id="99e24-103">Vorgehensweise beim unterstützen von Rückruf Elementen</span><span class="sxs-lookup"><span data-stu-id="99e24-103">How to Support Callback Items</span></span>

<span data-ttu-id="99e24-104">In diesem Thema wird veranschaulicht, wie Rückruf Elemente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="99e24-104">This topic demonstrates how to provide support for callback items.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="99e24-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="99e24-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="99e24-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="99e24-106">Technologies</span></span>

-   [<span data-ttu-id="99e24-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="99e24-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="99e24-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="99e24-108">Prerequisites</span></span>

-   <span data-ttu-id="99e24-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="99e24-109">C/C++</span></span>
-   <span data-ttu-id="99e24-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="99e24-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="99e24-111">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="99e24-111">Instructions</span></span>


<span data-ttu-id="99e24-112">Wenn die Anwendung Rückruf Elemente in einem ComboBoxEx-Steuerelement verwendet, muss Sie darauf vorbereitet sein, den [cben \_ getdispinfo](cben-getdispinfo.md) -Benachrichtigungs Code zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="99e24-112">If your application is going to use callback items in a ComboBoxEx control, it must be prepared to handle the [CBEN\_GETDISPINFO](cben-getdispinfo.md) notification code.</span></span> <span data-ttu-id="99e24-113">Ein ComboBoxEx-Steuerelement sendet diese Benachrichtigung, wenn der Besitzer bestimmte Element Informationen bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="99e24-113">A ComboBoxEx control sends this notification whenever it needs the owner to provide specific item information.</span></span> <span data-ttu-id="99e24-114">Weitere Informationen zu Rückruf Elementen finden Sie unter [Callback Items (Rückruf](comboboxex-controls.md)Elemente).</span><span class="sxs-lookup"><span data-stu-id="99e24-114">For more information about callback items, see [Callback Items](comboboxex-controls.md).</span></span>

<span data-ttu-id="99e24-115">Die folgende Anwendungs definierte Funktion verarbeitet [cben \_ getdispinfo](cben-getdispinfo.md) durch Bereitstellen von Attributen für ein bestimmtes Element.</span><span class="sxs-lookup"><span data-stu-id="99e24-115">The following application-defined function processes [CBEN\_GETDISPINFO](cben-getdispinfo.md) by providing attributes for a given item.</span></span> <span data-ttu-id="99e24-116">Beachten Sie, dass der **Mask** -Member der eingehenden [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur auf cbeif \_ di \_ SetItem festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="99e24-116">Note that it sets the **mask** member of the incoming [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM.</span></span> <span data-ttu-id="99e24-117">Wenn Sie **Mask** auf diesen Wert festlegen, behält das Steuerelement die Element Informationen bei, sodass die Informationen nicht erneut angefordert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="99e24-117">Setting **mask** to this value makes the control retain the item information so that it will not need to request the information again.</span></span>

## <a name="complete-example"></a><span data-ttu-id="99e24-118">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="99e24-118">Complete example</span></span>


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a><span data-ttu-id="99e24-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99e24-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e24-120">Informationen zu ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="99e24-120">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="99e24-121">ComboBoxEx-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="99e24-121">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="99e24-122">Verwenden von ComboBoxEx-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="99e24-122">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="99e24-123">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="99e24-123">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 