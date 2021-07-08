---
title: Arbeitsspeicherverwaltung in Direct3D 12
description: Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b8091c2893f8906fe2ab5baadbf1288a1474cd
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481805"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="ef2f7-103">Arbeitsspeicherverwaltung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ef2f7-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="ef2f7-104">Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="ef2f7-105">Die Verwaltung der Speicherresidenz bedeutet, dass noch mehr Synchronisierung durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="ef2f7-106">In diesem Abschnitt werden Strategien für die Speicherverwaltung und die Unterzuordnung in Heaps und Puffern behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="ef2f7-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ef2f7-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="ef2f7-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ef2f7-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="ef2f7-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ef2f7-109">In this section</span></span>



| <span data-ttu-id="ef2f7-110">Thema</span><span class="sxs-lookup"><span data-stu-id="ef2f7-110">Topic</span></span>                                                                       | <span data-ttu-id="ef2f7-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef2f7-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef2f7-112">Strategien für die Arbeitsspeicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="ef2f7-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="ef2f7-113">Ein Speicher-Manager für Direct3D 12 kann sehr schnell mit allen verschiedenen Supportebenen, für UMA- oder diskrete Adapter (nicht UMA) und mit einem erheblichen Bereich von Architekturunterschieden zwischen GPU-Adaptern sehr kompliziert werden.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discrete (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="ef2f7-114">Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "Klassifizieren, Budget und Streamen".</span><span class="sxs-lookup"><span data-stu-id="ef2f7-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="ef2f7-115">Unterzuweisung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="ef2f7-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="ef2f7-116">Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="ef2f7-117">In diesem Abschnitt werden vier gängige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="ef2f7-118">Unterzuweisung innerhalb von Heaps</span><span class="sxs-lookup"><span data-stu-id="ef2f7-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="ef2f7-119">Ressourcenheaps übertragen Daten von der CPU zur GPU (Upload) und von der GPU zur CPU (zurücklesen).</span><span class="sxs-lookup"><span data-stu-id="ef2f7-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="ef2f7-120">Residenz</span><span class="sxs-lookup"><span data-stu-id="ef2f7-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="ef2f7-121">Ein Objekt gilt als *resident,* wenn es von der GPU zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="ef2f7-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="ef2f7-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef2f7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef2f7-123">Direct3D 12-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="ef2f7-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="ef2f7-124">Ressourcenbindung</span><span class="sxs-lookup"><span data-stu-id="ef2f7-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





