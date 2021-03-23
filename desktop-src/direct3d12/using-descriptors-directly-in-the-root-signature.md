---
title: Verwenden von Deskriptoren direkt in der Stammsignatur
description: Anwendungen können Deskriptoren direkt in die Stamm Signatur einfügen, um zu vermeiden, dass Sie einen deskriptorheap durchlaufen müssen.
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548742"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a><span data-ttu-id="55e25-103">Verwenden von Deskriptoren direkt in der Stammsignatur</span><span class="sxs-lookup"><span data-stu-id="55e25-103">Using descriptors directly in the root signature</span></span>

<span data-ttu-id="55e25-104">Anwendungen können Deskriptoren direkt in die Stamm Signatur einfügen, um zu vermeiden, dass Sie einen deskriptorheap durchlaufen müssen.</span><span class="sxs-lookup"><span data-stu-id="55e25-104">Applications can put descriptors directly in the root signature to avoid having to go through a descriptor heap.</span></span> <span data-ttu-id="55e25-105">Diese Deskriptoren belegen viel Platz in der Stamm Signatur (siehe den Abschnitt root Signature Limits), sodass Anwendungen Sie sparsam verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="55e25-105">These descriptors take a lot of space in the root signature (see the root signature limits section), so applications have to use them sparingly.</span></span>

<span data-ttu-id="55e25-106">Ein Beispiel für die Verwendung ist das Platzieren einer Konstanten Puffer Ansicht (Constant Buffer views, CBV), die pro zeichnen im Stamm Layout geändert wird, sodass der deskriptorheap-Speicherplatz nicht von der Anwendung pro zeichnen zugeordnet werden muss (und das verweisen auf eine Deskriptortabelle an der neuen Position im deskriptorheap gespeichert werden).</span><span class="sxs-lookup"><span data-stu-id="55e25-106">An example usage would be to place a constant buffer views (CBV) that is changing per draw in the root layout so that descriptor heap space doesn't have to be allocated by the application per draw (and save pointing a descriptor table at the new location in the descriptor heap).</span></span> <span data-ttu-id="55e25-107">Wenn Sie etwas in die Stamm Signatur einfügen, übergibt die Anwendung lediglich die Versionskontrolle an den Treiber, aber dies ist die Infrastruktur, die Sie bereits haben.</span><span class="sxs-lookup"><span data-stu-id="55e25-107">By putting something in the root signature, the application is merely handing the versioning responsibility to the driver, but this is infrastructure that they already have.</span></span>

<span data-ttu-id="55e25-108">Für das Rendering, das sehr wenige Ressourcen verwendet, ist möglicherweise keine Deskriptortabelle/Heap-Verwendung erforderlich, wenn alle benötigten Deskriptoren direkt in die Stamm Signatur eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="55e25-108">For rendering that uses extremely few resources, descriptor table/heap use may not be needed at all if all the needed descriptors can be placed directly in the root signature.</span></span>

<span data-ttu-id="55e25-109">In der Stamm Signatur werden nur die folgenden deskriptortypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="55e25-109">The only types of descriptors supported in the root signature are:</span></span>
- <span data-ttu-id="55e25-110">Cbvs.</span><span class="sxs-lookup"><span data-stu-id="55e25-110">CBVs.</span></span>
- <span data-ttu-id="55e25-111">Shader-Ressourcen Sichten (Srvs)/unordered Access views (UAVs) der Puffer Ressourcen, in denen das SRV/UAV-Format nur 32 Bit Float/uint/Sint-Komponenten enthält (es gibt keine Formatkonvertierung).</span><span class="sxs-lookup"><span data-stu-id="55e25-111">Shader Resource Views (SRVs)/Unordered Access Views (UAVs) of buffer resources where the SRV/UAV format contains only 32 bit FLOAT/UINT/SINT components (there is no format conversion).</span></span>
- <span data-ttu-id="55e25-112">Srvs von Raytracing-beschleunigungsstrukturen in lokalen oder globalen Stamm Signaturen.</span><span class="sxs-lookup"><span data-stu-id="55e25-112">SRVs of raytracing acceleration structures, in local or global root signatures.</span></span> 

<span data-ttu-id="55e25-113">UAVs im Stamm können keine Indikatoren zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="55e25-113">UAVs in the root cannot have counters associated with them.</span></span> <span data-ttu-id="55e25-114">Deskriptoren in der Stamm Signatur werden jeweils als einzelne separate Deskriptoren angezeigt, &mdash; die nicht dynamisch indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="55e25-114">Descriptors in the root signature appear each as individual separate descriptors&mdash;they cannot be dynamically indexed.</span></span>

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

