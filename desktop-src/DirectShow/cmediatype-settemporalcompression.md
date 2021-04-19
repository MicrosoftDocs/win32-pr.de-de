---
description: Die settemporalcompression-Methode gibt an, ob Samples mithilfe der temporalen (Interframe-) Komprimierung komprimiert werden.
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Cmediatype. settemporalcompression-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367043"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="9e10c-103">Cmediatype. settemporalcompression-Methode</span><span class="sxs-lookup"><span data-stu-id="9e10c-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="9e10c-104">Die- `SetTemporalCompression` Methode gibt an, ob Samples mithilfe der temporalen (Interframe-) Komprimierung komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e10c-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e10c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e10c-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="9e10c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e10c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e10c-107">*bkomprimiert*</span><span class="sxs-lookup"><span data-stu-id="9e10c-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="9e10c-108">Boolescher Wert, der angibt, ob der Stream Temporale Komprimierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e10c-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="9e10c-109">Wenn der Stream die Temporale Komprimierung verwendet, legen Sie den Wert auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="9e10c-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e10c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e10c-110">Return value</span></span>

<span data-ttu-id="9e10c-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9e10c-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e10c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e10c-112">Remarks</span></span>

<span data-ttu-id="9e10c-113">Diese Methode legt den **btemporalcompression** -Member fest.</span><span class="sxs-lookup"><span data-stu-id="9e10c-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e10c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e10c-114">Requirements</span></span>



| <span data-ttu-id="9e10c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e10c-115">Requirement</span></span> | <span data-ttu-id="9e10c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9e10c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e10c-117">Header</span><span class="sxs-lookup"><span data-stu-id="9e10c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9e10c-118"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e10c-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9e10c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e10c-119">Library</span></span><br/> | <dl> <span data-ttu-id="9e10c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9e10c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e10c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e10c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e10c-122">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9e10c-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




