---
description: Die aktuelle maximale Anzahl der zu löschenden Delta Frames.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Cvideotransformfilter:: m_nWaitForKey Member (vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365177"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a><span data-ttu-id="9d44a-103">Cvideotransformfilter:: m \_ nwaitforkey-Member</span><span class="sxs-lookup"><span data-stu-id="9d44a-103">CVideoTransformFilter::m\_nWaitForKey member</span></span>

<span data-ttu-id="9d44a-104">Die aktuelle maximale Anzahl der zu löschenden Delta Frames.</span><span class="sxs-lookup"><span data-stu-id="9d44a-104">The current maximum number of delta frames to drop.</span></span> <span data-ttu-id="9d44a-105">Obwohl diese Variable größer als 0 (null) ist, löscht der Filter Frames, bis ein Keyframe erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="9d44a-105">While this variable is greater than zero, the filter will drop frames until it reaches a key frame.</span></span> <span data-ttu-id="9d44a-106">Für jeden abgelegten Rahmen verringert der Filter diese Variable um eins, wodurch verhindert wird, dass der Filter eine übermäßige Anzahl von Frames löscht.</span><span class="sxs-lookup"><span data-stu-id="9d44a-106">For each frame that is dropped, the filter decrements this variable by one, which prevents the filter from dropping an excessive number of frames.</span></span> <span data-ttu-id="9d44a-107">Nach 30 Delta Frames in einer Zeile ohne Keyframes beginnt der Filter erneut mit der Übermittlung von Frames.</span><span class="sxs-lookup"><span data-stu-id="9d44a-107">After 30 delta frames in a row with no key frames, the filter will start delivering frames again.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d44a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d44a-108">Syntax</span></span>


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a><span data-ttu-id="9d44a-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9d44a-109">Requirements</span></span>



| <span data-ttu-id="9d44a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d44a-110">Requirement</span></span> | <span data-ttu-id="9d44a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9d44a-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d44a-112">Header</span><span class="sxs-lookup"><span data-stu-id="9d44a-112">Header</span></span><br/>  | <dl> <span data-ttu-id="9d44a-113"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d44a-113"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9d44a-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d44a-114">Library</span></span><br/> | <dl> <span data-ttu-id="9d44a-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9d44a-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d44a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d44a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d44a-117">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d44a-117">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




