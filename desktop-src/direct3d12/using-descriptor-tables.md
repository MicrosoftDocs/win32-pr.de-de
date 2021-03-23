---
title: Verwenden von deskriptortabellen
description: Deskriptortabellen, von denen jedes einen Bereich in einem deskriptorheap identifiziert, werden an Slots gebunden, die durch die aktuelle Stamm Signatur in einer Befehlsliste definiert sind.
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104230"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="d1269-103">Verwenden von deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="d1269-103">Using Descriptor Tables</span></span>

<span data-ttu-id="d1269-104">Deskriptortabellen, von denen jedes einen Bereich in einem deskriptorheap identifiziert, werden an Slots gebunden, die durch die aktuelle Stamm Signatur in einer Befehlsliste definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1269-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="d1269-105">Indizieren von deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="d1269-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="d1269-106">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d1269-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="d1269-107">Shader können Ressourcen suchen, auf die von den Deskriptoren verwiesen wird, aus denen die Deskriptortabelle besteht.</span><span class="sxs-lookup"><span data-stu-id="d1269-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="d1269-108">Andere Ressourcen Bindungen: Index Puffer, Vertex-Puffer, streamausgabepuffer, Renderziele und tiefen Schablone werden direkt in einer Befehlsliste und nicht über Deskriptoren ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1269-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="d1269-109">Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="d1269-109">To summarize:</span></span>

<span data-ttu-id="d1269-110">Die folgenden Ressourcen Verweise können dieselbe Deskriptortabelle und denselben Heap aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d1269-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="d1269-111">Shaderressourcenansichten</span><span class="sxs-lookup"><span data-stu-id="d1269-111">Shader resource views</span></span>
-   <span data-ttu-id="d1269-112">Ungeordnete Zugriffs Sichten</span><span class="sxs-lookup"><span data-stu-id="d1269-112">Unordered access views</span></span>
-   <span data-ttu-id="d1269-113">Konstantenpuffersichten</span><span class="sxs-lookup"><span data-stu-id="d1269-113">Constant buffer views</span></span>

<span data-ttu-id="d1269-114">Die folgenden Ressourcen Verweise müssen sich in einem eigenen deskriptorheap befinden:</span><span class="sxs-lookup"><span data-stu-id="d1269-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="d1269-115">Sampler</span><span class="sxs-lookup"><span data-stu-id="d1269-115">Samplers</span></span>

<span data-ttu-id="d1269-116">Die folgenden Ressourcen werden nicht in deskriptortabellen oder Heaps abgelegt, sondern direkt mithilfe von Befehlslisten gebunden:</span><span class="sxs-lookup"><span data-stu-id="d1269-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="d1269-117">Indexpuffer</span><span class="sxs-lookup"><span data-stu-id="d1269-117">Index buffers</span></span>
-   <span data-ttu-id="d1269-118">Vertex-Puffer</span><span class="sxs-lookup"><span data-stu-id="d1269-118">Vertex buffers</span></span>
-   <span data-ttu-id="d1269-119">Stream-Ausgabepuffer</span><span class="sxs-lookup"><span data-stu-id="d1269-119">Stream output buffers</span></span>
-   <span data-ttu-id="d1269-120">Renderziele</span><span class="sxs-lookup"><span data-stu-id="d1269-120">Render targets</span></span>
-   <span data-ttu-id="d1269-121">Ansicht der tiefen Schablone</span><span class="sxs-lookup"><span data-stu-id="d1269-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="d1269-122">Indizieren von deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="d1269-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="d1269-123">Shader können nicht über deskriptortabellengrenzen hinweg dynamisch von einer bestimmten CallSite im Shader indizieren.</span><span class="sxs-lookup"><span data-stu-id="d1269-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="d1269-124">Allerdings kann die Auswahl eines Deskriptors in einer Deskriptortabelle dynamisch im Shader-Code innerhalb von Bereichen desselben deskriptortyps (z. b. Indizierung über einen zusammenhängenden Bereich von Srvs) indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d1269-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1269-125">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d1269-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1269-126">Deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="d1269-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




