---
description: Schnittstellen zum Steuern eines Filter Diagramms
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Schnittstellen zum Steuern eines Filter Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747105"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="2e053-103">Schnittstellen zum Steuern eines Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="2e053-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="2e053-104">Diese Schnittstellen stellen Methoden zum Steuern eines Filter Diagramms bereit.</span><span class="sxs-lookup"><span data-stu-id="2e053-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="2e053-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2e053-105">Interface</span></span>                                  | <span data-ttu-id="2e053-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e053-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e053-107">**Iamclock-Anpassung**</span><span class="sxs-lookup"><span data-stu-id="2e053-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="2e053-108">Passen Sie die Diagramm Uhr an.</span><span class="sxs-lookup"><span data-stu-id="2e053-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="2e053-109">**Iamgraphstreams**</span><span class="sxs-lookup"><span data-stu-id="2e053-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="2e053-110">Synchronisieren von Livestreams in einem Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="2e053-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="2e053-111">**Ifilterchain**</span><span class="sxs-lookup"><span data-stu-id="2e053-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="2e053-112">Steuerungs Ketten von Filtern.</span><span class="sxs-lookup"><span data-stu-id="2e053-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="2e053-113">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="2e053-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="2e053-114">Ausführen, anhalten und Anhalten des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="2e053-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="2e053-115">(Bietet auch Automatisierungs kompatible Methoden zum Entwickeln von Diagrammen.)</span><span class="sxs-lookup"><span data-stu-id="2e053-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="2e053-116">**Imediaeventex**</span><span class="sxs-lookup"><span data-stu-id="2e053-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="2e053-117">Reagieren auf Ereignisse im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="2e053-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="2e053-118">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="2e053-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="2e053-119">Suchen Sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2e053-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="2e053-120">**Iqueuecommand**</span><span class="sxs-lookup"><span data-stu-id="2e053-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="2e053-121">Warteschlangen Befehle, die zu einem späteren Zeitpunkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2e053-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="2e053-122">**Ivideoframestep**</span><span class="sxs-lookup"><span data-stu-id="2e053-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="2e053-123">Frame: Durchlaufen eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="2e053-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



