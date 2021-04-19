---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode implementiert die IMemInputPin:: Receive-Methode.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Ctransforminputpin. Receive-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367192"
---
# <a name="ctransforminputpinreceive-method"></a><span data-ttu-id="6835a-104">Ctransforminputpin. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="6835a-104">CTransformInputPin.Receive method</span></span>

<span data-ttu-id="6835a-105">Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="6835a-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="6835a-106">Diese Methode implementiert die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6835a-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6835a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6835a-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="6835a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6835a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6835a-109">*psample*</span><span class="sxs-lookup"><span data-stu-id="6835a-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="6835a-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6835a-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6835a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6835a-111">Return value</span></span>

<span data-ttu-id="6835a-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6835a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6835a-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6835a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6835a-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6835a-114">Return code</span></span>                                                                             | <span data-ttu-id="6835a-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6835a-115">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="6835a-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6835a-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6835a-117">PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="6835a-117">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="6835a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6835a-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6835a-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6835a-119">Success.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="6835a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6835a-120">Remarks</span></span>

<span data-ttu-id="6835a-121">Diese Methode ruft die [**cbaseinputpin:: Receive**](cbaseinputpin-receive.md) -Methode der PIN auf, die den streamingzustand der PIN überprüft und auf Formatänderungen im Medientyp prüft.</span><span class="sxs-lookup"><span data-stu-id="6835a-121">This method calls the pin's [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, which checks the pin's streaming state and checks for format changes in the media type.</span></span> <span data-ttu-id="6835a-122">Anschließend wird die [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode des Filters aufgerufen, die das Beispiel verarbeitet und es nach unten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6835a-122">Then it calls the filter's [**CTransformFilter::Receive**](ctransformfilter-receive.md) method, which processes the sample and delivers it downstream.</span></span>

<span data-ttu-id="6835a-123">Wenn der Filter auf das Beispiel zugreifen muss, nachdem diese Methode zurückgegeben wurde, sollte Sie einen Verweis Zähler enthalten, indem die **IUnknown:: adressf** -Methode für das Beispiel aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6835a-123">If the filter needs to access the sample after this method returns, it should hold a reference count by calling the **IUnknown::AddRef** method on the sample.</span></span> <span data-ttu-id="6835a-124">Beispielsweise benötigen einige Decoder-Filter das aktuelle Beispiel, um das nächste Beispiel zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="6835a-124">For example, some decoder filters need the current sample in order to decode the next sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="6835a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6835a-125">Requirements</span></span>



| <span data-ttu-id="6835a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6835a-126">Requirement</span></span> | <span data-ttu-id="6835a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6835a-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6835a-128">Header</span><span class="sxs-lookup"><span data-stu-id="6835a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6835a-129"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6835a-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6835a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6835a-130">Library</span></span><br/> | <dl> <span data-ttu-id="6835a-131">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6835a-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




