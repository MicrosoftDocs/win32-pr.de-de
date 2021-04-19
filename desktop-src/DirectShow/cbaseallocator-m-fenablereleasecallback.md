---
description: 'Flag zum angeben, ob der releaserückruf aktiviert ist. Dieses Flag wird in der Konstruktormethode festgelegt. Wenn der Wert false ist, bewirkt das Aufrufen der cbasezucator:: setnotify-Methode, dass eine-Assertion ausgelöst wird (in Debugbuilds).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Cbasezucator:: m_fEnableReleaseCallback Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362156"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="37e71-105">Cbasezucator:: m \_ fenablereleasecallback-Member</span><span class="sxs-lookup"><span data-stu-id="37e71-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="37e71-106">Flag zum angeben, ob der releaserückruf aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="37e71-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="37e71-107">Dieses Flag wird in der Konstruktormethode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37e71-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="37e71-108">Wenn der Wert **false** ist, bewirkt das Aufrufen der [**cbasezucator:: setnotify**](cbaseallocator-setnotify.md) -Methode, dass eine-Assertion ausgelöst wird (in Debugbuilds).</span><span class="sxs-lookup"><span data-stu-id="37e71-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="37e71-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="37e71-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="37e71-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="37e71-110">Requirements</span></span>



| <span data-ttu-id="37e71-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37e71-111">Requirement</span></span> | <span data-ttu-id="37e71-112">Wert</span><span class="sxs-lookup"><span data-stu-id="37e71-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e71-113">Header</span><span class="sxs-lookup"><span data-stu-id="37e71-113">Header</span></span><br/>  | <dl> <span data-ttu-id="37e71-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37e71-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="37e71-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="37e71-115">Library</span></span><br/> | <dl> <span data-ttu-id="37e71-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="37e71-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37e71-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37e71-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e71-118">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="37e71-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




