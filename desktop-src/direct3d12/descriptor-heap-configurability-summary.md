---
title: Deskriptorheap-Konfigurations Zusammenfassung
description: In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103571"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="2c7c2-103">Deskriptorheap-Konfigurations Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2c7c2-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="2c7c2-104">In der folgenden Tabelle werden Informationen zur Unterstützung von Shader und nicht-Shader-sichtbarem Heap zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="2c7c2-105">Shader-sichtbarer deskriptorheap</span><span class="sxs-lookup"><span data-stu-id="2c7c2-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="2c7c2-106">Sichtbarer deskriptorheap für nicht-Shader</span><span class="sxs-lookup"><span data-stu-id="2c7c2-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7c2-107">Unterstützte Heap Typen</span><span class="sxs-lookup"><span data-stu-id="2c7c2-107">Heap Types Supported</span></span>          | <span data-ttu-id="2c7c2-108">CBV \_ SRV \_ UAV, Sampler</span><span class="sxs-lookup"><span data-stu-id="2c7c2-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="2c7c2-109">Alle</span><span class="sxs-lookup"><span data-stu-id="2c7c2-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2c7c2-110">Unterstützte CPU-Seiteneigenschaften</span><span class="sxs-lookup"><span data-stu-id="2c7c2-110">CPU Page Properties Supported</span></span> | <span data-ttu-id="2c7c2-111">nicht \_ verfügbar, schreiben \_ kombinieren</span><span class="sxs-lookup"><span data-stu-id="2c7c2-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="2c7c2-112">\_Zurückschreiben</span><span class="sxs-lookup"><span data-stu-id="2c7c2-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2c7c2-113">Residenz Verwaltung nach App</span><span class="sxs-lookup"><span data-stu-id="2c7c2-113">Residency Management By App</span></span>   | <span data-ttu-id="2c7c2-114">Ja, App Verantwortlichkeit</span><span class="sxs-lookup"><span data-stu-id="2c7c2-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="2c7c2-115">Nicht zutreffend (nicht GPU-sichtbar).</span><span class="sxs-lookup"><span data-stu-id="2c7c2-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2c7c2-116">Unterstützung für deskriptorbearbeitung</span><span class="sxs-lookup"><span data-stu-id="2c7c2-116">Descriptor Edit Support</span></span>       | <span data-ttu-id="2c7c2-117">Nur Ziel kopieren, über die Befehlsliste aktualisieren und/oder CPU-Kopie, wenn CPU sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="2c7c2-118">Nur CPU-Lese-und Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-118">CPU read and write only.</span></span> <span data-ttu-id="2c7c2-119">Kein direkter GPU-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-119">No direct GPU access.</span></span> <span data-ttu-id="2c7c2-120">Kann zum sofortigen Kopieren von CPU (als Quelle und Ziel) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="2c7c2-121">Kann in einer Befehlsliste als Update Quelle verwendet werden – dadurch werden die Deskriptoren im Befehlslisten Daten Satz in den Befehlslisten Speicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="2c7c2-122">Bei der Ausführung wird die gespeicherte Kopie in das Ziel kopiert, bei dem es sich um einen für Shader sichtbaren Heap handeln muss.</span><span class="sxs-lookup"><span data-stu-id="2c7c2-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2c7c2-123">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2c7c2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c7c2-124">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="2c7c2-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




