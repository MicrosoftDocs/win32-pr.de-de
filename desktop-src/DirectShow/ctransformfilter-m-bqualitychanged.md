---
description: Flag, das angibt, ob sich die Qualität geändert hat.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Ctransformfilter:: m_bQualityChanged Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372660"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a><span data-ttu-id="040a6-103">Ctransformfilter:: m \_ bqualitychanged-Member</span><span class="sxs-lookup"><span data-stu-id="040a6-103">CTransformFilter::m\_bQualityChanged member</span></span>

<span data-ttu-id="040a6-104">Flag, das angibt, ob sich die Qualität geändert hat.</span><span class="sxs-lookup"><span data-stu-id="040a6-104">Flag that indicates whether the quality has changed.</span></span> <span data-ttu-id="040a6-105">Wenn der Filter zum ersten Mal ein Beispiel löscht, sendet er ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager und legt dieses Flag auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="040a6-105">The first time that the filter drops a sample, it sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager and sets this flag to **TRUE**.</span></span> <span data-ttu-id="040a6-106">Dieses Ereignis wird erst dann wieder gesendet, wenn der Filter angehalten und neu gestartet wird, auch wenn es in der Zwischenzeit weiterhin Beispiele enthält.</span><span class="sxs-lookup"><span data-stu-id="040a6-106">It does not send this event again until the filter stops and restarts, even if it continues to drop samples in the meantime.</span></span>

## <a name="syntax"></a><span data-ttu-id="040a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="040a6-107">Syntax</span></span>


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a><span data-ttu-id="040a6-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="040a6-108">Requirements</span></span>



| <span data-ttu-id="040a6-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="040a6-109">Requirement</span></span> | <span data-ttu-id="040a6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="040a6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="040a6-111">Header</span><span class="sxs-lookup"><span data-stu-id="040a6-111">Header</span></span><br/>  | <dl> <span data-ttu-id="040a6-112"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="040a6-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="040a6-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="040a6-113">Library</span></span><br/> | <dl> <span data-ttu-id="040a6-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="040a6-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="040a6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="040a6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040a6-116">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="040a6-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




