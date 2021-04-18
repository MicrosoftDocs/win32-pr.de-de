---
description: Speicherzuweisung
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Speicherzuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522203"
---
# <a name="memory-allocator"></a><span data-ttu-id="663b2-103">Speicherzuweisung</span><span class="sxs-lookup"><span data-stu-id="663b2-103">Memory Allocator</span></span>

<span data-ttu-id="663b2-104">Das arbeitsspeicherzuordnerobjekt weist Puffer für Medien Beispiele zu.</span><span class="sxs-lookup"><span data-stu-id="663b2-104">The Memory Allocator object allocates buffers for media samples.</span></span> <span data-ttu-id="663b2-105">Filter können dieses Objekt verwenden, um freigegebene Speicherpuffer zuzuordnen. ein Filter mit speziellen Anforderungen kann jedoch auch ein eigenes Speicher zuordnerobjekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="663b2-105">Filters can use this object to allocate shared memory buffers; however, a filter with special requirements can also implement its own memory allocator object.</span></span> <span data-ttu-id="663b2-106">Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="663b2-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="663b2-107">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="663b2-107">Class Identifier</span></span> | <span data-ttu-id="663b2-108">CLSID- \_ memoryzuweisung</span><span class="sxs-lookup"><span data-stu-id="663b2-108">CLSID\_MemoryAllocator</span></span>                 |
| <span data-ttu-id="663b2-109">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="663b2-109">Interfaces</span></span>       | [<span data-ttu-id="663b2-110">**Imemzuordcator**</span><span class="sxs-lookup"><span data-stu-id="663b2-110">**IMemAllocator**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a><span data-ttu-id="663b2-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="663b2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663b2-112">DirectShow-Objekte</span><span class="sxs-lookup"><span data-stu-id="663b2-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



