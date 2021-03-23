---
title: Speicherverwaltung in Direct3D 12
description: Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicher Residenz.
ms.assetid: 94D47EBB-8060-49F6-A1FF-8B7B98AD5363
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037a2d75adcde6ff03adf2ccee8ce30d33d090c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103400"
---
# <a name="memory-management-in-direct3d-12"></a><span data-ttu-id="c9f9e-103">Speicherverwaltung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="c9f9e-103">Memory Management in Direct3D 12</span></span>

<span data-ttu-id="c9f9e-104">Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicher Residenz.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-104">Moving to D3D12 involves doing proper synchronization and management of memory residency.</span></span> <span data-ttu-id="c9f9e-105">Das Verwalten der Speicher Residenz bedeutet, dass noch mehr Synchronisierungen ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-105">Managing memory residency means even more synchronization must be done.</span></span> <span data-ttu-id="c9f9e-106">In diesem Abschnitt werden die Strategien für die Speicherverwaltung und die unter Zuordnung von Heaps und Puffern behandelt.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-106">This section covers memory management strategies, and suballocation within heaps and buffers.</span></span>

-   [<span data-ttu-id="c9f9e-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c9f9e-107">In this section</span></span>](#in-this-section)
-   [<span data-ttu-id="c9f9e-108">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c9f9e-108">Related topics</span></span>](#related-topics)

## <a name="in-this-section"></a><span data-ttu-id="c9f9e-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c9f9e-109">In this section</span></span>



| <span data-ttu-id="c9f9e-110">Thema</span><span class="sxs-lookup"><span data-stu-id="c9f9e-110">Topic</span></span>                                                                       | <span data-ttu-id="c9f9e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9f9e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9f9e-112">Strategien für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="c9f9e-112">Memory Management Strategies</span></span>](memory-management-strategies.md)<br/> | <span data-ttu-id="c9f9e-113">Ein Speicher-Manager für Direct3D 12 kann mit allen unterstützten Unterstützungs Ebenen, für UMA-oder diskrete (nicht-UMA-) Adapter und mit einer beträchtlichen Bandbreite an Architektur Unterschiede zwischen GPU-Adaptern sehr kompliziert werden.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-113">A memory manager for Direct3D 12 could get very complicated quickly with all the different tiers of support, for UMA or discreet (non-UMA) adapters, and with a considerable range of architecture differences between GPU adapters.</span></span><br/> <span data-ttu-id="c9f9e-114">Die empfohlene Strategie für die Direct3D 12-Speicherverwaltung, die in diesem Abschnitt beschrieben wird, ist "klassifizieren, Budget und Stream".</span><span class="sxs-lookup"><span data-stu-id="c9f9e-114">The recommended strategy for Direct3D 12 memory management , described in this section, is "classify, budget and stream".</span></span><br/> |
| [<span data-ttu-id="c9f9e-115">Untergeordnete Zuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="c9f9e-115">Suballocation Within Buffers</span></span>](large-buffers.md)<br/>                | <span data-ttu-id="c9f9e-116">Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-116">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="c9f9e-117">In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-117">This section covers four common scenarios for the use and management of resources and buffers.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="c9f9e-118">Untergeordnete Zuordnung innerhalb von Heaps</span><span class="sxs-lookup"><span data-stu-id="c9f9e-118">Suballocation Within Heaps</span></span>](suballocation-within-heaps.md)<br/>     | <span data-ttu-id="c9f9e-119">Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back).</span><span class="sxs-lookup"><span data-stu-id="c9f9e-119">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span> <br/>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="c9f9e-120">Aufenthaltes</span><span class="sxs-lookup"><span data-stu-id="c9f9e-120">Residency</span></span>](residency.md)<br/>                                       | <span data-ttu-id="c9f9e-121">Ein Objekt gilt als *residente* , wenn es von der GPU zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="c9f9e-121">An object is considered to be *resident* when it is accessible by the GPU.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="c9f9e-122">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c9f9e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9f9e-123">Direct3D 12-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="c9f9e-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="c9f9e-124">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="c9f9e-124">Resource Binding</span></span>](resource-binding.md)
</dt> </dl>

 

 





