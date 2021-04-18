---
description: Anzahl der streamingthreads, die diese PIN verwenden.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Cdynamicoutputpin:: m_dwNumOutstandingOutputPinUsers Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352155"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="c09b9-103">Cdynamicoutputpin:: m \_ dwnumoutstandingoutputpinusers-Member</span><span class="sxs-lookup"><span data-stu-id="c09b9-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="c09b9-104">Anzahl der streamingthreads, die diese PIN verwenden.</span><span class="sxs-lookup"><span data-stu-id="c09b9-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c09b9-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="c09b9-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c09b9-106">Remarks</span></span>

<span data-ttu-id="c09b9-107">Die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode erhöht diese Variable, und die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode dekretet diese Variable.</span><span class="sxs-lookup"><span data-stu-id="c09b9-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="c09b9-108">Wenn der Wert größer als 0 (null) ist, verwendet ein Thread diese PIN, um Daten zu streamen oder den Verbindungstyp zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c09b9-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="c09b9-109">Die PIN kann nicht blockiert werden, wenn dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c09b9-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="c09b9-110">Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="c09b9-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09b9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c09b9-111">Requirements</span></span>



| <span data-ttu-id="c09b9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c09b9-112">Requirement</span></span> | <span data-ttu-id="c09b9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c09b9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09b9-114">Header</span><span class="sxs-lookup"><span data-stu-id="c09b9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c09b9-115"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c09b9-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c09b9-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c09b9-116">Library</span></span><br/> | <dl> <span data-ttu-id="c09b9-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c09b9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c09b9-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c09b9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09b9-119">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c09b9-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="c09b9-120">**Cdynamicoutputpin:: streamingthreadusingoutputpin**</span><span class="sxs-lookup"><span data-stu-id="c09b9-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




