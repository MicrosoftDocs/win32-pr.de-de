---
description: Die initializeoutputsample-Methode ruft eine neue Ausgabe Stichprobe ab und initialisiert sie.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Initializeoutputsample-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359707"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="33e99-103">CTransformFilter.Initializeoutputsample-Methode</span><span class="sxs-lookup"><span data-stu-id="33e99-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="33e99-104">Die `InitializeOutputSample` -Methode ruft eine neue Ausgabe Stichprobe ab und initialisiert sie.</span><span class="sxs-lookup"><span data-stu-id="33e99-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e99-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="33e99-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33e99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e99-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="33e99-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="33e99-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle der Eingabe Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="33e99-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="33e99-109">*ppoutsample*</span><span class="sxs-lookup"><span data-stu-id="33e99-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="33e99-110">Empfängt einen Zeiger auf die **imediasample** -Schnittstelle des Ausgabe Beispiels.</span><span class="sxs-lookup"><span data-stu-id="33e99-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e99-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33e99-111">Return value</span></span>

<span data-ttu-id="33e99-112">Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="33e99-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e99-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e99-113">Remarks</span></span>

<span data-ttu-id="33e99-114">Diese Methode wird von der [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode aufgerufen, um das Ausgabe Beispiel vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="33e99-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="33e99-115">Im Allgemeinen müssen Sie diese Methode nicht in der abgeleiteten Klasse aufzurufen, es sei denn, Sie überschreiben die **Receive** -Methode.</span><span class="sxs-lookup"><span data-stu-id="33e99-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="33e99-116">Diese Methode ruft ein neues Beispiel aus der Zuweisung der Ausgabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="33e99-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="33e99-117">Anschließend werden die Beispiel Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert.</span><span class="sxs-lookup"><span data-stu-id="33e99-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="33e99-118">Die Beispiel Eigenschaften werden in der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="33e99-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="33e99-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e99-119">Requirements</span></span>



| <span data-ttu-id="33e99-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e99-120">Requirement</span></span> | <span data-ttu-id="33e99-121">Wert</span><span class="sxs-lookup"><span data-stu-id="33e99-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e99-122">Header</span><span class="sxs-lookup"><span data-stu-id="33e99-122">Header</span></span><br/>  | <dl> <span data-ttu-id="33e99-123"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33e99-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33e99-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33e99-124">Library</span></span><br/> | <dl> <span data-ttu-id="33e99-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33e99-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e99-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e99-127">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33e99-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




