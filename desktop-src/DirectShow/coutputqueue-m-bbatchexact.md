---
description: Flag, das angibt, ob das Objekt Stichproben in exakten Batches bereitstellt.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Coutputqueue:: m_bBatchExact-Member (outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372643"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="12695-103">Coutputqueue:: m \_ bbatchexact-Member</span><span class="sxs-lookup"><span data-stu-id="12695-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="12695-104">Flag, das angibt, ob das Objekt Stichproben in exakten Batches bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="12695-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="12695-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12695-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="12695-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12695-106">Remarks</span></span>

<span data-ttu-id="12695-107">Wenn der Wert **true** ist, wartet das Objekt, bis es über einen kompletten Batch von Medien Beispielen verfügt, bevor es bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12695-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="12695-108">Andernfalls werden bei ihrer Ankunft Beispiele bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="12695-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="12695-109">Die Element Variable [**coutputqueue:: m \_ lbatchsize**](coutputqueue-m-lbatchsize.md) definiert die Batch Größe.</span><span class="sxs-lookup"><span data-stu-id="12695-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="12695-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12695-110">Requirements</span></span>



| <span data-ttu-id="12695-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12695-111">Requirement</span></span> | <span data-ttu-id="12695-112">Wert</span><span class="sxs-lookup"><span data-stu-id="12695-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12695-113">Header</span><span class="sxs-lookup"><span data-stu-id="12695-113">Header</span></span><br/>  | <dl> <span data-ttu-id="12695-114"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12695-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12695-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12695-115">Library</span></span><br/> | <dl> <span data-ttu-id="12695-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="12695-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12695-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12695-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12695-118">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="12695-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




