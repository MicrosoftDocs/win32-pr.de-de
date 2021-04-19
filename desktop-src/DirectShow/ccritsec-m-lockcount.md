---
description: Anzahl der ausstehenden Sperren für dieses Objekt.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Ccritsec:: m_lockCount Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373843"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="b9615-103">Ccritsec:: m- \_ LockCount-Member</span><span class="sxs-lookup"><span data-stu-id="b9615-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="b9615-104">Anzahl der ausstehenden Sperren für dieses Objekt.</span><span class="sxs-lookup"><span data-stu-id="b9615-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9615-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9615-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="b9615-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9615-106">Remarks</span></span>

<span data-ttu-id="b9615-107">Diese Member-Variable wird nur in der Debugversion der Basisklasse definiert.</span><span class="sxs-lookup"><span data-stu-id="b9615-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="b9615-108">Der [kritische Abschnitt Debuggingfunktionen](critical-section-debugging-functions.md) verwenden diesen Member.</span><span class="sxs-lookup"><span data-stu-id="b9615-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9615-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9615-109">Requirements</span></span>



| <span data-ttu-id="b9615-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9615-110">Requirement</span></span> | <span data-ttu-id="b9615-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b9615-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9615-112">Header</span><span class="sxs-lookup"><span data-stu-id="b9615-112">Header</span></span><br/>  | <dl> <span data-ttu-id="b9615-113"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9615-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b9615-114">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9615-114">Library</span></span><br/> | <dl> <span data-ttu-id="b9615-115">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b9615-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9615-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9615-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9615-117">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b9615-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




