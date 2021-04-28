---
description: Neue Low-Level Binärdateien
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Neue Low-Level Binärdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088068"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="64739-103">Neue Low-Level Binärdateien</span><span class="sxs-lookup"><span data-stu-id="64739-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="64739-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="64739-104">Affected Platforms</span></span>

<span data-ttu-id="64739-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="64739-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="64739-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64739-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="64739-107">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="64739-107">Feature Impact</span></span>

<span data-ttu-id="64739-108">**Schweregrad –** Mittel</span><span class="sxs-lookup"><span data-stu-id="64739-108">**Severity** - Medium</span></span>  
<span data-ttu-id="64739-109">**Häufigkeit** : Hoch</span><span class="sxs-lookup"><span data-stu-id="64739-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="64739-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64739-110">Description</span></span>

<span data-ttu-id="64739-111">Um die Interne Engineering-Effizienz zu verbessern und die Grundlagen für zukünftige Arbeit zu verbessern, haben wir einige Funktionen in neue Binärdateien auf niedriger Ebene verschoben.</span><span class="sxs-lookup"><span data-stu-id="64739-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="64739-112">Durch dieses Refactoring können zukünftige Installationen von Windows Teilmengen der Funktionalität bereitstellen, um die Oberfläche zu reduzieren (Datenträger- und Arbeitsspeicheranforderungen, Wartung und Angriffsfläche).</span><span class="sxs-lookup"><span data-stu-id="64739-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="64739-113">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="64739-113">Manifestation of Impact</span></span>

<span data-ttu-id="64739-114">Als Beispiel für die Funktionalität, die wir in Binärdateien auf niedriger Ebene verschoben haben, ruft kernelbase.dll Funktionen aus kernel32.dll und advapi32.dll ab.</span><span class="sxs-lookup"><span data-stu-id="64739-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="64739-115">Dies bedeutet, dass die vorhandene Binärdatei jetzt Aufrufe an die neue Binärdatei weiterleitet, anstatt sie direkt zu verarbeiten. Die Weiterleitung kann statisch sein (die Exporttabelle zeigt die Umleitung) oder runtime (die DLL verfügt über eine Stubroutine, die die neue Binärdatei aufruft).</span><span class="sxs-lookup"><span data-stu-id="64739-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="64739-116">Dies wirkt sich auf Low-Level-Anwendungen wie Sicherheits- und Sicherungsanwendungen aus, die von internen APIs und Offsets abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="64739-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="64739-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="64739-117">Solution</span></span>

<span data-ttu-id="64739-118">Die einzige Auswirkung ist der Code, der Annahmen trifft, wenn versucht wird, die kernel32.dll oder die advapi32.dll Exporttabelle im Arbeitsspeicher zu betrachten, z. B. eine Antivirenanwendung.</span><span class="sxs-lookup"><span data-stu-id="64739-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="64739-119">Verwenden Sie veröffentlichte APIs und nicht die Details ihrer Implementierung.</span><span class="sxs-lookup"><span data-stu-id="64739-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="64739-120">Dies ist nur ein Beispiel für die Implementierung eines Implementierungsdetails für eine API.</span><span class="sxs-lookup"><span data-stu-id="64739-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



