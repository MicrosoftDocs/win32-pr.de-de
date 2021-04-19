---
description: Was wird repliziert?
ms.assetid: d1f0bc92-37bc-4de2-876a-e6b8b09da58d
title: Was wird repliziert?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2739cb0ff615ddc38f30a7aa9b0a572be5e28a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342768"
---
# <a name="what-gets-replicated"></a><span data-ttu-id="567f7-103">Was wird repliziert?</span><span class="sxs-lookup"><span data-stu-id="567f7-103">What Gets Replicated</span></span>

## <a name="applications"></a><span data-ttu-id="567f7-104">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="567f7-104">Applications</span></span>

<span data-ttu-id="567f7-105">Alle auf dem Quellcomputer installierten Anwendungen werden mit Ausnahme der folgenden repliziert:</span><span class="sxs-lookup"><span data-stu-id="567f7-105">All applications installed on the source computer are replicated except for the following:</span></span>

<dl> <dt>

<span data-ttu-id="567f7-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Nicht-com +-Anwendungs Elemente und-Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="567f7-106"><span id="Non-COM__application_elements_and_dependencies"></span><span id="non-com__application_elements_and_dependencies"></span><span id="NON-COM__APPLICATION_ELEMENTS_AND_DEPENDENCIES"></span>Non-COM+ application elements and dependencies</span></span>
</dt> <dd>

<span data-ttu-id="567f7-107">Der Administrator ist dafür verantwortlich, alle Elemente zu replizieren, von denen eine COM+-Anwendung abhängt, die jedoch nicht ordnungsgemäß Teil der Anwendung selbst ist, wie z. b. Datendateien und DLLs.</span><span class="sxs-lookup"><span data-stu-id="567f7-107">The administrator is responsible for replicating anything that a COM+ application depends on but which is not properly part of the application itself, such as data files and DLLs.</span></span> <span data-ttu-id="567f7-108">Comrepl repliziert nichts außerhalb der com+-Anwendungs Elemente.</span><span class="sxs-lookup"><span data-stu-id="567f7-108">COMREPL will not replicate anything outside of COM+ application elements.</span></span>

</dd> <dt>

<span data-ttu-id="567f7-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>Vorinstallierte com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="567f7-109"><span id="COM__preinstalled_applications"></span><span id="com__preinstalled_applications"></span><span id="COM__PREINSTALLED_APPLICATIONS"></span>COM+ preinstalled applications</span></span>
</dt> <dd>

<span data-ttu-id="567f7-110">Anwendungen, die intern von com+ verwendet werden und über das com+-Setup Programm installiert werden, werden nicht repliziert.</span><span class="sxs-lookup"><span data-stu-id="567f7-110">Applications that are used internally by COM+ and are installed via the COM+ setup program are not replicated.</span></span> <span data-ttu-id="567f7-111">Dabei handelt es sich z. B. um:</span><span class="sxs-lookup"><span data-stu-id="567f7-111">These include the following:</span></span>

-   <span data-ttu-id="567f7-112">System Anwendung</span><span class="sxs-lookup"><span data-stu-id="567f7-112">System application</span></span>
-   <span data-ttu-id="567f7-113">Com+-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="567f7-113">COM+ utilities</span></span>
-   <span data-ttu-id="567f7-114">Anqueue-Listener für com+-QC</span><span class="sxs-lookup"><span data-stu-id="567f7-114">COM+ QC Dead Letter Queue Listener</span></span>

</dd> <dt>

<span data-ttu-id="567f7-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Von IIS erstellte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="567f7-115"><span id="Applications_created_by_IIS"></span><span id="applications_created_by_iis"></span><span id="APPLICATIONS_CREATED_BY_IIS"></span>Applications created by IIS</span></span>
</dt> <dd>

<span data-ttu-id="567f7-116">Diese Anwendungen werden nicht repliziert und umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="567f7-116">These applications are not replicated and include the following:</span></span>

-   <span data-ttu-id="567f7-117">IIS-in-Process-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="567f7-117">IIS in-process applications</span></span>
-   <span data-ttu-id="567f7-118">IIS-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="567f7-118">IIS utilities</span></span>
-   <span data-ttu-id="567f7-119">Alle Anwendungen, die für isolierte oder gepoolte virtuelle Stämme erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="567f7-119">All applications created for isolated or pooled virtual roots</span></span>

</dd> </dl>

## <a name="computer-list"></a><span data-ttu-id="567f7-120">Computer Liste</span><span class="sxs-lookup"><span data-stu-id="567f7-120">Computer List</span></span>

