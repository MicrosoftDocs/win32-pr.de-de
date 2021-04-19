---
title: NDF-Funktionen
description: Die folgenden Funktionen ermöglichen Softwareentwicklern die Verwendung der vom Netzwerk Diagnose Framework (ndf) bereitgestellten Funktionalität.
ms.assetid: c2774e05-82f4-4d40-a80c-ad773bb03ca7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a039768b77d69072111f814cb871115bcca24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337571"
---
# <a name="ndf-functions"></a><span data-ttu-id="8bcf7-103">NDF-Funktionen</span><span class="sxs-lookup"><span data-stu-id="8bcf7-103">NDF Functions</span></span>

<span data-ttu-id="8bcf7-104">Die folgenden Funktionen ermöglichen Softwareentwicklern die Verwendung der vom Netzwerk Diagnose Framework (ndf) bereitgestellten Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-104">The following functions enable software developers to use the functionality provided by the Network Diagnostic Framework (NDF).</span></span> <span data-ttu-id="8bcf7-105">Wenn Netzwerkprobleme auftreten, kann NDF die Grundursache diagnostizieren und die erforderliche Auflösung ordnungsgemäß behandeln, manchmal sogar die erforderlichen Reparaturen durchführen.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-105">When network issues occur, NDF can diagnose the root cause and handle the necessary resolution gracefully, sometimes even performing the necessary repairs.</span></span>

> [!Note]  
> <span data-ttu-id="8bcf7-106">Diese Funktionen sind für Entwickler konzipiert, die grundlegende NDF-Funktionen in Ihren Anwendungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="8bcf7-106">These functions are for developers implementing basic NDF functionality in their applications.</span></span>

 

-   [<span data-ttu-id="8bcf7-107">**Copyhelperattribute**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-107">**CopyHelperAttribute**</span></span>](copyhelperattribute.md)
-   [<span data-ttu-id="8bcf7-108">**Copyrepairren Info**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-108">**CopyRepairInfo**</span></span>](copyrepairinfo.md)
-   [<span data-ttu-id="8bcf7-109">**Copyrootkauseingefo**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-109">**CopyRootCauseInfo**</span></span>](copyrootcauseinfo.md)
-   [<span data-ttu-id="8bcf7-110">**Freerepaar infoexs**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-110">**FreeRepairInfoExs**</span></span>](freerepairinfoexs.md)
-   [<span data-ttu-id="8bcf7-111">**Freerepaarinfos**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-111">**FreeRepairInfos**</span></span>](freerepairinfos.md)
-   [<span data-ttu-id="8bcf7-112">**Freerootcauseingefos**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-112">**FreeRootCauseInfos**</span></span>](freerootcauseinfos.md)
-   [<span data-ttu-id="8bcf7-113">**Freehelperattribute**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-113">**FreeHelperAttributes**</span></span>](freehelperattributes.md)
-   [<span data-ttu-id="8bcf7-114">**Freeuiinfo**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-114">**FreeUiInfo**</span></span>](freeuiinfo.md)
-   [<span data-ttu-id="8bcf7-115">**Ndfcancelincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-115">**NdfCancelIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident)
-   [<span data-ttu-id="8bcf7-116">**Ndfcloseincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-116">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
-   [<span data-ttu-id="8bcf7-117">**Ndfkreateconnectivityincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-117">**NdfCreateConnectivityIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)
-   [<span data-ttu-id="8bcf7-118">**Ndfkreatednsincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-118">**NdfCreateDNSIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)
-   [<span data-ttu-id="8bcf7-119">**Ndfkreategroupingincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-119">**NdfCreateGroupingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)
-   [<span data-ttu-id="8bcf7-120">**Ndfkreateingeboundincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-120">**NdfCreateInboundIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateinboundincident)
-   [<span data-ttu-id="8bcf7-121">**Ndfkreatabcident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-121">**NdfCreateIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)
-   [<span data-ttu-id="8bcf7-122">**Ndfkreatenetconnectionincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-122">**NdfCreateNetConnectionIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatenetconnectionincident)
-   [<span data-ttu-id="8bcf7-123">**Ndfkreatepnrpincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-123">**NdfCreatePnrpIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)
-   [<span data-ttu-id="8bcf7-124">**Ndfkreatesharingincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-124">**NdfCreateSharingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)
-   [<span data-ttu-id="8bcf7-125">**Ndfkreatewebincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-125">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
-   [<span data-ttu-id="8bcf7-126">**Ndfkreatewebincidentex**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-126">**NdfCreateWebIncidentEx**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)
-   [<span data-ttu-id="8bcf7-127">**Ndfkreatewinsockincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-127">**NdfCreateWinSockIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)
-   [<span data-ttu-id="8bcf7-128">**Ndfdiagnoseincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-128">**NdfDiagnoseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
-   [<span data-ttu-id="8bcf7-129">**Ndfexecutediagnose**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-129">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
-   [<span data-ttu-id="8bcf7-130">**Ndfgettracefile**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-130">**NdfGetTraceFile**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile)
-   [<span data-ttu-id="8bcf7-131">**Ndfrepaarincident**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-131">**NdfRepairIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident)
-   [<span data-ttu-id="8bcf7-132">**Utilassemlestringswithzuweisung**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-132">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
-   [<span data-ttu-id="8bcf7-133">**Utilloadstringwithzuordc**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-133">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
-   [<span data-ttu-id="8bcf7-134">**Utilstringcopywithzuzuweisung**</span><span class="sxs-lookup"><span data-stu-id="8bcf7-134">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)

 

 




