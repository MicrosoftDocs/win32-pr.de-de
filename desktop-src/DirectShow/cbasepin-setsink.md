---
description: 'Mit der setsink-Methode wird ein externer Quality Manager festgelegt. Diese Methode implementiert die iqualitycontrol:: setsink-Methode.'
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: Cbasepin. setsink-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4237e342f8f49059cab017b17a1f116ca6e2da67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356441"
---
# <a name="cbasepinsetsink-method"></a><span data-ttu-id="97a7a-104">Cbasepin. setsink-Methode</span><span class="sxs-lookup"><span data-stu-id="97a7a-104">CBasePin.SetSink method</span></span>

<span data-ttu-id="97a7a-105">Mit der- `SetSink` Methode wird ein externer Quality Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97a7a-105">The `SetSink` method sets an external quality manager.</span></span> <span data-ttu-id="97a7a-106">Diese Methode implementiert die [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) -Methode.</span><span class="sxs-lookup"><span data-stu-id="97a7a-106">This method implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97a7a-107">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="97a7a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a7a-109">*piqc*</span><span class="sxs-lookup"><span data-stu-id="97a7a-109">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="97a7a-110">Ein Zeiger auf die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle von Quality Manager.</span><span class="sxs-lookup"><span data-stu-id="97a7a-110">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface of the quality manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a7a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97a7a-111">Return value</span></span>

<span data-ttu-id="97a7a-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="97a7a-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a7a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97a7a-113">Remarks</span></span>

<span data-ttu-id="97a7a-114">Mit dieser Methode können Sie Qualitäts Steuerungs Meldungen an einen externen Quality Manager umleiten.</span><span class="sxs-lookup"><span data-stu-id="97a7a-114">Call this method to redirect quality-control messages to an external quality manager.</span></span> <span data-ttu-id="97a7a-115">Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="97a7a-115">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97a7a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97a7a-116">Requirements</span></span>



| <span data-ttu-id="97a7a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97a7a-117">Requirement</span></span> | <span data-ttu-id="97a7a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="97a7a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a7a-119">Header</span><span class="sxs-lookup"><span data-stu-id="97a7a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="97a7a-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97a7a-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97a7a-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97a7a-121">Library</span></span><br/> | <dl> <span data-ttu-id="97a7a-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="97a7a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a7a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97a7a-124">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="97a7a-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




