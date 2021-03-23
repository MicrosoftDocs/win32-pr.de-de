---
title: Deskriptortabellen
description: Eine Deskriptortabelle ist logisch ein Array von Deskriptoren.
ms.assetid: 5faf294f-acd5-4b39-92f4-1d6b2abe3040
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10414f8458006029f3279203e949b43410911fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103486"
---
# <a name="descriptor-tables"></a><span data-ttu-id="c4026-103">Deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="c4026-103">Descriptor Tables</span></span>

<span data-ttu-id="c4026-104">Eine Deskriptortabelle ist logisch ein Array von Deskriptoren.</span><span class="sxs-lookup"><span data-stu-id="c4026-104">A descriptor table is logically an array of descriptors.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4026-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c4026-105">In this section</span></span>



| <span data-ttu-id="c4026-106">Thema</span><span class="sxs-lookup"><span data-stu-id="c4026-106">Topic</span></span>                                                                                 | <span data-ttu-id="c4026-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4026-107">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4026-108">Übersicht über deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="c4026-108">Descriptor Tables Overview</span></span>](descriptor-tables-overview.md)<br/>               | <span data-ttu-id="c4026-109">Jede Deskriptortabelle speichert Deskriptoren von einem oder mehreren Typen: Srvs, uave, cbvs und Samplers.</span><span class="sxs-lookup"><span data-stu-id="c4026-109">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="c4026-110">Eine Deskriptortabelle ist keine Speicher Belegung. Es handelt sich einfach um einen Offset und eine Länge in einem deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="c4026-110">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span><br/> |
| [<span data-ttu-id="c4026-111">Verwenden von deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="c4026-111">Using Descriptor Tables</span></span>](using-descriptor-tables.md)<br/>                     | <span data-ttu-id="c4026-112">Deskriptortabellen, von denen jedes einen Bereich in einem deskriptorheap identifiziert, werden an Slots gebunden, die durch die aktuelle Stamm Signatur in einer Befehlsliste definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c4026-112">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span> <br/>                                                               |
| [<span data-ttu-id="c4026-113">Erweiterte Verwendung von deskriptortabellen</span><span class="sxs-lookup"><span data-stu-id="c4026-113">Advanced Use of Descriptor Tables</span></span>](advanced-use-of-descriptor-tables.md)<br/> | <span data-ttu-id="c4026-114">In den folgenden Abschnitten finden Sie Informationen zur erweiterten Verwendung von deskriptortabellen.</span><span class="sxs-lookup"><span data-stu-id="c4026-114">The following sections provide information about the advanced use of descriptor tables.</span></span><br/>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="c4026-115">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c4026-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4026-116">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="c4026-116">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="c4026-117">Ressourcen Bindung</span><span class="sxs-lookup"><span data-stu-id="c4026-117">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="c4026-118">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="c4026-118">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





