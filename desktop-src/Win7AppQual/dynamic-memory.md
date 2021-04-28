---
description: Dynamischer Arbeitsspeicher
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Dynamischer Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088468"
---
# <a name="dynamic-memory"></a><span data-ttu-id="dad10-103">Dynamischer Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="dad10-103">Dynamic Memory</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="dad10-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="dad10-104">Affected Platforms</span></span>

<span data-ttu-id="dad10-105">**Clients (als virtuelle Computer ausgeführt)** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="dad10-105">**Clients (running as virtual machines)** - Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="dad10-106">**Server** – Windows Server 2008 R2 Hyper-V SP1</span><span class="sxs-lookup"><span data-stu-id="dad10-106">**Servers** - Windows Server 2008 R2 Hyper-V SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="dad10-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="dad10-107">Feature Impact</span></span>

 <span data-ttu-id="dad10-108">**Schweregrad:** Niedrig</span><span class="sxs-lookup"><span data-stu-id="dad10-108">**Severity** - Low</span></span>  
<span data-ttu-id="dad10-109">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="dad10-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="dad10-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dad10-110">Description</span></span>

<span data-ttu-id="dad10-111">Auf hoher Ebene ist Hyper-V-Dynamischer Arbeitsspeicher eine Speicherverwaltungserweiterung für die Hyper-V-Rolle, die in Windows Server 2008 R2 SP1 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dad10-111">At a high level, Hyper-V Dynamic Memory is a memory management enhancement for the Hyper-V role included in Windows Server 2008 R2 SP1.</span></span> <span data-ttu-id="dad10-112">Es ist für den Einsatz in der Produktion konzipiert und ermöglicht Es Kunden, ein höheres Konsolidierungs-/VM-Dichteverhältnis zu erzielen und gleichzeitig die Arbeitsspeicherauslastung auf dem physischen Computer zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="dad10-112">It is designed for production use and enables customers to achieve higher consolidation/virtual machine (VM) density ratios while optimizing the memory utilization in the physical machine.</span></span> <span data-ttu-id="dad10-113">Die statische Speicherzuweisung wird reduziert, und bei Bedarf wird zusätzlicher Arbeitsspeicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dad10-113">The static memory allocation is reduced and additional memory is allocated on an as needed basis.</span></span> <span data-ttu-id="dad10-114">Dynamischer Arbeitsspeicher auswirkungen auf Softwareentwickler, die sicherstellen möchten, dass ihre Software in einer Umgebung eines virtuellen Computers ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="dad10-114">Dynamic Memory impacts software developers who want to ensure that their software works correctly in a virtual machine environment.</span></span>

## <a name="usage-scenario"></a><span data-ttu-id="dad10-115">Verwendungsszenario</span><span class="sxs-lookup"><span data-stu-id="dad10-115">Usage Scenario</span></span>

<span data-ttu-id="dad10-116">Es gibt zwei wichtige Verwendungsszenarien, Dynamischer Arbeitsspeicher ins Spiel kommen: hostseitige Anwendungen und gastseitige Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="dad10-116">There are two key usage scenarios where Dynamic Memory comes into play, host-side applications and guest-side applications.</span></span>

<span data-ttu-id="dad10-117">**Hostseitige Anwendungen (Verwaltungstools)**</span><span class="sxs-lookup"><span data-stu-id="dad10-117">**Host-side applications (management tools)**</span></span>

