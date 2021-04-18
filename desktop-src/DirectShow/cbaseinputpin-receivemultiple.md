---
description: 'Die receivemultiple-Methode empfängt ein Array von-Beispielen. Diese Methode implementiert die IMemInputPin:: receivemultiple-Methode.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Cbaseinputpin. receivemultiple-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364535"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="b368f-104">Cbaseinputpin. receivemultiple-Methode</span><span class="sxs-lookup"><span data-stu-id="b368f-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="b368f-105">Die- `ReceiveMultiple` Methode empfängt ein Array von-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="b368f-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="b368f-106">Diese Methode implementiert die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b368f-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b368f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b368f-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="b368f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b368f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b368f-109">*psamples*</span><span class="sxs-lookup"><span data-stu-id="b368f-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="b368f-110">Die Adresse eines Arrays von [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeigern der Größe *nsamples*.</span><span class="sxs-lookup"><span data-stu-id="b368f-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="b368f-111">*nsamples*</span><span class="sxs-lookup"><span data-stu-id="b368f-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="b368f-112">Anzahl der zu verarbeitenden Stichproben.</span><span class="sxs-lookup"><span data-stu-id="b368f-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="b368f-113">*nsamplesprocgelassene*</span><span class="sxs-lookup"><span data-stu-id="b368f-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="b368f-114">Ein Zeiger auf eine Variable, die die Anzahl der verarbeiteten Beispiele empfängt.</span><span class="sxs-lookup"><span data-stu-id="b368f-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b368f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b368f-115">Return value</span></span>

<span data-ttu-id="b368f-116">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b368f-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b368f-117">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="b368f-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b368f-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b368f-118">Return code</span></span>                                                                                             | <span data-ttu-id="b368f-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b368f-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="b368f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="b368f-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b368f-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b368f-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="b368f-123">PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="b368f-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="b368f-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="b368f-125">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="b368f-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="b368f-126"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="b368f-127">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b368f-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="b368f-128"><dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="b368f-129">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="b368f-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="b368f-130"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="b368f-131">Die PIN wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="b368f-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="b368f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b368f-132">Remarks</span></span>

<span data-ttu-id="b368f-133">Diese Methode verhält sich wie die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode, empfängt jedoch ein Array von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="b368f-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="b368f-134">In der Basisklasse durchläuft die-Methode das Array und ruft mit jedem Beispiel **Receive** auf.</span><span class="sxs-lookup"><span data-stu-id="b368f-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="b368f-135">Überschreiben Sie diese Funktion, wenn der Filter Batches von Beispielen effizienter verarbeiten kann, als Sie nacheinander verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b368f-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="b368f-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b368f-136">Requirements</span></span>



| <span data-ttu-id="b368f-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b368f-137">Requirement</span></span> | <span data-ttu-id="b368f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b368f-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b368f-139">Header</span><span class="sxs-lookup"><span data-stu-id="b368f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b368f-140"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b368f-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b368f-141">Library</span></span><br/> | <dl> <span data-ttu-id="b368f-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b368f-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b368f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b368f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b368f-144">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b368f-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




