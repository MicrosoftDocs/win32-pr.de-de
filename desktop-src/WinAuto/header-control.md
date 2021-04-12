---
title: Header Steuer Element (MSAA UI-Element Referenz)
description: Ein Header Steuerelement zeigt Überschriften am oberen Rand der Spalten von Informationen an und ermöglicht dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren. Windows-Explorer verwendet ein Header-Steuerelement, wenn die Detailansicht ausgewählt wird.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310760"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="af30a-104">Header Steuer Element (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="af30a-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="af30a-105">In diesem Thema werden **Header Steuerungs** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="af30a-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="af30a-106">Die Vorgehensweise zum Erstellen von **Header Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="af30a-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="af30a-107">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="af30a-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="af30a-108">Ein Header Steuerelement zeigt Überschriften am oberen Rand der Spalten von Informationen an und ermöglicht dem Benutzer, die Informationen durch Klicken auf die Überschriften zu sortieren.</span><span class="sxs-lookup"><span data-stu-id="af30a-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="af30a-109">Windows-Explorer verwendet ein Header-Steuerelement, wenn die Detailansicht ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="af30a-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="af30a-110">Der Fenster Klassenname für ein Header Steuerelement ist ein WC- \_ Header, der in "kommctrl. h" als "SysHeader32" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="af30a-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="af30a-111">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="af30a-111">IAccessible Methods</span></span>

<span data-ttu-id="af30a-112">Ein Header-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="af30a-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="af30a-113">Methode</span><span class="sxs-lookup"><span data-stu-id="af30a-113">Method</span></span>                                                                    | <span data-ttu-id="af30a-114">Kommentare</span><span class="sxs-lookup"><span data-stu-id="af30a-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="af30a-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="af30a-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="af30a-116">Diese Methode führt die Standardaktion durch Klicken auf den Header aus.</span><span class="sxs-lookup"><span data-stu-id="af30a-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="af30a-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="af30a-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="af30a-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="af30a-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="af30a-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="af30a-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="af30a-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="af30a-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="af30a-121">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="af30a-121">IAccessible Properties</span></span>

<span data-ttu-id="af30a-122">Ein Header-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="af30a-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="af30a-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af30a-123">Property</span></span>                                                                       | <span data-ttu-id="af30a-124">Kommentare</span><span class="sxs-lookup"><span data-stu-id="af30a-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af30a-125">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="af30a-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="af30a-126">Die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="af30a-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="af30a-127">**get \_ accdefaultaction**</span><span class="sxs-lookup"><span data-stu-id="af30a-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="af30a-128">Die **DEFAULTACTION** -Eigenschaft ist "Click".</span><span class="sxs-lookup"><span data-stu-id="af30a-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="af30a-129">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="af30a-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="af30a-130">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="af30a-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="af30a-131">Die **Name** -Eigenschaft ist identisch mit dem Namen der Spaltenüberschrift.</span><span class="sxs-lookup"><span data-stu-id="af30a-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="af30a-132">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="af30a-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="af30a-133">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Liste**](object-roles.md) ), das das Steuerelement umgibt und denselben Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="af30a-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="af30a-134">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="af30a-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="af30a-135">Die **Role** -Eigenschaft ist [**Rollen \_ System- \_ ColumnHeader**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="af30a-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="af30a-136">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="af30a-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="af30a-137">Der Wert für die **State** -Eigenschaft lautet [**immer \_ Zustands \_ System**](object-state-constants.md) schreibgeschützt und kann auch [**Status \_ System \_ unsichtbar**](object-state-constants.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="af30a-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="af30a-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af30a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af30a-139">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="af30a-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




