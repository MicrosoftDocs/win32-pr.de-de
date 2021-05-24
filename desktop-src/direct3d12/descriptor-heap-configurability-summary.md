---
title: Zusammenfassung der Deskriptorheap-Konfigurierbarkeit
description: In der folgenden Tabelle sind Informationen zur Unterstützung von shader- und nicht shader-sichtbaren Heaps zusammengefasst.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335568"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="390ee-103">Zusammenfassung der Deskriptorheap-Konfigurierbarkeit</span><span class="sxs-lookup"><span data-stu-id="390ee-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="390ee-104">In der folgenden Tabelle sind Informationen zur Unterstützung von shader- und nicht shader-sichtbaren Heaps zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="390ee-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="390ee-105">Shader Visible Descriptor Heap</span><span class="sxs-lookup"><span data-stu-id="390ee-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="390ee-106">Nicht shader sichtbarer Deskriptor-Heap</span><span class="sxs-lookup"><span data-stu-id="390ee-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="390ee-107">**Unterstützte Heaptypen**</span><span class="sxs-lookup"><span data-stu-id="390ee-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="390ee-108">CBV \_ SRV \_ UAV, Sampler</span><span class="sxs-lookup"><span data-stu-id="390ee-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="390ee-109">Alle</span><span class="sxs-lookup"><span data-stu-id="390ee-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="390ee-110">**Unterstützte CPU-Seiteneigenschaften**</span><span class="sxs-lookup"><span data-stu-id="390ee-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="390ee-111">NICHT \_ VERFÜGBAR, WRITE \_ COMBINE</span><span class="sxs-lookup"><span data-stu-id="390ee-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="390ee-112">\_ZURÜCKSCHREIBEN</span><span class="sxs-lookup"><span data-stu-id="390ee-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="390ee-113">**Verwaltung von Residencys nach App**</span><span class="sxs-lookup"><span data-stu-id="390ee-113">**Residency Management By App**</span></span>   | <span data-ttu-id="390ee-114">Ja, app responsible</span><span class="sxs-lookup"><span data-stu-id="390ee-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="390ee-115">Nicht zutreffend (nicht gpu-sichtbar).</span><span class="sxs-lookup"><span data-stu-id="390ee-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="390ee-116">**Unterstützung für Deskriptorbearbeitung**</span><span class="sxs-lookup"><span data-stu-id="390ee-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="390ee-117">Nur Ziel kopieren, über Befehlslistenaktualisierung und/oder CPU-Kopie, wenn CPU sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="390ee-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="390ee-118">Nur CPU-Lese- und -Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="390ee-118">CPU read and write only.</span></span> <span data-ttu-id="390ee-119">Kein direkter GPU-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="390ee-119">No direct GPU access.</span></span> <span data-ttu-id="390ee-120">Kann zum sofortigen Kopieren von CPUs (als Quelle und Ziel) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="390ee-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="390ee-121">Kann als Updatequelle für eine Befehlsliste verwendet werden. Dadurch werden die Deskriptoren während des Befehlslisten-Eintrags in den Befehlslistenspeicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="390ee-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="390ee-122">Bei der Ausführung wird die gespeicherte Kopie in das Ziel kopiert, bei dem es sich um einen shader sichtbaren Heap geben muss.</span><span class="sxs-lookup"><span data-stu-id="390ee-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="390ee-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="390ee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="390ee-124">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="390ee-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




