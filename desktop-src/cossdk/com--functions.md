---
description: Im folgenden finden Sie die com+-Funktionen.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Com+-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106367292"
---
# <a name="com-functions"></a><span data-ttu-id="28eec-103">Com+-Funktionen</span><span class="sxs-lookup"><span data-stu-id="28eec-103">COM+ Functions</span></span>

<span data-ttu-id="28eec-104">Im folgenden finden Sie die com+-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="28eec-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="28eec-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="28eec-105">Function</span></span>                                                                 | <span data-ttu-id="28eec-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28eec-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28eec-107">**Cokreateactivity**</span><span class="sxs-lookup"><span data-stu-id="28eec-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="28eec-108">Erstellt eine Aktivität für die synchrone oder asynchrone Batchverarbeitung, die COM+-Dienste verwenden kann, ohne dass eine COM+-Komponente erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="28eec-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="28eec-109">**Coenterservicedomain**</span><span class="sxs-lookup"><span data-stu-id="28eec-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="28eec-110">Wird verwendet, um Code einzugeben, der dann com+-Dienste verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="28eec-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="28eec-111">**Cogetdefaultcontext**</span><span class="sxs-lookup"><span data-stu-id="28eec-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="28eec-112">Ruft einen Verweis auf den Standardkontext des angegebenen Apartment ab.</span><span class="sxs-lookup"><span data-stu-id="28eec-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="28eec-113">**Coleaveservicedomain**</span><span class="sxs-lookup"><span data-stu-id="28eec-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="28eec-114">Wird verwendet, um Code zu verlassen, der com+-Dienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="28eec-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="28eec-115">**Compluscompletecbbsetup**</span><span class="sxs-lookup"><span data-stu-id="28eec-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="28eec-116">Schließt eine Katalog Migration auf dem Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="28eec-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="28eec-117">**Getcompluspackageingestallstatus**</span><span class="sxs-lookup"><span data-stu-id="28eec-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="28eec-118">Gibt an, ob die Common Language Runtime (CLR) von 64 Bit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="28eec-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="28eec-119">**Getdispenser Server-Manager**</span><span class="sxs-lookup"><span data-stu-id="28eec-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="28eec-120">Ruft die [**idispenser Manager Manager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) -Schnittstelle des Dispenser-Managers ab.</span><span class="sxs-lookup"><span data-stu-id="28eec-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="28eec-121">**Getmanagedextensions**</span><span class="sxs-lookup"><span data-stu-id="28eec-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="28eec-122">Bestimmt, ob die installierte Version von com+ spezielle Features unterstützt, die zum Verwalten von Serviced Components (verwalteten Objekten) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="28eec-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="28eec-123">**GetObjectContext**</span><span class="sxs-lookup"><span data-stu-id="28eec-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="28eec-124">Ruft einen Verweis auf den Kontext ab, der dem aktuellen com+-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="28eec-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="28eec-125">**Mtscreateactivity**</span><span class="sxs-lookup"><span data-stu-id="28eec-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="28eec-126">Erstellt eine Aktivität in einem Single Thread-Apartment, um synchrone oder asynchrone Batch Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="28eec-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="28eec-127">**Recycleersatz**</span><span class="sxs-lookup"><span data-stu-id="28eec-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="28eec-128">Wieder verwendet den aufrufenden Prozess.</span><span class="sxs-lookup"><span data-stu-id="28eec-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="28eec-129">**Saferef**</span><span class="sxs-lookup"><span data-stu-id="28eec-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="28eec-130">Veralteten Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="28eec-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



