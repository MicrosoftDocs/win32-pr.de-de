---
description: Flag, das angibt, ob der Filter eine Benachrichtigung über das Ende des Datenstroms gesendet hat.
ms.assetid: 93f897de-04bb-4de4-a612-39b27c7d6f6c
title: 'Ctransformfilter:: m_bEOSDelivered Member (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bEOSDelivered
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24b87f9808c53b5f64f66031a8ee2a4e9449089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371679"
---
# <a name="ctransformfilterm_beosdelivered-member"></a><span data-ttu-id="cd088-103">Ctransformfilter:: m-über \_ mittelte Member</span><span class="sxs-lookup"><span data-stu-id="cd088-103">CTransformFilter::m\_bEOSDelivered member</span></span>

<span data-ttu-id="cd088-104">Flag, das angibt, ob der Filter eine Benachrichtigung über das Ende des Datenstroms gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="cd088-104">Flag that indicates whether the filter has sent an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd088-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd088-105">Syntax</span></span>


```C++
BOOL m_bEOSDelivered;
```



## <a name="remarks"></a><span data-ttu-id="cd088-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd088-106">Remarks</span></span>

<span data-ttu-id="cd088-107">Wenn der Filter angehalten wird, wenn keine Eingabe Verbindung vorhanden ist, sendet er eine downstreambenachrichtigung und legt dieses Flag auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="cd088-107">If the filter pauses when it does not have an input connection, it sends an end-of-stream notification downstream and sets this flag to **TRUE**.</span></span> <span data-ttu-id="cd088-108">Die Benachrichtigung über das Ende des Datenstroms stellt sicher, dass der Downstream-Filter nicht auf Stichproben wartet.</span><span class="sxs-lookup"><span data-stu-id="cd088-108">The end-of-stream notification ensures that the downstream filter does not wait for samples.</span></span> <span data-ttu-id="cd088-109">Beachten Sie, dass die [**EndOf Stream**](ctransformfilter-endofstream.md) -Methode des Filters dieses Flag nicht festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="cd088-109">Note that the filter's [**EndOfStream**](ctransformfilter-endofstream.md) method does not set this flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd088-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd088-110">Requirements</span></span>



| <span data-ttu-id="cd088-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd088-111">Requirement</span></span> | <span data-ttu-id="cd088-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cd088-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd088-113">Header</span><span class="sxs-lookup"><span data-stu-id="cd088-113">Header</span></span><br/>  | <dl> <span data-ttu-id="cd088-114"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd088-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd088-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cd088-115">Library</span></span><br/> | <dl> <span data-ttu-id="cd088-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cd088-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd088-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd088-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd088-118">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd088-118">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




