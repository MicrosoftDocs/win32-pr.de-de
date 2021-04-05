---
title: NAP-Hilfsprogrammfunktionen
description: Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709798"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="809f9-103">NAP-Hilfsprogrammfunktionen</span><span class="sxs-lookup"><span data-stu-id="809f9-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="809f9-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="809f9-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="809f9-105">Die folgenden Hilfsprogrammfunktionen unterstützen die NAP-API.</span><span class="sxs-lookup"><span data-stu-id="809f9-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="809f9-106">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicherzuweisung (cotaskmembelegc und CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="809f9-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="809f9-107">IN Parametern – zugewiesen und von Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="809f9-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="809f9-108">OUT-Parameter – vom aufgerufenen zugewiesen, freigegeben durch Aufrufer mit cotaskmem \* ()</span><span class="sxs-lookup"><span data-stu-id="809f9-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="809f9-109">IN/out-Parameter – vom Aufrufer zugeordnet, freigegeben und vom Aufrufer freigegeben, letztendlich mithilfe von cotaskmem \* ()</span><span class="sxs-lookup"><span data-stu-id="809f9-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="809f9-110">In den freexxx ()-Funktionen werden alle eingebetteten Zeiger ebenfalls freigegeben.</span><span class="sxs-lookup"><span data-stu-id="809f9-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="809f9-111">**Zuordnung von Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="809f9-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="809f9-112">**"Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="809f9-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="809f9-113">**Zuordnung von "Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="809f9-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="809f9-114">**Freeconnections**</span><span class="sxs-lookup"><span data-stu-id="809f9-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="809f9-115">**Freizähltedstring**</span><span class="sxs-lookup"><span data-stu-id="809f9-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="809f9-116">**"Freifixupinfo"**</span><span class="sxs-lookup"><span data-stu-id="809f9-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="809f9-117">**Freeisolationinfo**</span><span class="sxs-lookup"><span data-stu-id="809f9-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="809f9-118">**Freeisolationinfoex**</span><span class="sxs-lookup"><span data-stu-id="809f9-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="809f9-119">**Freenapcomponentregistrationinfoarray**</span><span class="sxs-lookup"><span data-stu-id="809f9-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="809f9-120">**Freumetworksoh**</span><span class="sxs-lookup"><span data-stu-id="809f9-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="809f9-121">**"Freiprivatedata"**</span><span class="sxs-lookup"><span data-stu-id="809f9-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="809f9-122">**Freesoh**</span><span class="sxs-lookup"><span data-stu-id="809f9-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="809f9-123">**Freesohattributevalue**</span><span class="sxs-lookup"><span data-stu-id="809f9-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="809f9-124">**Freesystemhealthagentstate**</span><span class="sxs-lookup"><span data-stu-id="809f9-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="809f9-125">**Initializenapagentnotifier**</span><span class="sxs-lookup"><span data-stu-id="809f9-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="809f9-126">**Uninitializenapagentnotifier**</span><span class="sxs-lookup"><span data-stu-id="809f9-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




