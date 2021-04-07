---
description: Schnittstellen zum Entwickeln von Filter Diagrammen
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Schnittstellen zum Entwickeln von Filter Diagrammen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746009"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="d8e36-103">Schnittstellen zum Entwickeln von Filter Diagrammen</span><span class="sxs-lookup"><span data-stu-id="d8e36-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="d8e36-104">Anwendungen verwenden diese Schnittstellen, um verschiedene Arten von Filter Diagrammen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8e36-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="d8e36-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8e36-105">Interface</span></span>                                                  | <span data-ttu-id="d8e36-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8e36-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="d8e36-107">**Iamfiltergraphcallback**</span><span class="sxs-lookup"><span data-stu-id="d8e36-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="d8e36-108">Empfangen von Rückruf Benachrichtigungen, wenn eine PIN nicht gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8e36-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="d8e36-109">**Iamgraphbuildercallback**</span><span class="sxs-lookup"><span data-stu-id="d8e36-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="d8e36-110">Stellt während der Diagramm Bildung einen Rückrufmechanismus bereit.</span><span class="sxs-lookup"><span data-stu-id="d8e36-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="d8e36-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="d8e36-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="d8e36-112">Buildfilterdiagramme für die Video Erfassung.</span><span class="sxs-lookup"><span data-stu-id="d8e36-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="d8e36-113">**Ikreatedevenum**</span><span class="sxs-lookup"><span data-stu-id="d8e36-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="d8e36-114">Auflisten von System Geräten, z. b. Geräte Erfassung</span><span class="sxs-lookup"><span data-stu-id="d8e36-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="d8e36-115">**Idvdgraphbuilder**</span><span class="sxs-lookup"><span data-stu-id="d8e36-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="d8e36-116">Buildfilterdiagramme für DVD-Navigation und-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="d8e36-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="d8e36-117">**Ienumfilters**</span><span class="sxs-lookup"><span data-stu-id="d8e36-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="d8e36-118">Listet die Filter im Diagramm auf.</span><span class="sxs-lookup"><span data-stu-id="d8e36-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="d8e36-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="d8e36-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="d8e36-120">Hinzufügen, entfernen oder Verbinden von Filtern.</span><span class="sxs-lookup"><span data-stu-id="d8e36-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="d8e36-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="d8e36-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="d8e36-122">Listet die auf dem System des Benutzers registrierten Filter auf.</span><span class="sxs-lookup"><span data-stu-id="d8e36-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="d8e36-123">**Igraphbuilder**</span><span class="sxs-lookup"><span data-stu-id="d8e36-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="d8e36-124">Buildfilterdiagramme für die Dateiwiedergabe oder für benutzerdefinierte Verwendungen.</span><span class="sxs-lookup"><span data-stu-id="d8e36-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="d8e36-125">**Igraphconfig**</span><span class="sxs-lookup"><span data-stu-id="d8e36-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="d8e36-126">Dynamisches Neukonfigurieren eines Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="d8e36-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="d8e36-127">**Igraphversion**</span><span class="sxs-lookup"><span data-stu-id="d8e36-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="d8e36-128">Bestimmen Sie, wann das Diagramm geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d8e36-128">Determine when the graph changes.</span></span>                           |



 

 

 



