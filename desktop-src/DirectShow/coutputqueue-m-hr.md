---
description: HRESULT-Wert, der angibt, ob das Objekt Beispiele akzeptiert. Wenn der Wert S \_ OK ist, akzeptiert das Objekt Stichproben. Andernfalls werden Stichproben abgelehnt.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Coutputqueue:: m_hr-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372348"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="e9626-105">Coutputqueue:: m \_ HR-Mitglied</span><span class="sxs-lookup"><span data-stu-id="e9626-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="e9626-106">**HRESULT** -Wert, der angibt, ob das Objekt Beispiele akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e9626-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="e9626-107">Wenn der Wert S \_ OK ist, akzeptiert das Objekt Stichproben.</span><span class="sxs-lookup"><span data-stu-id="e9626-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="e9626-108">Andernfalls werden Stichproben abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="e9626-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9626-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9626-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="e9626-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9626-110">Remarks</span></span>

<span data-ttu-id="e9626-111">Diese Element Variable wird verwendet, um Aktivitäten Thread übergreifend zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="e9626-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="e9626-112">Wenn die downstreameingabepin eine Stichprobe ablehnt, oder wenn das Objekt mit dem leeren beginnt, wird der Wert auf S \_ false oder auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9626-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="e9626-113">Das Objekt stellt keine weiteren Beispiele bereit, bis die Leerung beendet ist, oder bis die [**coutputqueue:: Reset**](coutputqueue-reset.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e9626-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9626-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9626-114">Requirements</span></span>



| <span data-ttu-id="e9626-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9626-115">Requirement</span></span> | <span data-ttu-id="e9626-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e9626-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9626-117">Header</span><span class="sxs-lookup"><span data-stu-id="e9626-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e9626-118"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9626-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9626-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e9626-119">Library</span></span><br/> | <dl> <span data-ttu-id="e9626-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e9626-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9626-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9626-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9626-122">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e9626-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




