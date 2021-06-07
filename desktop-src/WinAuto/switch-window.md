---
title: Switch-Fenster (MSAA UI-Elementreferenz)
description: Das Schalterfenster wird angezeigt, wenn ein Benutzer ALT+TAB drückt, um zu einer anderen Anwendung zu wechseln. Das Switchfenster enthält ein Symbol für jede derzeit ausgeführte Anwendung.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443981"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="0906d-104">Switch-Fenster (MSAA UI-Elementreferenz)</span><span class="sxs-lookup"><span data-stu-id="0906d-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="0906d-105">Das Schalterfenster wird angezeigt, wenn ein Benutzer ALT+TAB drückt, um zu einer anderen Anwendung zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="0906d-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="0906d-106">Das Switchfenster enthält ein Symbol für jede derzeit ausgeführte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0906d-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="0906d-107">Der Name der Fensterklasse für das Switchfenster lautet " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="0906d-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="0906d-108">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="0906d-108">IAccessible Methods</span></span>

<span data-ttu-id="0906d-109">Das Switchfenster unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)</span><span class="sxs-lookup"><span data-stu-id="0906d-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="0906d-110">Methode</span><span class="sxs-lookup"><span data-stu-id="0906d-110">Method</span></span>                                                                    | <span data-ttu-id="0906d-111">Kommentare</span><span class="sxs-lookup"><span data-stu-id="0906d-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0906d-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="0906d-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="0906d-113">Das Switchfensterobjekt selbst verfügt nicht über eine **DefaultAction-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="0906d-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="0906d-114">Die [**accDoDefaultAction-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) für jedes Element im Switchfenster aktiviert das angegebene Element.</span><span class="sxs-lookup"><span data-stu-id="0906d-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="0906d-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="0906d-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="0906d-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="0906d-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="0906d-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0906d-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="0906d-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="0906d-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="0906d-119">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0906d-119">IAccessible Properties</span></span>

<span data-ttu-id="0906d-120">Das Schalterfenster unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)</span><span class="sxs-lookup"><span data-stu-id="0906d-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|      <span data-ttu-id="0906d-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0906d-121">Property</span></span>                                                                          |      <span data-ttu-id="0906d-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0906d-122">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0906d-123">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="0906d-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="0906d-124">Die **ChildCount-Eigenschaft** ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0906d-124">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="0906d-125">**get \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="0906d-125">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="0906d-126">Das Switchfensterobjekt selbst verfügt nicht über eine **DefaultAction-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="0906d-126">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="0906d-127">Die **DefaultAction-Eigenschaft** für jedes Element im Switchfenster lautet "Switch".</span><span class="sxs-lookup"><span data-stu-id="0906d-127">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="0906d-128">**get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="0906d-128">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="0906d-129">Das übergeordnete Objekt des Switchfensters kann den Fokus nicht erhalten. nur die einzelnen untergeordneten Elemente können den Fokus erhalten.</span><span class="sxs-lookup"><span data-stu-id="0906d-129">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="0906d-130">**get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="0906d-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="0906d-131">Das Switchfensterobjekt selbst verfügt nicht über eine **Name-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="0906d-131">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="0906d-132">Die **Name-Eigenschaft** für jedes Anwendungssymbol im Switchfenster entspricht dem angezeigten Anwendungsnamen.</span><span class="sxs-lookup"><span data-stu-id="0906d-132">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="0906d-133">**get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="0906d-133">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="0906d-134">Das Switchfensterobjekt selbst verfügt über die **Role-Eigenschaft** "window \[ 32771". \]</span><span class="sxs-lookup"><span data-stu-id="0906d-134">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="0906d-135">Außerdem verfügt jedes Anwendungssymbol im Switchfenster über die **Role-Eigenschaft** [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="0906d-135">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="0906d-136">**get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="0906d-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="0906d-137">Das Switchfensterobjekt selbst unterstützt die **State-Eigenschaft** nicht.</span><span class="sxs-lookup"><span data-stu-id="0906d-137">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="0906d-138">Der **Wert State** für die Listenansichtselemente ist STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="0906d-138">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="0906d-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0906d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0906d-140">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0906d-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




