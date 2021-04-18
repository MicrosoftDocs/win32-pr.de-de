---
title: Gedenkens. CPP
description: In der Beispiel Anbieter Komponente ist ein Codebeispiel, das die Speicher Belegung und-Freigabe anzeigt, in "Memory. cpp". In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340404"
---
# <a name="memorycpp"></a><span data-ttu-id="09d0c-104">Gedenkens. CPP</span><span class="sxs-lookup"><span data-stu-id="09d0c-104">MEMORY.CPP</span></span>

<span data-ttu-id="09d0c-105">In der Beispiel Anbieter Komponente ist ein Codebeispiel, das die Speicher Belegung und-Freigabe anzeigt, in "Memory. cpp".</span><span class="sxs-lookup"><span data-stu-id="09d0c-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="09d0c-106">In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="09d0c-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="09d0c-107">Element</span><span class="sxs-lookup"><span data-stu-id="09d0c-107">Item</span></span>                | <span data-ttu-id="09d0c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09d0c-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="09d0c-109">**"Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="09d0c-109">**AllocProvMem**</span></span>    | <span data-ttu-id="09d0c-110">Zuordnen des angegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="09d0c-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="09d0c-111">**Freiprovmem**</span><span class="sxs-lookup"><span data-stu-id="09d0c-111">**FreeProvMem**</span></span>     | <span data-ttu-id="09d0c-112">Der freie Speicherplatz wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="09d0c-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="09d0c-113">**Rezuweisung**</span><span class="sxs-lookup"><span data-stu-id="09d0c-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="09d0c-114">Zuordnen von zusammenhängenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="09d0c-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="09d0c-115">**Zuordnung von "Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="09d0c-115">**AllocProvStr**</span></span>    | <span data-ttu-id="09d0c-116">Zuordnen einer LPWSTR-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="09d0c-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="09d0c-117">**Freiprovstr**</span><span class="sxs-lookup"><span data-stu-id="09d0c-117">**FreeProvStr**</span></span>     | <span data-ttu-id="09d0c-118">Freie Zeichenfolge, wenn Sie nicht bereits freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="09d0c-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="09d0c-119">**Rezuweisung**</span><span class="sxs-lookup"><span data-stu-id="09d0c-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="09d0c-120">Zuordnen von zusammenhängenden Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="09d0c-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="09d0c-121">**Provallocstring**</span><span class="sxs-lookup"><span data-stu-id="09d0c-121">**ProvAllocString**</span></span> | <span data-ttu-id="09d0c-122">Überprüft die Zeichenfolge und den ersten Parameter.</span><span class="sxs-lookup"><span data-stu-id="09d0c-122">Verifies string and first parameter.</span></span> <span data-ttu-id="09d0c-123">Wenn OK, wird die Zuordnung durchführt.</span><span class="sxs-lookup"><span data-stu-id="09d0c-123">If OK, then performs allocation.</span></span> |



 

 

 




