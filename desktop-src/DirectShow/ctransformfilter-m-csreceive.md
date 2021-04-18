---
description: Kritischer Abschnitt, der den streamingstatus schützt. Weitere Informationen finden Sie unter Datenfluss für Filter Entwickler.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Ctransformfilter:: m_csReceive Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372193"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="759a9-104">Ctransformfilter:: m \_ csreceive-Member</span><span class="sxs-lookup"><span data-stu-id="759a9-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="759a9-105">Kritischer Abschnitt, der den streamingstatus schützt.</span><span class="sxs-lookup"><span data-stu-id="759a9-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="759a9-106">Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="759a9-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="759a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="759a9-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="759a9-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="759a9-108">Requirements</span></span>



| <span data-ttu-id="759a9-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="759a9-109">Requirement</span></span> | <span data-ttu-id="759a9-110">Wert</span><span class="sxs-lookup"><span data-stu-id="759a9-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="759a9-111">Header</span><span class="sxs-lookup"><span data-stu-id="759a9-111">Header</span></span><br/>  | <dl> <span data-ttu-id="759a9-112"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="759a9-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="759a9-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="759a9-113">Library</span></span><br/> | <dl> <span data-ttu-id="759a9-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="759a9-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="759a9-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="759a9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="759a9-116">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="759a9-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




