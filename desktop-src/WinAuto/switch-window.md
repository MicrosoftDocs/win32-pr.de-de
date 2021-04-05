---
title: Fenster wechseln (MSAA UI-Element Referenz)
description: Das Fenster Switch wird angezeigt, wenn ein Benutzer Alt + Tab drückt, um zu einer anderen Anwendung zu wechseln. Das Fenster Switch enthält ein Symbol für jede Anwendung, die gerade ausgeführt wird.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714129"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="af87d-104">Fenster wechseln (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="af87d-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="af87d-105">Das Fenster Switch wird angezeigt, wenn ein Benutzer Alt + Tab drückt, um zu einer anderen Anwendung zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="af87d-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="af87d-106">Das Fenster Switch enthält ein Symbol für jede Anwendung, die gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="af87d-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="af87d-107">Der Fenster Klassenname für das Fenster Switch lautet " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="af87d-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="af87d-108">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="af87d-108">IAccessible Methods</span></span>

<span data-ttu-id="af87d-109">Das Fenster Switch unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="af87d-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="af87d-110">Methode</span><span class="sxs-lookup"><span data-stu-id="af87d-110">Method</span></span>                                                                    | <span data-ttu-id="af87d-111">Kommentare</span><span class="sxs-lookup"><span data-stu-id="af87d-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af87d-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="af87d-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="af87d-113">Das Switch Window-Objekt selbst verfügt über keine **DEFAULTACTION** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="af87d-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="af87d-114">Die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode für jedes Element im Switch-Fenster aktiviert das angegebene Element.</span><span class="sxs-lookup"><span data-stu-id="af87d-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="af87d-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="af87d-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="af87d-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="af87d-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="af87d-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="af87d-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="af87d-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="af87d-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="af87d-119">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af87d-119">IAccessible Properties</span></span>

<span data-ttu-id="af87d-120">Das Fenster Switch unterstützt die [**folgenden Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , auf die zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="af87d-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af87d-121">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="af87d-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="af87d-122">Die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="af87d-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="af87d-123">**get \_ accdefaultaction**</span><span class="sxs-lookup"><span data-stu-id="af87d-123">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="af87d-124">Das Switch Window-Objekt selbst verfügt über keine **DEFAULTACTION** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="af87d-124">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="af87d-125">Die **DEFAULTACTION** -Eigenschaft für jedes Element im Switch-Fenster ist "Switch".</span><span class="sxs-lookup"><span data-stu-id="af87d-125">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="af87d-126">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="af87d-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="af87d-127">Das übergeordnete Objekt des Switch-Fensters kann den Fokus nicht erhalten. nur die einzelnen untergeordneten Elemente können den Fokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="af87d-127">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="af87d-128">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="af87d-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="af87d-129">Das Switch Window-Objekt selbst hat keine **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="af87d-129">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="af87d-130">Die **Name** -Eigenschaft für jedes Anwendungssymbol im Fenster Switch ist mit dem angezeigten Anwendungsnamen identisch.</span><span class="sxs-lookup"><span data-stu-id="af87d-130">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="af87d-131">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="af87d-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="af87d-132">Das Switch Window-Objekt selbst verfügt über die **Role** -Eigenschaft "Window \[ 32771 \] ".</span><span class="sxs-lookup"><span data-stu-id="af87d-132">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="af87d-133">Außerdem verfügt jedes Anwendungssymbol im Fenster Switch über die **Rollen** Eigenschaften [**Rolle \_ System \_ ListItem**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="af87d-133">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="af87d-134">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="af87d-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="af87d-135">Das Switch Window-Objekt selbst unterstützt die **State** -Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="af87d-135">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="af87d-136">Der **Zustands** Wert für die Listen Ansichts Elemente ist [**Zustands \_ System- \_ focverwendbar**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="af87d-136">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="af87d-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af87d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af87d-138">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="af87d-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




