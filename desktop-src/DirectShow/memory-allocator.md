---
description: Speicherzuweisung
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Speicherzuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909419"
---
# <a name="memory-allocator"></a><span data-ttu-id="3c4fd-103">Speicherzuweisung</span><span class="sxs-lookup"><span data-stu-id="3c4fd-103">Memory Allocator</span></span>

<span data-ttu-id="3c4fd-104">Das Speicherzuweisungsobjekt ordnet Puffer für Medienbeispiele zu.</span><span class="sxs-lookup"><span data-stu-id="3c4fd-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="3c4fd-105">Filter können dieses Objekt verwenden, um Freigegebene Speicherpuffer zu reservieren. Ein Filter mit speziellen Anforderungen kann jedoch auch ein eigenes Speicherzuweisungsobjekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="3c4fd-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="3c4fd-106">Erstellen Sie dieses Objekt, indem Sie **CoCreateInstance aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="3c4fd-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="3c4fd-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="3c4fd-107">Label</span></span> | <span data-ttu-id="3c4fd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3c4fd-108">Value</span></span> |
|------------------|----------------------------------------|
| <span data-ttu-id="3c4fd-109">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="3c4fd-109">Class Identifier</span></span> | <span data-ttu-id="3c4fd-110">CLSID \_ MemoryAllocator</span><span class="sxs-lookup"><span data-stu-id="3c4fd-110">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="3c4fd-111">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="3c4fd-111">Interfaces</span></span>       | [<span data-ttu-id="3c4fd-112">**IMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="3c4fd-112">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="3c4fd-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c4fd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c4fd-114">DirectShow-Objekte</span><span class="sxs-lookup"><span data-stu-id="3c4fd-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



