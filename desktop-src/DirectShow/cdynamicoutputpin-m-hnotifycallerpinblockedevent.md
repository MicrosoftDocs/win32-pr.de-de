---
description: Das Ereignis, das signalisiert wird, wenn die PIN erfolgreich blockiert wird, oder der Benutzer bricht einen ausstehenden Block ab.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Cdynamicoutputpin:: m_hNotifyCallerPinBlockedEvent Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373628"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="5d6d1-103">Cdynamicoutputpin:: m \_ hnotifycallerpinblockedevent-Member</span><span class="sxs-lookup"><span data-stu-id="5d6d1-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="5d6d1-104">Das Ereignis, das signalisiert wird, wenn die PIN erfolgreich blockiert wird, oder der Benutzer bricht einen ausstehenden Block ab.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d6d1-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="5d6d1-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-106">Remarks</span></span>

<span data-ttu-id="5d6d1-107">Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="5d6d1-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6d1-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d6d1-108">Requirements</span></span>



| <span data-ttu-id="5d6d1-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d6d1-109">Requirement</span></span> | <span data-ttu-id="5d6d1-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5d6d1-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6d1-111">Header</span><span class="sxs-lookup"><span data-stu-id="5d6d1-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5d6d1-112"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5d6d1-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d6d1-113">Library</span></span><br/> | <dl> <span data-ttu-id="5d6d1-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5d6d1-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d6d1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d6d1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6d1-116">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5d6d1-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




