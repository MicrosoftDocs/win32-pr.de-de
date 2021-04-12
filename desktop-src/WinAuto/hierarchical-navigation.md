---
title: Hierarchische Navigation
description: Häufig müssen Clients auf der Grundlage ihrer über-/Unterordnungsbeziehungen zwischen Objekten wechseln. Beispielsweise verfügt ein Client möglicherweise bereits über Informationen über ein ToolBar-Steuerelement, aber keine Informationen zu den darin enthaltenen Schaltflächen.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206738"
---
# <a name="hierarchical-navigation"></a><span data-ttu-id="5aa31-104">Hierarchische Navigation</span><span class="sxs-lookup"><span data-stu-id="5aa31-104">Hierarchical Navigation</span></span>

<span data-ttu-id="5aa31-105">Häufig müssen Clients auf der Grundlage ihrer über-/Unterordnungsbeziehungen zwischen Objekten wechseln.</span><span class="sxs-lookup"><span data-stu-id="5aa31-105">Often clients must move between objects based on their parent-child relationships.</span></span> <span data-ttu-id="5aa31-106">Beispielsweise verfügt ein Client möglicherweise bereits über Informationen über ein ToolBar-Steuerelement, aber keine Informationen zu den darin enthaltenen Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="5aa31-106">For example, a client might already have information about a toolbar control, but not have information about the buttons contained within it.</span></span>

<span data-ttu-id="5aa31-107">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle macht die hierarchischen Beziehungen zwischen Objekten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa31-107">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface exposes the hierarchical relationships between objects.</span></span> <span data-ttu-id="5aa31-108">Clients können von einem übergeordneten Objekt zu seinen untergeordneten Elementen oder von einem untergeordneten Objekt zu dessen übergeordnetem Element navigieren, indem Sie [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) oder [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5aa31-108">Clients can navigate from a parent object to its children or from a child object to its parent by calling [**IAccessible::get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) or [**IAccessible::get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).</span></span>

 

 




