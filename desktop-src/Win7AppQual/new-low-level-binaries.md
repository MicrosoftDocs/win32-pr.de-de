---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Neue Low-Level-Binärdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217412"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="7caad-103">Neue Low-Level-Binärdateien</span><span class="sxs-lookup"><span data-stu-id="7caad-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="7caad-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="7caad-104">Affected Platforms</span></span>

<span data-ttu-id="7caad-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="7caad-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7caad-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7caad-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="7caad-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="7caad-107">Feature Impact</span></span>

<span data-ttu-id="7caad-108">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="7caad-108">**Severity** - Medium</span></span>  
<span data-ttu-id="7caad-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="7caad-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="7caad-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7caad-110">Description</span></span>

<span data-ttu-id="7caad-111">Um die interne Entwicklungseffizienz zu verbessern und die Grundlagen für zukünftige arbeiten zu verbessern, haben wir einige Funktionen in neue Low-Level-Binärdateien verlagert.</span><span class="sxs-lookup"><span data-stu-id="7caad-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="7caad-112">Dieses Refactoring ermöglicht die zukünftige Installation von Windows, um Teilmengen von Funktionen zur Reduzierung der Oberfläche (Datenträger-und Arbeitsspeicher Anforderungen, Wartung und Angriffsfläche) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7caad-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="7caad-113">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="7caad-113">Manifestation of Impact</span></span>

<span data-ttu-id="7caad-114">Als Beispiel für Funktionen, die in Binärdateien auf niedriger Ebene verschoben wurden, kernelbase.dll die Funktionalität von kernel32.dll und advapi32.dll abrufen.</span><span class="sxs-lookup"><span data-stu-id="7caad-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="7caad-115">Dies bedeutet, dass die vorhandene Binärdatei jetzt Aufrufe an die neue Binärdatei weiterleitet, anstatt Sie direkt zu verarbeiten. die Weiterleitung kann statisch sein (die Export Tabelle zeigt die Umleitung), oder die Laufzeit (die dll verfügt über eine Stub-Routine, die die neue Binärdatei aufruft).</span><span class="sxs-lookup"><span data-stu-id="7caad-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="7caad-116">Dies wirkt sich auf Low-Level-Anwendungen wie z. b. Sicherheits-und Sicherungs Anwendungen aus, die von internen APIs und Offsets abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="7caad-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="7caad-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="7caad-117">Solution</span></span>

<span data-ttu-id="7caad-118">Der einzige Untergrund ist der Code, der Annahmen trifft, wenn versucht wird, die kernel32.dll oder die advapi32.dll Export Tabelle im Speicher zu untersuchen, z. b. eine Antivirussoftware.</span><span class="sxs-lookup"><span data-stu-id="7caad-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="7caad-119">Verwenden Sie veröffentlichte APIs und nicht die Details Ihrer Implementierung.</span><span class="sxs-lookup"><span data-stu-id="7caad-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="7caad-120">Dies ist nur ein Beispiel für die Implementierung von Implementierungsdetails für eine API.</span><span class="sxs-lookup"><span data-stu-id="7caad-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



