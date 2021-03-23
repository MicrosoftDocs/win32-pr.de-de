---
title: Untergeordnete Zuordnung innerhalb von Heaps
description: Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back).
ms.assetid: 7E319BCF-FF3F-43CB-9C48-A9DD2A043592
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701e68e31e698bbf2c955a252bd46876f45d6b7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103485"
---
# <a name="suballocation-within-heaps"></a><span data-ttu-id="9aa6d-103">Untergeordnete Zuordnung innerhalb von Heaps</span><span class="sxs-lookup"><span data-stu-id="9aa6d-103">Suballocation Within Heaps</span></span>

<span data-ttu-id="9aa6d-104">Ressourcen Heaps übertragen Daten von der CPU auf die GPU (Upload) und von der GPU zur CPU (Read Back).</span><span class="sxs-lookup"><span data-stu-id="9aa6d-104">Resource heaps transfer data from the CPU to the GPU (upload), and from the GPU to the CPU (read back).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9aa6d-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9aa6d-105">In this section</span></span>



| <span data-ttu-id="9aa6d-106">Thema</span><span class="sxs-lookup"><span data-stu-id="9aa6d-106">Topic</span></span>                                                                                       | <span data-ttu-id="9aa6d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9aa6d-107">Description</span></span>                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aa6d-108">Speicher Aliasing und Datenvererbung</span><span class="sxs-lookup"><span data-stu-id="9aa6d-108">Memory Aliasing and Data Inheritance</span></span>](memory-aliasing-and-data-inheritance.md)<br/> | <span data-ttu-id="9aa6d-109">Die platzierte und die reservierte Ressource können den physischen Speicher innerhalb eines Heaps als Alias.</span><span class="sxs-lookup"><span data-stu-id="9aa6d-109">Placed and reserved resource may alias physical memory within a heap.</span></span> <span data-ttu-id="9aa6d-110">Platzierte Ressourcen ermöglichen mehr Daten Vererbungs Szenarien als reservierte Ressourcen, wenn für den Heap das Shared-Flag festgelegt wurde oder wenn die Aliasing-Ressourcen vollständig definierte Speicher Layouts aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9aa6d-110">Placed resources enable more data inheritance scenarios than reserved resources when the heap has the shared flag set or when the aliased resources have fully defined memory layouts.</span></span> <br/> |
| [<span data-ttu-id="9aa6d-111">Freigegebene Heaps</span><span class="sxs-lookup"><span data-stu-id="9aa6d-111">Shared Heaps</span></span>](shared-heaps.md)<br/>                                                 | <span data-ttu-id="9aa6d-112">Die Freigabe eignet sich für Multiprozess-und multiadapterarchitekturen.</span><span class="sxs-lookup"><span data-stu-id="9aa6d-112">Sharing is useful for multi-process and multi-adapter architectures.</span></span><br/>                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="9aa6d-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9aa6d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa6d-114">**ID3D12Device:: kreateheap**</span><span class="sxs-lookup"><span data-stu-id="9aa6d-114">**ID3D12Device::CreateHeap**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap)
</dt> <dt>

[<span data-ttu-id="9aa6d-115">**ID3D12Heap**</span><span class="sxs-lookup"><span data-stu-id="9aa6d-115">**ID3D12Heap**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[<span data-ttu-id="9aa6d-116">Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="9aa6d-116">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





