---
description: Boolescher Wert, der angibt, ob der Filter derzeit Frames löscht. Wenn dieser Wert true ist, fährt der Filter mit dem Ablegen von Frames fort, bis der nächste Keyframe erreicht oder 30 Delta Rahmen in einer Zeile ohne Keyframe empfangen werden.
ms.assetid: 1af22879-bf9b-4835-b3b5-06fb52b3140f
title: 'Cvideotransformfilter:: m_bSkipping Member (vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSkipping
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7beb4073052149e246a55ffbb1ff057e836704c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360924"
---
# <a name="cvideotransformfilterm_bskipping-member"></a><span data-ttu-id="6a49f-104">Cvideotransformfilter:: m \_ bskipping-Member</span><span class="sxs-lookup"><span data-stu-id="6a49f-104">CVideoTransformFilter::m\_bSkipping member</span></span>

<span data-ttu-id="6a49f-105">Boolescher Wert, der angibt, ob der Filter derzeit Frames löscht.</span><span class="sxs-lookup"><span data-stu-id="6a49f-105">Boolean value that indicates whether the filter is currently dropping frames.</span></span> <span data-ttu-id="6a49f-106">Wenn dieser Wert **true** ist, fährt der Filter mit dem Ablegen von Frames fort, bis der nächste Keyframe erreicht oder 30 Delta Rahmen in einer Zeile ohne Keyframe empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6a49f-106">If this value is **TRUE**, the filter continues to drop frames until it reaches the next key frame, or until it receives 30 delta frames in a row without a key frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a49f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a49f-107">Syntax</span></span>


```C++
BOOL m_bSkipping;
```



## <a name="requirements"></a><span data-ttu-id="6a49f-108">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6a49f-108">Requirements</span></span>



| <span data-ttu-id="6a49f-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a49f-109">Requirement</span></span> | <span data-ttu-id="6a49f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="6a49f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a49f-111">Header</span><span class="sxs-lookup"><span data-stu-id="6a49f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="6a49f-112"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a49f-112"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6a49f-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a49f-113">Library</span></span><br/> | <dl> <span data-ttu-id="6a49f-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6a49f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a49f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a49f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a49f-116">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6a49f-116">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