<span data-ttu-id="55e25-115">Im obigen Beispiel `mySceneData` kann nicht als Array deklariert werden, wie in, `cbuffer mySceneData[2]` Wenn es in einem Deskriptor in der Stamm Signatur zugeordnet werden soll, da die Indizierung über Deskriptoren in der Stamm Signatur nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="55e25-115">In the above example, `mySceneData` cannot be declared as an array, as in `cbuffer mySceneData[2]` if it is going to be mapped onto a descriptor in the root signature, since indexing across descriptors is not supported in the root signature.</span></span> <span data-ttu-id="55e25-116">Die Anwendung kann separate einzelne Konstante Puffer definieren und Sie bei Bedarf als separaten Eintrag in der Stamm Signatur definieren.</span><span class="sxs-lookup"><span data-stu-id="55e25-116">The application can define separate individual constant buffers and define them each as a separate entry in the root signature if desired.</span></span> <span data-ttu-id="55e25-117">Beachten Sie, dass `mySceneData` ein Array innerhalb von oben vorhanden ist `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="55e25-117">Note that within `mySceneData` above, there is an array `bar[2]`.</span></span> <span data-ttu-id="55e25-118">Die dynamische Indizierung innerhalb des Konstanten Puffers ist gültig. ein Deskriptor in der Stamm Signatur verhält sich so, wie sich der gleiche Deskriptor verhält, wenn er über einen deskriptorheap aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="55e25-118">Dynamic indexing within the constant buffer is valid - a descriptor in the root signature behaves just like the same descriptor would behave if accessed through a descriptor heap.</span></span> <span data-ttu-id="55e25-119">Dies steht im Gegensatz zu Inlining-Konstanten direkt in der Stamm Signatur, die auch wie ein konstanter Puffer angezeigt werden, außer mit der Einschränkung, dass die dynamische Indizierung innerhalb der Inline Konstanten nicht zulässig ist `bar[2]` .</span><span class="sxs-lookup"><span data-stu-id="55e25-119">This is in contrast with inlining constants directly in the root signature, which also appears like a constant buffer except with the constraint that dynamic indexing within the inlined constants is not permitted, so `bar[2]` would not be allowed there.</span></span>

<span data-ttu-id="55e25-120">Die folgenden APIs (von der [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Schnittstelle) dienen zum Festlegen von Deskriptoren direkt auf der Stamm Signatur:</span><span class="sxs-lookup"><span data-stu-id="55e25-120">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting descriptors directly on the root signature:</span></span>

-   [<span data-ttu-id="55e25-121">**Setcomputerootconstantbufferview**</span><span class="sxs-lookup"><span data-stu-id="55e25-121">**SetComputeRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [<span data-ttu-id="55e25-122">**Setgraphicsrootconstantbufferview**</span><span class="sxs-lookup"><span data-stu-id="55e25-122">**SetGraphicsRootConstantBufferView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [<span data-ttu-id="55e25-123">**Setcomputerootshaderresourceview**</span><span class="sxs-lookup"><span data-stu-id="55e25-123">**SetComputeRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [<span data-ttu-id="55e25-124">**Setgraphicsrootshaderresourceview**</span><span class="sxs-lookup"><span data-stu-id="55e25-124">**SetGraphicsRootShaderResourceView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [<span data-ttu-id="55e25-125">**Setcomputerootunorderedaccessview**</span><span class="sxs-lookup"><span data-stu-id="55e25-125">**SetComputeRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [<span data-ttu-id="55e25-126">**Setgraphicsrootunorderedaccessview**</span><span class="sxs-lookup"><span data-stu-id="55e25-126">**SetGraphicsRootUnorderedAccessView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> <span data-ttu-id="55e25-127">Es gibt kein Konzept eines "root Deskriptor Array" in Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="55e25-127">There is no concept of a "root descriptor array" in Direct3D 12.</span></span> <span data-ttu-id="55e25-128">Deskriptorarrays werden nur in deskriptorheaps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55e25-128">Descriptor arrays are only supported in descriptor heaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55e25-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="55e25-129">Related topics</span></span>

[<span data-ttu-id="55e25-130">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="55e25-130">Root Signatures</span></span>](root-signatures.md)
