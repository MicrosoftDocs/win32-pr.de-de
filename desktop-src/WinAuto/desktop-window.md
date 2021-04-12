---
title: Desktop Fenster (MSAA UI-Element Referenz)
description: Das Desktop Fenster zeigt die Desktop Listenansicht an (die Symbole wie Arbeitsplatz enthält) und die Taskleiste, die die Schaltfläche Start enthält.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388063"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="a7d3d-103">Desktop Fenster (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="a7d3d-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="a7d3d-104">Das Desktop Fenster zeigt die Desktop Listenansicht an (die Symbole wie Arbeitsplatz enthält) und die Taskleiste, die die Schaltfläche **Start** enthält.</span><span class="sxs-lookup"><span data-stu-id="a7d3d-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="a7d3d-105">Dieses Objekt wird nur selten von Clients abgefragt, weil die Listenansicht und die Taskleiste den gesamten Desktop abdecken.</span><span class="sxs-lookup"><span data-stu-id="a7d3d-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="a7d3d-106">Das Desktop Objekt wird abgerufen, wenn Sie sich anmelden, bevor die Betriebssystem-Shell die Listenansicht und die Taskleiste anzeigt.</span><span class="sxs-lookup"><span data-stu-id="a7d3d-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="a7d3d-107">In einigen Fällen wird der Desktop beim Navigieren von anderen Objekten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a7d3d-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="a7d3d-108">Der Fenster Klassenname für das Desktop Fenster lautet " \# 32769".</span><span class="sxs-lookup"><span data-stu-id="a7d3d-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="a7d3d-109">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="a7d3d-109">IAccessible Methods</span></span>

<span data-ttu-id="a7d3d-110">Das Desktop Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="a7d3d-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="a7d3d-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="a7d3d-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="a7d3d-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="a7d3d-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="a7d3d-115">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7d3d-115">IAccessible Properties</span></span>

<span data-ttu-id="a7d3d-116">Das Desktop Fenster unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a7d3d-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="a7d3d-117">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7d3d-117">Property</span></span>                                                                 | <span data-ttu-id="a7d3d-118">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a7d3d-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7d3d-119">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a7d3d-120">**\_Zugriffs Fokus erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a7d3d-121">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="a7d3d-122">Die Name-Eigenschaft ist "Desktop".</span><span class="sxs-lookup"><span data-stu-id="a7d3d-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a7d3d-123">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="a7d3d-124">Die **Role** -Eigenschaft ist [**role \_ System \_ Client**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="a7d3d-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="a7d3d-125">**\_Zugriffs Auswahl**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a7d3d-126">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="a7d3d-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="a7d3d-127">Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="a7d3d-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a7d3d-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7d3d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7d3d-129">IAccessible-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a7d3d-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





