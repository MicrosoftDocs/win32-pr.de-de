---
title: Größen Zieh Punkt (MSAA UI-Element Referenz)
description: Der Größen Zieh Punkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, in dem ein Benutzer auf den Größen Zieh Punkt klicken und ihn ziehen kann, um die Größe des Fensters zu ändern.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714135"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="d6c73-103">Größen Zieh Punkt (MSAA UI-Element Referenz)</span><span class="sxs-lookup"><span data-stu-id="d6c73-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="d6c73-104">Der Größen Zieh Punkt ist ein spezieller Mauszeiger in der unteren rechten Ecke eines Fensters, in dem ein Benutzer auf den Größen Zieh Punkt klicken und ihn ziehen kann, um die Größe des Fensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="d6c73-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="d6c73-105">IAccessible-Methoden</span><span class="sxs-lookup"><span data-stu-id="d6c73-105">IAccessible Methods</span></span>

<span data-ttu-id="d6c73-106">Der Größen Zieh Punkt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:</span><span class="sxs-lookup"><span data-stu-id="d6c73-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="d6c73-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="d6c73-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="d6c73-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="d6c73-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="d6c73-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="d6c73-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="d6c73-110">IAccessible-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6c73-110">IAccessible Properties</span></span>

<span data-ttu-id="d6c73-111">Der Größen Zieh Punkt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d6c73-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="d6c73-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6c73-112">Property</span></span>                                                                   | <span data-ttu-id="d6c73-113">Kommentare</span><span class="sxs-lookup"><span data-stu-id="d6c73-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6c73-114">**get- \_ accdescription**</span><span class="sxs-lookup"><span data-stu-id="d6c73-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="d6c73-115">Die **Description** -Eigenschaft ist "kann verwendet werden, um die Breite und Höhe eines Fensters zu ändern".</span><span class="sxs-lookup"><span data-stu-id="d6c73-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="d6c73-116">**\_accName erhalten**</span><span class="sxs-lookup"><span data-stu-id="d6c73-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="d6c73-117">Die **Name** -Eigenschaft ist "Size Box".</span><span class="sxs-lookup"><span data-stu-id="d6c73-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="d6c73-118">**\_accParent erhalten**</span><span class="sxs-lookup"><span data-stu-id="d6c73-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="d6c73-119">Das Fenster, das den Größen Zieh Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="d6c73-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="d6c73-120">**get- \_ Zugriffs Rolle**</span><span class="sxs-lookup"><span data-stu-id="d6c73-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="d6c73-121">Die **Role** -Eigenschaft ist ein [**Rollen \_ System \_**](object-roles.md)-Ziehpunkt.</span><span class="sxs-lookup"><span data-stu-id="d6c73-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="d6c73-122">**\_accState erhalten**</span><span class="sxs-lookup"><span data-stu-id="d6c73-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="d6c73-123">Der Wert für die **State** -Eigenschaft ist 0 (null), was bedeutet, dass das Objekt sichtbar ist oder das [**Zustands \_ System \_ unsichtbar**](object-state-constants.md)ist.</span><span class="sxs-lookup"><span data-stu-id="d6c73-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d6c73-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6c73-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6c73-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="d6c73-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




