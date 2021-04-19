---
description: Die receivemultiple-Methode übermittelt einen Batch mit Medien Beispielen an die Eingabe-PIN.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Coutputqueue. receivemultiple-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360286"
---
# <a name="coutputqueuereceivemultiple-method"></a><span data-ttu-id="ff290-103">Coutputqueue. receivemultiple-Methode</span><span class="sxs-lookup"><span data-stu-id="ff290-103">COutputQueue.ReceiveMultiple method</span></span>

<span data-ttu-id="ff290-104">Die- `ReceiveMultiple` Methode übermittelt einen Batch von Medien Beispielen an die Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="ff290-104">The `ReceiveMultiple` method delivers a batch of media samples to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff290-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff290-105">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="ff290-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff290-107">*ppsamples*</span><span class="sxs-lookup"><span data-stu-id="ff290-107">*ppSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="ff290-108">Adresse eines Zeigers auf ein Array von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="ff290-108">Address of a pointer to an array of samples.</span></span>

</dd> <dt>

<span data-ttu-id="ff290-109">*nsamples*</span><span class="sxs-lookup"><span data-stu-id="ff290-109">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="ff290-110">Anzahl der Stichproben im Array.</span><span class="sxs-lookup"><span data-stu-id="ff290-110">Number of samples in the array.</span></span>

</dd> <dt>

<span data-ttu-id="ff290-111">*nsamplesprocgelassene*</span><span class="sxs-lookup"><span data-stu-id="ff290-111">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="ff290-112">Ein Zeiger auf eine Variable, die die Anzahl der erfolgreich übermittelten Stichproben empfängt.</span><span class="sxs-lookup"><span data-stu-id="ff290-112">Pointer to a variable that receives the number of samples delivered successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff290-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff290-113">Return value</span></span>

<span data-ttu-id="ff290-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff290-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ff290-115">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff290-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ff290-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ff290-116">Return code</span></span>                                                                             | <span data-ttu-id="ff290-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff290-117">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff290-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ff290-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ff290-119">End-of-Stream-Benachrichtigung empfangen, bevor dieses Beispiel verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ff290-119">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="ff290-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff290-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ff290-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ff290-121">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="ff290-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff290-122">Remarks</span></span>

<span data-ttu-id="ff290-123">Wenn das Objekt einen Thread verwendet, fügt diese Methode alle im Array bestandenen Beispiele in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="ff290-123">If the object is using a thread, this method queues all of the samples passed in the array.</span></span> <span data-ttu-id="ff290-124">Andernfalls ruft die-Methode die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="ff290-124">Otherwise, the method calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff290-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff290-125">Requirements</span></span>



| <span data-ttu-id="ff290-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff290-126">Requirement</span></span> | <span data-ttu-id="ff290-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ff290-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff290-128">Header</span><span class="sxs-lookup"><span data-stu-id="ff290-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ff290-129"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff290-129"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff290-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff290-130">Library</span></span><br/> | <dl> <span data-ttu-id="ff290-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff290-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff290-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff290-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff290-133">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff290-133">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