<span data-ttu-id="567f7-121">Die Remote Computer, die im Ordner " **Computer** " im Verwaltungs Tool "Komponenten Dienste" genannt werden, werden nicht von der Quell-auf den Zielcomputer repliziert.</span><span class="sxs-lookup"><span data-stu-id="567f7-121">The remote computers named in the **Computers** folder in the Component Services administration tool will not be replicated from source to target computer.</span></span>

## <a name="properties"></a><span data-ttu-id="567f7-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="567f7-122">Properties</span></span>

<span data-ttu-id="567f7-123">Die folgenden **LocalComputer** -Sammlungs Eigenschaften werden repliziert:</span><span class="sxs-lookup"><span data-stu-id="567f7-123">The following **LocalComputer** collection properties are replicated:</span></span>

-   <span data-ttu-id="567f7-124">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="567f7-124">TransactionTimeout</span></span>
-   <span data-ttu-id="567f7-125">Resourcepoolingenabled</span><span class="sxs-lookup"><span data-stu-id="567f7-125">ResourcePoolingEnabled</span></span>
-   <span data-ttu-id="567f7-126">Dcomaktiviert</span><span class="sxs-lookup"><span data-stu-id="567f7-126">DCOMEnabled</span></span>
-   <span data-ttu-id="567f7-127">DefaultAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="567f7-127">DefaultAuthenticationLevel</span></span>
-   <span data-ttu-id="567f7-128">DefaultImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="567f7-128">DefaultImpersonationLevel</span></span>
-   <span data-ttu-id="567f7-129">Securitytrackingenabled</span><span class="sxs-lookup"><span data-stu-id="567f7-129">SecurityTrackingEnabled</span></span>
-   <span data-ttu-id="567f7-130">Cisenabled</span><span class="sxs-lookup"><span data-stu-id="567f7-130">CISEnabled</span></span>
-   <span data-ttu-id="567f7-131">Securereferencesaktiviert</span><span class="sxs-lookup"><span data-stu-id="567f7-131">SecureReferencesEnabled</span></span>
-   <span data-ttu-id="567f7-132">Internetportslisted</span><span class="sxs-lookup"><span data-stu-id="567f7-132">InternetPortsListed</span></span>
-   <span data-ttu-id="567f7-133">Deafulttinternetports</span><span class="sxs-lookup"><span data-stu-id="567f7-133">DeafultToInternetPorts</span></span>
-   <span data-ttu-id="567f7-134">Ports</span><span class="sxs-lookup"><span data-stu-id="567f7-134">Ports</span></span>
-   <span data-ttu-id="567f7-135">Rpcproxyaktivierte</span><span class="sxs-lookup"><span data-stu-id="567f7-135">RpcProxyEnabled</span></span>

<span data-ttu-id="567f7-136">Die folgenden **LocalComputer** -Sammlungs Eigenschaften werden nicht repliziert:</span><span class="sxs-lookup"><span data-stu-id="567f7-136">The following **LocalComputer** collection properties are not replicated:</span></span>

-   <span data-ttu-id="567f7-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="567f7-137">Description</span></span>
-   <span data-ttu-id="567f7-138">Applicationproxyrsn</span><span class="sxs-lookup"><span data-stu-id="567f7-138">ApplicationProxyRSN</span></span>
-   <span data-ttu-id="567f7-139">Isrouter</span><span class="sxs-lookup"><span data-stu-id="567f7-139">IsRouter</span></span>

<span data-ttu-id="567f7-140">Beschreibungen der Eigenschaften der **LocalComputer** -Sammlung finden Sie unter [**LocalComputer**](localcomputer.md).</span><span class="sxs-lookup"><span data-stu-id="567f7-140">For descriptions of the **LocalComputer** collection properties, see [**LocalComputer**](localcomputer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="567f7-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="567f7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="567f7-142">Dateiverwaltung</span><span class="sxs-lookup"><span data-stu-id="567f7-142">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="567f7-143">Protokollierung und Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="567f7-143">Logging and Error Reporting</span></span>](logging-and-error-reporting.md)
</dt> <dt>

[<span data-ttu-id="567f7-144">Replikations Phasen</span><span class="sxs-lookup"><span data-stu-id="567f7-144">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="567f7-145">Verwenden von Comrepl</span><span class="sxs-lookup"><span data-stu-id="567f7-145">Using COMREPL</span></span>](using-comrepl.md)
</dt> </dl>

 

 