<span data-ttu-id="dad10-118">Alte Tools, die einen neuen Windows Server 2008 R2 SP1-Server verwalten, können nicht auf die neuen Dynamischer Arbeitsspeicher zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dad10-118">Old tools managing a new Windows Server 2008 R2 SP1 server will not be able to access the new Dynamic Memory settings.</span></span> <span data-ttu-id="dad10-119">Neue WMI-APIs und Leistungsindikatoren wurden entwickelt, um die neuen Dynamischer Arbeitsspeicher für virtuelle Hyper-V-Computer zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dad10-119">New WMI APIs and performance counters have been developed to manage the new Dynamic Memory settings for Hyper-V virtual machines.</span></span> <span data-ttu-id="dad10-120">Softwareentwickler, die an Verwaltungstools arbeiten, sollten diese APIs und Leistungsindikatoren für die Verwendung mit Windows Server 2008 R2 SP1 mit installierter Hyper-V-Rolle nutzen.</span><span class="sxs-lookup"><span data-stu-id="dad10-120">Software developers working on management tools should take advantage of these APIs and counters for use with Windows Server 2008 R2 SP1 with the Hyper-V role installed.</span></span> <span data-ttu-id="dad10-121">Details zu diesen neuen APIs finden Sie in der Dokumentation zum [Hyper-V-WMI-Anbieter auf MSDN.](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dad10-121">Details about these new APIs will be available via [Hyper-V WMI Provider documentation on MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).</span></span>

<span data-ttu-id="dad10-122">**Gastseitige Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="dad10-122">**Guest-side applications**</span></span>

<span data-ttu-id="dad10-123">Entwickler, die Software für die Verwendung auf einem virtuellen Computer schreiben, der für die Verwendung von Dynamischer Arbeitsspeicher müssen bedenken, dass der Arbeitsspeicher des VM-Systems nicht mehr konstant ist.</span><span class="sxs-lookup"><span data-stu-id="dad10-123">Developers writing software for use inside a virtual machine configured to use Dynamic Memory need to keep in mind that VM system memory is no longer constant.</span></span> <span data-ttu-id="dad10-124">Daher sollte ihre Anwendung Arbeitsspeicher frei geben, wenn sie nicht mehr benötigt wird, um anderen Anwendungen die Nutzung der Ressource zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="dad10-124">Consequently, their application should free memory when it is no longer needed to allow other applications to take advantage of the resource.</span></span>

<span data-ttu-id="dad10-125">Speicherzuweisungen und Dasentlegungen funktionieren für Benutzeranwendungen weiterhin wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="dad10-125">Memory allocations and de-allocations continue to work as normal for user applications.</span></span> <span data-ttu-id="dad10-126">Dynamischer Arbeitsspeicher ist für die meisten Endbenutzeranwendungen vollständig transparent.</span><span class="sxs-lookup"><span data-stu-id="dad10-126">Dynamic Memory is completely transparent to most end user applications.</span></span> <span data-ttu-id="dad10-127">Wenn die entwickelte Software jedoch Speicherleistungsindikatoren auf dem virtuellen Computer verwendet, sollten sie in einer Dynamischer Arbeitsspeicher aktivierten Umgebung sorgfältig getestet werden, um sicherzustellen, dass die Software die Änderungen berücksichtigt, die an der Speicherbelegung des Gastbetriebssystems vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="dad10-127">However if the software being developed makes use of memory performance counters in the virtual machine then careful testing should be performed in a Dynamic Memory enabled environment to ensure that the software takes the changes that are made to the Guest operating system memory allocation into account.</span></span> <span data-ttu-id="dad10-128">Verfügbarer Arbeitsspeicher ist aus Sicht des virtuellen Computers nicht mehr "statisch".</span><span class="sxs-lookup"><span data-stu-id="dad10-128">Available memory is no longer "static" from the virtual machine?s perspective.</span></span>

## <a name="solutions"></a><span data-ttu-id="dad10-129">Lösungen</span><span class="sxs-lookup"><span data-stu-id="dad10-129">Solutions</span></span>

<span data-ttu-id="dad10-130">Auf virtuellen Computern müssen aktualisierte Integrationsdienste (SP1) installiert sein, um Dynamischer Arbeitsspeicher nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="dad10-130">Virtual machines must have updated integration services (SP1) installed in order to take advantage of Dynamic Memory.</span></span> <span data-ttu-id="dad10-131">Stellen Sie sicher, dass alle Computer, die in der Verwaltung virtueller Hyper-V-Computer verwendet werden, die neuesten Windows Server 2008 R2 SP1-Bits verwenden.</span><span class="sxs-lookup"><span data-stu-id="dad10-131">Ensure that all machines used in the management of Hyper-V virtual machines are using the latest Windows Server 2008 R2 SP1 bits.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="dad10-132">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dad10-132">Links to Other Resources</span></span>

-   [<span data-ttu-id="dad10-133">Blog zu Dynamischer Arbeitsspeicher Coming To Hyper-V</span><span class="sxs-lookup"><span data-stu-id="dad10-133">Dynamic Memory Coming To Hyper-V blog</span></span>](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [<span data-ttu-id="dad10-134">Verwenden des Hyper-V-WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="dad10-134">Using the Hyper-V WMI Provider</span></span>](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a><span data-ttu-id="dad10-135">Haftungsausschluss</span><span class="sxs-lookup"><span data-stu-id="dad10-135">Disclaimer</span></span>

<span data-ttu-id="dad10-136">Die in diesem Dokument enthaltenen Informationen beziehen sich auf vorab veröffentlichte Softwareprodukte, die vor dem ersten kommerziellen Release erheblich geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dad10-136">The information contained in this document relates to prerelease software product that may be substantially modified before its first commercial release.</span></span> <span data-ttu-id="dad10-137">Entsprechend können die Informationen das Softwareprodukt bei der ersten kommerziellen Veröffentlichung nicht genau beschreiben oder widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="dad10-137">Accordingly, the information may not accurately describe or reflect the software product when first commercially released.</span></span> <span data-ttu-id="dad10-138">Dieses Dokument dient nur zu Informationszwecken.</span><span class="sxs-lookup"><span data-stu-id="dad10-138">This document is for informational purposes only.</span></span> <span data-ttu-id="dad10-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span><span class="sxs-lookup"><span data-stu-id="dad10-139">MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.</span></span>

 

 
