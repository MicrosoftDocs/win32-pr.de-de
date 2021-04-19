---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Dynamischer Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357052"
---
# <a name="dynamic-memory"></a><span data-ttu-id="dbede-103">Dynamischer Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="dbede-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="dbede-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="dbede-104">Affected Platforms</span></span>

<span data-ttu-id="dbede-105">**Clients (als virtuelle Computer ausgeführt)** -Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbede-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="dbede-106">**Server** -Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="dbede-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="dbede-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="dbede-107">Feature Impact</span></span>

 <span data-ttu-id="dbede-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="dbede-108">**Severity** - Low</span></span>  
<span data-ttu-id="dbede-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="dbede-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="dbede-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbede-110">Description</span></span>

<span data-ttu-id="dbede-111">Auf hoher Ebene ist Hyper-v dynamischer Arbeitsspeicher eine Verbesserung der Arbeitsspeicher Verwaltung für die Hyper-v-Rolle, die in Windows Server 2008 R2 SP1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dbede-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="dbede-112">Es ist für die Verwendung in der Produktion vorgesehen und ermöglicht Kunden, höhere Konsolidierungs-und VM-Dichte Verhältnisse zu erreichen, während gleichzeitig die Arbeitsspeicher Auslastung auf dem physischen Computer optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="dbede-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="dbede-113">Die statische Speicher Belegung wird reduziert, und zusätzlicher Arbeitsspeicher wird Bedarfs abhängig zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dbede-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="dbede-114">Dynamischer Arbeitsspeicher wirkt sich auf Softwareentwickler aus, die sicherstellen möchten, dass Ihre Software in einer virtuellen Computerumgebung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="dbede-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="dbede-115">Verwendungsszenario</span><span class="sxs-lookup"><span data-stu-id="dbede-115">Usage Scenario</span></span>

<span data-ttu-id="dbede-116">Es gibt zwei wichtige Verwendungs Szenarien, in denen dynamischer Arbeitsspeicher, Host seitige Anwendungen und Gast seitige Anwendungen ins Spiel kommt.</span><span class="sxs-lookup"><span data-stu-id="dbede-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="dbede-117">**Host seitige Anwendungen (Verwaltungs Tools)**</span><span class="sxs-lookup"><span data-stu-id="dbede-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="dbede-118">Alte Tools, mit denen ein neuer Windows Server 2008 R2 SP1-Server verwaltet wird, können nicht auf die neuen dynamischer Arbeitsspeicher Einstellungen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dbede-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="dbede-119">Neue WMI-APIs und Leistungsindikatoren wurden entwickelt, um die neuen dynamischer Arbeitsspeicher Einstellungen für virtuelle Hyper-V-Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dbede-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="dbede-120">Software Entwickler, die an Verwaltungs Tools arbeiten, sollten diese APIs und Leistungsindikatoren für die Verwendung mit Windows Server 2008 R2 SP1 mit installierter Hyper-V-Rolle nutzen.</span><span class="sxs-lookup"><span data-stu-id="dbede-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="dbede-121">Details zu diesen neuen APIs finden Sie [in der Dokumentation zum Hyper-V-WMI-Anbieter auf MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span><span class="sxs-lookup"><span data-stu-id="dbede-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="dbede-122">**Gast seitige Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="dbede-122">**Guest-side applications**</span></span>

<span data-ttu-id="dbede-123">Entwickler, die Software für die Verwendung in einem virtuellen Computer schreiben, der für die Verwendung dynamischer Arbeitsspeicher konfiguriert ist, müssen beachten, dass der Speicher des VM-Systems nicht mehr konstant ist.</span><span class="sxs-lookup"><span data-stu-id="dbede-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="dbede-124">Folglich sollte Ihre Anwendung Arbeitsspeicher freigeben, wenn Sie nicht mehr benötigt wird, damit andere Anwendungen die Ressource nutzen können.</span><span class="sxs-lookup"><span data-stu-id="dbede-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="dbede-125">Speicher Belegungen und Zuordnungs Zuweisungen funktionieren für Benutzer Anwendungen weiterhin normal.</span><span class="sxs-lookup"><span data-stu-id="dbede-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="dbede-126">Dynamischer Arbeitsspeicher ist für die meisten Endbenutzer Anwendungen vollständig transparent.</span><span class="sxs-lookup"><span data-stu-id="dbede-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="dbede-127">Wenn die entwickelte Software jedoch Arbeitsspeicher-Leistungsindikatoren auf dem virtuellen Computer nutzt, sollten Sie in einer dynamischer Arbeitsspeicher aktivierten Umgebung sorgfältige Tests durchführen, um sicherzustellen, dass die Software die an der Arbeitsspeicher Belegung des Gast Betriebssystems vorgenommenen Änderungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="dbede-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="dbede-128">Der verfügbare Arbeitsspeicher ist nicht mehr "statisch" aus der Perspektive der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="dbede-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="dbede-129">Lösungen</span><span class="sxs-lookup"><span data-stu-id="dbede-129">Solutions</span></span>

<span data-ttu-id="dbede-130">Auf virtuellen Computern muss eine aktualisierte Integration Services (SP1) installiert sein, damit Sie von dynamischer Arbeitsspeicher profitieren können.</span><span class="sxs-lookup"><span data-stu-id="dbede-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="dbede-131">Stellen Sie sicher, dass alle Computer, die bei der Verwaltung von virtuellen Hyper-V-Computern verwendet werden, die neuesten Windows Server 2008 R2 SP1-Bits verwenden.</span><span class="sxs-lookup"><span data-stu-id="dbede-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="dbede-132">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbede-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="dbede-133">Dynamischer Arbeitsspeicher des Hyper-V-Blogs</span><span class="sxs-lookup"><span data-stu-id="dbede-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="dbede-134">Verwenden des Hyper-V-WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="dbede-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="dbede-135">Haftungsausschluss</span><span class="sxs-lookup"><span data-stu-id="dbede-135">Disclaimer</span></span>

<span data-ttu-id="dbede-136">Die in diesem Dokument enthaltenen Informationen beziehen sich auf vorab Softwareprodukte, die vor der ersten kommerziellen Version erheblich geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dbede-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="dbede-137">Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Freigabe nicht exakt beschreiben oder widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="dbede-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="dbede-138">Dieses Dokument dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="dbede-138">This document is for informational purposes only.</span></span> <span data-ttu-id="dbede-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="dbede-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
