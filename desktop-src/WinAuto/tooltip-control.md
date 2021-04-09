---
title: ToolTip-Steuer Element (MSAA UI-Element Referenz)
description: Ein QuickInfo-Steuerelement zeigt ein kleines Popup Fenster an, das eine Textzeile enthält, in der der Zweck eines als grafisches Objekt dargestellten Tools in einer Anwendung beschrieben wird.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856160"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="acf40-103">ToolTip-Steuer Element (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="acf40-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="acf40-104">In diesem Thema werden QuickInfo- **Steuer** Elemente für den MSAA-Benutzeroberflächen-Element Verweis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="acf40-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="acf40-105">Das Erstellen von QuickInfo- **Steuer** Element Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="acf40-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="acf40-106">Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.</span><span class="sxs-lookup"><span data-stu-id="acf40-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="acf40-107">Ein QuickInfo-Steuerelement zeigt ein kleines Popup Fenster an, das eine Textzeile enthält, in der der Zweck eines als grafisches Objekt dargestellten Tools in einer Anwendung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="acf40-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="acf40-108">Der Fenster Klassenname für eine QuickInfo ist die Tooltips- \_ Klasse, die als "Tooltips- \_ Klasse" in "kommctrl. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="acf40-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="acf40-109">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="acf40-109">IAccessible Methods</span></span>

<span data-ttu-id="acf40-110">Ein QuickInfo-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="acf40-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="acf40-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="acf40-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="acf40-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="acf40-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="acf40-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="acf40-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="acf40-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="acf40-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="acf40-115">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="acf40-115">IAccessible Properties</span></span>

<span data-ttu-id="acf40-116">Ein QuickInfo-Steuerelement unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="acf40-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="acf40-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="acf40-117">Property</span></span>                                                                 | <span data-ttu-id="acf40-118">Kommentare</span><span class="sxs-lookup"><span data-stu-id="acf40-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acf40-119">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="acf40-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="acf40-120">Die **childCount** -Eigenschaft ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="acf40-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="acf40-121">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="acf40-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="acf40-122">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="acf40-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="acf40-123">Die **Name** -Eigenschaft ist der Text, der im QuickInfo-Steuerelement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="acf40-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="acf40-124">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="acf40-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="acf40-125">Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.</span><span class="sxs-lookup"><span data-stu-id="acf40-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="acf40-126">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="acf40-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="acf40-127">Die **Role** -Eigenschaft [**ist \_ Rollen \_ System**](object-roles.md)-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="acf40-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="acf40-128">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="acf40-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="acf40-129">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="acf40-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="acf40-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="acf40-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf40-131">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="acf40-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





