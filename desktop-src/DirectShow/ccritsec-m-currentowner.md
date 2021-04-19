---
description: Thread Bezeichner des besitzenden Threads.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Ccritsec:: m_currentOwner Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372718"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="010c7-103">Ccritsec:: m \_ currentowner-Member</span><span class="sxs-lookup"><span data-stu-id="010c7-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="010c7-104">Thread Bezeichner des besitzenden Threads.</span><span class="sxs-lookup"><span data-stu-id="010c7-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="010c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="010c7-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="010c7-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="010c7-106">Remarks</span></span>

<span data-ttu-id="010c7-107">Diese Member-Variable wird nur in der Debugversion der Basisklasse definiert.</span><span class="sxs-lookup"><span data-stu-id="010c7-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="010c7-108">Der [kritische Abschnitt Debuggingfunktionen](critical-section-debugging-functions.md) verwenden diesen Member.</span><span class="sxs-lookup"><span data-stu-id="010c7-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="010c7-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="010c7-109">Requirements</span></span>



| <span data-ttu-id="010c7-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="010c7-110">Requirement</span></span> | <span data-ttu-id="010c7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="010c7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010c7-112">Header</span><span class="sxs-lookup"><span data-stu-id="010c7-112">Header</span></span><br/>  | <dl> <span data-ttu-id="010c7-113"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="010c7-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="010c7-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="010c7-114">Library</span></span><br/> | <dl> <span data-ttu-id="010c7-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="010c7-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010c7-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="010c7-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010c7-117">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="010c7-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




