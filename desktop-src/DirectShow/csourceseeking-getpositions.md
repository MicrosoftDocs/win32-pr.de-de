---
description: 'Die getpositions-Methode ruft die aktuelle Position und die Position des Stopps ab. Diese Methode implementiert die imediaseeking:: getpositions-Methode.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Csourceseeking. getpositions-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366752"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="005d7-104">Csourceseeking. getpositions-Methode</span><span class="sxs-lookup"><span data-stu-id="005d7-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="005d7-105">Die `GetPositions` -Methode ruft die aktuelle Position und die Position des Stopps ab.</span><span class="sxs-lookup"><span data-stu-id="005d7-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="005d7-106">Diese Methode implementiert die [**imediaseeking:: getpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) -Methode.</span><span class="sxs-lookup"><span data-stu-id="005d7-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="005d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="005d7-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="005d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="005d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005d7-109">*pcurrent*</span><span class="sxs-lookup"><span data-stu-id="005d7-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="005d7-110">Ein Zeiger auf eine Variable, die die Startposition empfängt.</span><span class="sxs-lookup"><span data-stu-id="005d7-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="005d7-111">*pstopps*</span><span class="sxs-lookup"><span data-stu-id="005d7-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="005d7-112">Ein Zeiger auf eine Variable, die die Position des Stopps empfängt.</span><span class="sxs-lookup"><span data-stu-id="005d7-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="005d7-113">Return value</span></span>

<span data-ttu-id="005d7-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="005d7-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="005d7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="005d7-115">Remarks</span></span>

<span data-ttu-id="005d7-116">Für den *pcurrent* -Parameter gibt diese Methode den Wert der [**csourceseeking:: m \_ rtstart**](csourceseeking-m-rtstart.md) -Member-Variable zurück, die die letzte Suchzeit und nicht die aktuelle streamingposition darstellt.</span><span class="sxs-lookup"><span data-stu-id="005d7-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="005d7-117">Wenn eine Anwendung jedoch **imediaseeking:: getpositions** über den Filter Graph-Manager aufruft, werden die Werte in der Regel von einem rendererfilter und keinem Quell Filter abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="005d7-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="005d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="005d7-118">Requirements</span></span>



| <span data-ttu-id="005d7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="005d7-119">Requirement</span></span> | <span data-ttu-id="005d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="005d7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="005d7-121">Header</span><span class="sxs-lookup"><span data-stu-id="005d7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="005d7-122"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="005d7-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="005d7-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="005d7-123">Library</span></span><br/> | <dl> <span data-ttu-id="005d7-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="005d7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005d7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="005d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005d7-126">**Csourceseeking-Klasse**</span><span class="sxs-lookup"><span data-stu-id="005d7-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




