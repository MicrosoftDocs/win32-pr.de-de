---
title: Objekt Navigations Eigenschaften und-Methoden
description: Clients Navigieren von einem Objekt zu einem anderen mithilfe von Methoden wie IAccessible accNavigate und IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947613"
---
# <a name="object-navigation-properties-and-methods"></a><span data-ttu-id="fb042-103">Objekt Navigations Eigenschaften und-Methoden</span><span class="sxs-lookup"><span data-stu-id="fb042-103">Object Navigation Properties and Methods</span></span>

<span data-ttu-id="fb042-104">Clients *Navigieren* von einem Objekt zu einem anderen mithilfe von Methoden wie [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) und [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span><span class="sxs-lookup"><span data-stu-id="fb042-104">Clients *navigate* from one object to another using methods such as [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) and [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest).</span></span> <span data-ttu-id="fb042-105">Diese Methoden ermöglichen es Clients, entweder eine untergeordnete ID oder die Adresse der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle eines anderen Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fb042-105">These methods allow clients to retrieve either a child ID or the address of another object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="fb042-106">Mithilfe der Navigation können Clients untersuchen, wie Objekte miteinander in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="fb042-106">Navigation allows clients to explore how objects are related to each other.</span></span> <span data-ttu-id="fb042-107">Beachten Sie, dass beim Navigieren zu einem anderen Objekt die Auswahl oder der Fokus nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb042-107">Note that navigating to another object does not change the selection or focus.</span></span>

<span data-ttu-id="fb042-108">Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle stellt Eigenschaften und Methoden bereit, die die folgenden Arten der Navigation unterstützen:</span><span class="sxs-lookup"><span data-stu-id="fb042-108">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides properties and methods that support the following kinds of navigation:</span></span>

-   [<span data-ttu-id="fb042-109">Hierarchische Navigation</span><span class="sxs-lookup"><span data-stu-id="fb042-109">Hierarchical Navigation</span></span>](hierarchical-navigation.md)
-   [<span data-ttu-id="fb042-110">Räumliche und logische Navigation</span><span class="sxs-lookup"><span data-stu-id="fb042-110">Spatial and Logical Navigation</span></span>](spatial-and-logical-navigation.md)
-   [<span data-ttu-id="fb042-111">Navigation durch Treffer Tests und Bildschirmposition</span><span class="sxs-lookup"><span data-stu-id="fb042-111">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)

 

 




