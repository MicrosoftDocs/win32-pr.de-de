---
description: Die getdeliverybuffer-Methode ruft ein Medien Beispiel ab, das einen leeren Puffer enthält.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Cbaseoutputpin. getdeliverybuffer-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373953"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="7d65c-103">Cbaseoutputpin. getdeliverybuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="7d65c-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="7d65c-104">Die- `GetDeliveryBuffer` Methode ruft ein Medien Beispiel ab, das einen leeren Puffer enthält.</span><span class="sxs-lookup"><span data-stu-id="7d65c-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d65c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d65c-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7d65c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d65c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d65c-107">*ppsample*</span><span class="sxs-lookup"><span data-stu-id="7d65c-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7d65c-108">Adresse einer Variablen, die einen Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Puffers empfängt.</span><span class="sxs-lookup"><span data-stu-id="7d65c-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7d65c-109">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="7d65c-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7d65c-110">Ein Zeiger auf die Startzeit des Beispiels oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7d65c-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7d65c-111">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="7d65c-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="7d65c-112">Ein Zeiger auf die Endzeit der Stichprobe oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7d65c-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7d65c-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="7d65c-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="7d65c-114">Bitweise Kombination von Flags, die von der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Schnittstelle unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7d65c-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d65c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d65c-115">Return value</span></span>

<span data-ttu-id="7d65c-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7d65c-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7d65c-117">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="7d65c-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="7d65c-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7d65c-118">Return code</span></span>                                                                                   | <span data-ttu-id="7d65c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d65c-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="7d65c-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d65c-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7d65c-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7d65c-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="7d65c-122"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="7d65c-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="7d65c-123">Keine Zuweisung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d65c-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d65c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d65c-124">Remarks</span></span>

<span data-ttu-id="7d65c-125">Diese Methode ruft die **imemzuzucator:: GetBuffer** -Methode für die Zuweisung auf und übergibt die Parameter an diese Methode.</span><span class="sxs-lookup"><span data-stu-id="7d65c-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d65c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d65c-126">Requirements</span></span>



| <span data-ttu-id="7d65c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d65c-127">Requirement</span></span> | <span data-ttu-id="7d65c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7d65c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d65c-129">Header</span><span class="sxs-lookup"><span data-stu-id="7d65c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7d65c-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d65c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7d65c-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d65c-131">Library</span></span><br/> | <dl> <span data-ttu-id="7d65c-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7d65c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d65c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d65c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d65c-134">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7d65c-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




