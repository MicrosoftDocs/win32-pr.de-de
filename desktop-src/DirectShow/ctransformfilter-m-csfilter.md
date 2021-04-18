---
description: Kritischer Abschnitt, der den Filter Zustand schützt. Weitere Informationen finden Sie unter Datenfluss für Filter Entwickler.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Ctransformfilter:: m_csFilter Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358690"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="acb3d-104">Ctransformfilter:: m \_ CSFilter-Member</span><span class="sxs-lookup"><span data-stu-id="acb3d-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="acb3d-105">Kritischer Abschnitt, der den Filter Zustand schützt.</span><span class="sxs-lookup"><span data-stu-id="acb3d-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="acb3d-106">Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="acb3d-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="acb3d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="acb3d-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="acb3d-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="acb3d-108">Requirements</span></span>



| <span data-ttu-id="acb3d-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acb3d-109">Requirement</span></span> | <span data-ttu-id="acb3d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="acb3d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acb3d-111">Header</span><span class="sxs-lookup"><span data-stu-id="acb3d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="acb3d-112"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acb3d-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="acb3d-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="acb3d-113">Library</span></span><br/> | <dl> <span data-ttu-id="acb3d-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="acb3d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb3d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acb3d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb3d-116">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="acb3d-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




