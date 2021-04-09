---
title: Hinzufügen von Treibern in einer Anwendung
description: Hinzufügen von Treibern in einer Anwendung
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Audiokomprimierungs-Manager (ACM), Hinzufügen von Treibern
- ACM (Audiokomprimierungs-Manager), Hinzufügen von Treibern
- ACM-Beispiele, Hinzufügen von Treibern
- Hinzufügen von Treibern
- acmdriveradd-Funktion
- globale Treiber
- lokale Treiber
- Audiokomprimierungs-Manager (ACM), globale Treiber
- ACM (Audiokomprimierungs-Manager), globale Treiber
- Audiokomprimierungs-Manager (ACM), lokale Treiber
- ACM (Audiokomprimierungs-Manager), lokale Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036978"
---
# <a name="adding-drivers-within-an-application"></a><span data-ttu-id="4fbb5-114">Hinzufügen von Treibern in einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="4fbb5-114">Adding Drivers Within an Application</span></span>

<span data-ttu-id="4fbb5-115">Wenn Sie möchten, dass Ihre Anwendung ihre eigenen Komprimierungs Routinen intern implementiert, kann die Anwendung dem ACM Treiber hinzufügen, indem Sie die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-115">If you need your application to implement its own compression routines internally, the application can add drivers to the ACM by calling the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span> <span data-ttu-id="4fbb5-116">Die Anwendung implementiert den Treiber durch Bereitstellen einer Funktion, die dem [**acmdriverproc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) -Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-116">The application implements the driver by providing a function that conforms to the [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) prototype.</span></span> <span data-ttu-id="4fbb5-117">Nachdem der Treiber von der Anwendung hinzugefügt wurde, kann die Anwendung den Treiber über das ACM verwenden, da er einen beliebigen anderen Treiber verwenden würde.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-117">After the application has added the driver, the application can use the driver through the ACM as it would use any other driver.</span></span>

<span data-ttu-id="4fbb5-118">Der ACM behandelt Treiber entweder global oder local.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-118">The ACM treats drivers as either global or local.</span></span> <span data-ttu-id="4fbb5-119">Eine Anwendung gibt an, ob ein Treiber als Global oder local hinzugefügt werden soll, wenn er **acmdriveradd** aufruft.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-119">An application specifies whether a driver should be added as global or local when it calls **acmDriverAdd**.</span></span> <span data-ttu-id="4fbb5-120">Es gibt zwei Unterschiede zwischen globalen und lokalen Treibern:</span><span class="sxs-lookup"><span data-stu-id="4fbb5-120">There are two differences between global and local drivers:</span></span>

-   <span data-ttu-id="4fbb5-121">Treiber, die als globale Treiber hinzugefügt werden, werden nicht für andere Anwendungen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-121">Drivers added as global drivers are not shared with other applications.</span></span>
-   <span data-ttu-id="4fbb5-122">Eine Anwendung kann die Priorität eines globalen Treibers (aber nicht eines lokalen Treibers) direkt ändern, indem er die [**acmdriverpriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-122">An application can directly alter the priority of a global driver (but not a local driver) by calling the [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) function.</span></span> <span data-ttu-id="4fbb5-123">Der ACM führt bei der Suche nach einem geeigneten Treiber eine priorisierte Suche durch, um eine Implementierung eines Funktions Aufrufes bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-123">The ACM conducts a prioritized search when seeking an appropriate driver to provide an implementation of a function call.</span></span> <span data-ttu-id="4fbb5-124">Das ACM gibt immer höhere Priorität für lokale Treiber als globale Treiber.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-124">The ACM always gives local drivers higher priority than global drivers.</span></span> <span data-ttu-id="4fbb5-125">Der zuletzt hinzugefügte lokale Treiber hat die höchste Priorität.</span><span class="sxs-lookup"><span data-stu-id="4fbb5-125">The most recently added local driver has highest priority.</span></span>

 

 




