---
title: Popup Menü (MSAA UI-Element Referenz)
description: In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856496"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="9cef2-103">Popup Menü (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="9cef2-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="9cef2-104">In diesem Thema werden **Popup Menü** Objekte zum Zweck der MSAA-Benutzeroberflächen-Element Referenz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9cef2-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="9cef2-105">Hier wird beschrieben, wie Sie **Popup Menü** Objekte in verschiedenen Benutzeroberflächen-Frameworks erstellen.</span><span class="sxs-lookup"><span data-stu-id="9cef2-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="9cef2-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="9cef2-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="9cef2-107">In einem Popupmenü wird eine Liste mit Menübefehlen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9cef2-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="9cef2-108">Microsoft Active Accessibility erstellt ein Popup-Menü Objekt, wenn ein Menü Element in einer Menüleiste geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="9cef2-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="9cef2-109">Microsoft Active Accessibility erstellt auch Menü-Popup Objekte für Kontextmenüs, die angezeigt werden, wenn der Benutzer mit der rechten Maustaste auf ein Benutzeroberflächen Element klickt.</span><span class="sxs-lookup"><span data-stu-id="9cef2-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="9cef2-110">Der Fenster Klassenname für ein Popup Menü ist " \# 32768".</span><span class="sxs-lookup"><span data-stu-id="9cef2-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="9cef2-111">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="9cef2-111">IAccessible Methods</span></span>

<span data-ttu-id="9cef2-112">Ein Popup Menü unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="9cef2-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="9cef2-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="9cef2-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="9cef2-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="9cef2-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="9cef2-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="9cef2-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="9cef2-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="9cef2-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="9cef2-117">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9cef2-117">IAccessible Properties</span></span>

<span data-ttu-id="9cef2-118">Ein Popup Menü unterstützt [**die folgenden Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , auf die zugegriffen werden kann:</span><span class="sxs-lookup"><span data-stu-id="9cef2-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="9cef2-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9cef2-119">Property</span></span>                                                                 | <span data-ttu-id="9cef2-120">Kommentare</span><span class="sxs-lookup"><span data-stu-id="9cef2-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cef2-121">**\_accChild erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cef2-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="9cef2-122">Ruft das [**IDispatch**](idispatch-interface.md) für das angegebene Menü Element ab.</span><span class="sxs-lookup"><span data-stu-id="9cef2-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="9cef2-123">Die untergeordneten IDs für die Menü Elemente werden nacheinander von oben nach unten nummeriert, beginnend mit einem.</span><span class="sxs-lookup"><span data-stu-id="9cef2-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9cef2-124">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="9cef2-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="9cef2-125">Die **childCount** -Eigenschaft ist die Anzahl der Menü Elemente im Menü, einschließlich Menü Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="9cef2-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9cef2-126">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cef2-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9cef2-127">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cef2-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="9cef2-128">Die **Name** -Eigenschaft für ein Popup Menü ist derselbe Name wie das Menü.</span><span class="sxs-lookup"><span data-stu-id="9cef2-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="9cef2-129">Die **Name** -Eigenschaft für ein Kontextmenü ist "Context".</span><span class="sxs-lookup"><span data-stu-id="9cef2-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="9cef2-130">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cef2-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="9cef2-131">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Popup Menü umgibt und die **Name** -Eigenschaft und den Namen der Fenster Klasse wie das Popup Menü enthält.</span><span class="sxs-lookup"><span data-stu-id="9cef2-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="9cef2-132">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="9cef2-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="9cef2-133">Die **Role** -Eigenschaft ist [**Rollen \_ System- \_ menupup**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="9cef2-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9cef2-134">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cef2-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="9cef2-135">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="9cef2-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="9cef2-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cef2-136">Notes</span></span>

-   <span data-ttu-id="9cef2-137">Popup-Menü Objekte erzeugen keine Ereignisse für [**Ereignis \_ Objekt \_ Erstellung**](event-constants.md) und [**Ereignis \_ Objekt \_ Zerstörung**](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="9cef2-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="9cef2-138">Mehrspaltige Menüs unterstützen nicht die Rechte des [**navDir \_ left**](navigation-constants.md) -oder [**\_ navDir**](navigation-constants.md) -Flags der [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9cef2-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="9cef2-139">Das [**Ereignis \_ System " \_ menupopupstart**](event-constants.md) " und das [**Ereignis \_ System " \_ menupopupend**](event-constants.md) " werden nicht konsistent gesendet.</span><span class="sxs-lookup"><span data-stu-id="9cef2-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="9cef2-140">Dies ist ein bekanntes Problem und wird behandelt.</span><span class="sxs-lookup"><span data-stu-id="9cef2-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9cef2-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9cef2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cef2-142">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9cef2-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="9cef2-143">**Menüleiste**</span><span class="sxs-lookup"><span data-stu-id="9cef2-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="9cef2-144">**Menü Element**</span><span class="sxs-lookup"><span data-stu-id="9cef2-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





