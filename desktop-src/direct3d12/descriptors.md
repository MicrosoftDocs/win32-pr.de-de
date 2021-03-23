---
title: Deskriptoren
description: Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104144"
---
# <a name="descriptors"></a><span data-ttu-id="6c55b-103">Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="6c55b-103">Descriptors</span></span>

<span data-ttu-id="6c55b-104">Deskriptoren sind die primäre Bindungs Einheit für eine einzelne Ressource in D3D12.</span><span class="sxs-lookup"><span data-stu-id="6c55b-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6c55b-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6c55b-105">In this section</span></span>



| <span data-ttu-id="6c55b-106">Thema</span><span class="sxs-lookup"><span data-stu-id="6c55b-106">Topic</span></span>                                                       | <span data-ttu-id="6c55b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c55b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c55b-108">Übersicht über Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="6c55b-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="6c55b-109">Deskriptoren werden von API-aufrufen erstellt und identifizieren Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6c55b-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6c55b-110">Erstellen von Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="6c55b-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="6c55b-111">Beschreibt und zeigt Beispiele für das Erstellen von Index-, Vertex-und konstantenpuffersichten. Shader-Ressource, Renderziel, unsortierter Zugriff, Streamausgabe-und tiefen Schablonen Ansichten; und Samplers.</span><span class="sxs-lookup"><span data-stu-id="6c55b-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="6c55b-112">Alle Methoden zum Erstellen von Deskriptoren sind frei Thread.</span><span class="sxs-lookup"><span data-stu-id="6c55b-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="6c55b-113">Kopieren von Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="6c55b-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="6c55b-114">Die [**ID3D12Device:: copydescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) -Methode und die [**ID3D12Device:: copydescriptorssimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) -Methode auf der Geräteschnittstelle verwenden die CPU zum sofortigen Kopieren von Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="6c55b-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="6c55b-115">Sie können als frei Thread bezeichnet werden, solange mehrere Threads auf der CPU oder GPU keine potenziell in Konflikt stehenden Schreibvorgänge durchführen.</span><span class="sxs-lookup"><span data-stu-id="6c55b-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6c55b-116">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6c55b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c55b-117">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="6c55b-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="6c55b-118">Deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="6c55b-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="6c55b-119">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="6c55b-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="6c55b-120">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="6c55b-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





