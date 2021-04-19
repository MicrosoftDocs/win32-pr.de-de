---
description: Die Receive-Methode übergibt ein Medien Beispiel an die Eingabe-PIN.
ms.assetid: a8ee0988-8955-48d0-be1b-24eea72d560d
title: Coutputqueue. Receive-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ce8a0d44730fa35b38cf6d738edd26168284a46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373601"
---
# <a name="coutputqueuereceive-method"></a><span data-ttu-id="02451-103">Coutputqueue. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="02451-103">COutputQueue.Receive method</span></span>

<span data-ttu-id="02451-104">Die- `Receive` Methode übergibt ein Medien Beispiel an die Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="02451-104">The `Receive` method delivers a media sample to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="02451-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02451-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="02451-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02451-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="02451-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="02451-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="02451-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02451-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02451-109">Return value</span></span>

<span data-ttu-id="02451-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="02451-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="02451-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="02451-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="02451-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="02451-112">Return code</span></span>                                                                             | <span data-ttu-id="02451-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02451-113">Description</span></span>                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02451-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="02451-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="02451-115">End-of-Stream-Benachrichtigung empfangen, bevor dieses Beispiel verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="02451-115">End-of-stream notification received before processing this sample.</span></span><br/> |
| <dl> <span data-ttu-id="02451-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02451-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="02451-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="02451-117">Success.</span></span><br/>                                                           |



 

## <a name="remarks"></a><span data-ttu-id="02451-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02451-118">Remarks</span></span>

<span data-ttu-id="02451-119">Diese Methode ruft die [**coutputqueue:: receivemultiple**](coutputqueue-receivemultiple.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="02451-119">This method calls the [**COutputQueue::ReceiveMultiple**](coutputqueue-receivemultiple.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02451-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02451-120">Requirements</span></span>



| <span data-ttu-id="02451-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02451-121">Requirement</span></span> | <span data-ttu-id="02451-122">Wert</span><span class="sxs-lookup"><span data-stu-id="02451-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02451-123">Header</span><span class="sxs-lookup"><span data-stu-id="02451-123">Header</span></span><br/>  | <dl> <span data-ttu-id="02451-124"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02451-124"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02451-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="02451-125">Library</span></span><br/> | <dl> <span data-ttu-id="02451-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="02451-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02451-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02451-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02451-128">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="02451-128">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




