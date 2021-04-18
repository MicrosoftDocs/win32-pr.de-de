---
description: 'Die setpositions-Methode legt die aktuelle Position und die Position des Stopps fest. Diese Methode implementiert die imediaseeking:: setpositions-Methode.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Cpospassthru. setpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361050"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="5ad68-104">Cpospassthru. setpositions-Methode</span><span class="sxs-lookup"><span data-stu-id="5ad68-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="5ad68-105">Die `SetPositions` -Methode legt die aktuelle Position und die Position des Stopps fest.</span><span class="sxs-lookup"><span data-stu-id="5ad68-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="5ad68-106">Diese Methode implementiert die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5ad68-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad68-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ad68-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5ad68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ad68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad68-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="5ad68-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad68-110">Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats angibt.</span><span class="sxs-lookup"><span data-stu-id="5ad68-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5ad68-111">*dwcurrentflags*</span><span class="sxs-lookup"><span data-stu-id="5ad68-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad68-112">Bitweise Kombination von-Flags.</span><span class="sxs-lookup"><span data-stu-id="5ad68-112">Bitwise combination of flags.</span></span> <span data-ttu-id="5ad68-113">Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="5ad68-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="5ad68-114">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="5ad68-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad68-115">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats angibt.</span><span class="sxs-lookup"><span data-stu-id="5ad68-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="5ad68-116">*dwstopflags*</span><span class="sxs-lookup"><span data-stu-id="5ad68-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad68-117">Bitweise Kombination von-Flags.</span><span class="sxs-lookup"><span data-stu-id="5ad68-117">Bitwise combination of flags.</span></span> <span data-ttu-id="5ad68-118">Weitere Informationen finden Sie unter [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="5ad68-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad68-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ad68-119">Return value</span></span>

<span data-ttu-id="5ad68-120">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="5ad68-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad68-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ad68-121">Requirements</span></span>



| <span data-ttu-id="5ad68-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ad68-122">Requirement</span></span> | <span data-ttu-id="5ad68-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5ad68-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad68-124">Header</span><span class="sxs-lookup"><span data-stu-id="5ad68-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5ad68-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad68-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ad68-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ad68-126">Library</span></span><br/> | <dl> <span data-ttu-id="5ad68-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad68-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad68-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ad68-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad68-129">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5ad68-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




