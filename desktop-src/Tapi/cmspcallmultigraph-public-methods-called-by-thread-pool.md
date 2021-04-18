---
description: Die folgende Liste enthält die öffentlichen cmspcallmultigraph-Methoden, die vom Thread Pool aufgerufen werden.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Vom Thread Pool aufgerufene öffentliche cmspcallmultigraph-Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358486"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="0fca8-103">Vom Thread Pool aufgerufene öffentliche cmspcallmultigraph-Methoden</span><span class="sxs-lookup"><span data-stu-id="0fca8-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="0fca8-104">Öffentliche cmspcallmultigraph-Methoden</span><span class="sxs-lookup"><span data-stu-id="0fca8-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="0fca8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fca8-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fca8-106">**Dispatchgraphevent**</span><span class="sxs-lookup"><span data-stu-id="0fca8-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="0fca8-107">Wird aufgerufen, wenn das Filter Diagramm ein Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="0fca8-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="0fca8-108">**"Lenker"**</span><span class="sxs-lookup"><span data-stu-id="0fca8-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="0fca8-109">Wird von der statischen [**dispatchgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0fca8-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="0fca8-110">Warteschlangen [**processgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) auf dem Haupt-MSP-Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="0fca8-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="0fca8-111">**Processgraphevent**</span><span class="sxs-lookup"><span data-stu-id="0fca8-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="0fca8-112">Ermöglicht der MSP-Aufruf Objektinstanz, das Filter Diagramm Ereignis zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="0fca8-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="0fca8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0fca8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fca8-114">**Cmspcallmultigraph**</span><span class="sxs-lookup"><span data-stu-id="0fca8-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



