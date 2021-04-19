---
description: Zeiger auf ein kritisches Abschnitts Objekt, das den Filter Zustand schützt.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Cbasepin:: m_pLock Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361417"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="94e6c-103">Cbasepin:: m \_ Plock-Member</span><span class="sxs-lookup"><span data-stu-id="94e6c-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="94e6c-104">Zeiger auf ein kritisches Abschnitts Objekt, das den Filter Zustand schützt.</span><span class="sxs-lookup"><span data-stu-id="94e6c-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="94e6c-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="94e6c-106">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="94e6c-106">Requirements</span></span>



| <span data-ttu-id="94e6c-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94e6c-107">Requirement</span></span> | <span data-ttu-id="94e6c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="94e6c-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e6c-109">Header</span><span class="sxs-lookup"><span data-stu-id="94e6c-109">Header</span></span><br/>  | <dl> <span data-ttu-id="94e6c-110"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94e6c-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94e6c-111">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94e6c-111">Library</span></span><br/> | <dl> <span data-ttu-id="94e6c-112">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="94e6c-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e6c-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94e6c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e6c-114">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="94e6c-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="94e6c-115">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="94e6c-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




