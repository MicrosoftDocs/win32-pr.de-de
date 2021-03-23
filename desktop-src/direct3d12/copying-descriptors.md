---
title: Kopieren von Deskriptoren
description: Die ID3D12Device copydescriptors-Methode und die ID3D12Device copydescriptorssimple-Methode auf der Geräteschnittstelle verwenden die CPU, um die Deskriptoren sofort zu kopieren.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104555"
---
# <a name="copying-descriptors"></a><span data-ttu-id="a33b2-103">Kopieren von Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a33b2-103">Copying Descriptors</span></span>

<span data-ttu-id="a33b2-104">Die [**ID3D12Device:: copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) -Methode und die [**ID3D12Device:: copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) -Methode auf der Geräteschnittstelle verwenden die CPU zum sofortigen Kopieren von Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="a33b2-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="a33b2-105">Sie können als frei Thread bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge durchführen.</span><span class="sxs-lookup"><span data-stu-id="a33b2-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="a33b2-106">Sofortiges Kopieren von Deskriptoren (CPU-Zeitachse)</span><span class="sxs-lookup"><span data-stu-id="a33b2-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="a33b2-107">Die Anzahl der Quell Deskriptoren (aus der kopiert werden soll), die als Satz von Deskriptorbereichen angegeben werden, muss gleich der Anzahl der Ziel Deskriptoren (zum Kopieren in) sein, die als separater Satz von Deskriptorbereichen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a33b2-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="a33b2-108">Die Quell-und Zielbereiche müssen andernfalls nicht in der Zeile angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a33b2-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="a33b2-109">Beispielsweise könnte eine Reihe von Deskriptoren mit geringer Dichte in ein zusammenhängendes Ziel kopiert werden, umgekehrt oder in einer Kombination.</span><span class="sxs-lookup"><span data-stu-id="a33b2-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="a33b2-110">Es können mehrere deskriptorheaps an dem Kopiervorgang beteiligt sein, sowohl als Quelle als auch als Ziel.</span><span class="sxs-lookup"><span data-stu-id="a33b2-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="a33b2-111">Die Verwendung von Deskriptorhandles als Parameter bedeutet, dass die Kopiermethoden nicht darauf achten, welche Heaps ein bestimmter Deskriptor ist – es handelt sich lediglich um Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a33b2-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="a33b2-112">Die deskriptorheap-Typen, von denen und in kopiert werden, müssen abgeglichen werden, sodass die-Methoden einen einzelnen deskriptorheap als Eingabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="a33b2-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="a33b2-113">Der Treiber muss den heaptyp aller Deskriptoren im angegebenen Kopiervorgang kennen, damit er weiß, welche Datenmenge an dem Kopiervorgang beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="a33b2-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="a33b2-114">Der Treiber muss möglicherweise auch benutzerdefinierte Kopiervorgänge durchführen, wenn er von einem bestimmten deskriptorheap verlangt wird – ein Implementierungsdetail.</span><span class="sxs-lookup"><span data-stu-id="a33b2-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="a33b2-115">Beachten Sie, dass die Deskriptorhandles selbst nicht ermitteln, auf welchen Typ Sie verweisen. Daher ist ein zusätzlicher Parameter für den Kopiervorgang erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a33b2-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="a33b2-116">Eine Alternative API zu [**copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) wird für den einfachen Fall bereitgestellt, dass ein einzelner Bereich von Deskriptoren von einem Speicherort in einen anderen kopiert wird – [**copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="a33b2-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="a33b2-117">Für diese gerätebasierten Methoden zum Kopieren von Deskriptoren (CPU-Zeitachse) müssen Quell Deskriptoren von einem sichtbaren deskriptorheap für nicht-Shader stammen.</span><span class="sxs-lookup"><span data-stu-id="a33b2-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="a33b2-118">Die Ziel Deskriptoren können sich in jedem deskriptorheap befinden, der CPU-sichtbar ist (Shader ist sichtbar oder nicht).</span><span class="sxs-lookup"><span data-stu-id="a33b2-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a33b2-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a33b2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a33b2-120">Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="a33b2-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




