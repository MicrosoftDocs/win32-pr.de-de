---
description: Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und übergibt sie an den downstreamfilter.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Ctransinplacefilter. Receive-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e7a1f87617b59c31139cb3d857c83d4470fd709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366822"
---
# <a name="ctransinplacefilterreceive-method"></a><span data-ttu-id="419a9-103">Ctransinplacefilter. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="419a9-103">CTransInPlaceFilter.Receive method</span></span>

<span data-ttu-id="419a9-104">Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und übergibt sie an den downstreamfilter.</span><span class="sxs-lookup"><span data-stu-id="419a9-104">The `Receive` method receives a media sample, processes it, and delivers it to the downstream filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="419a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="419a9-105">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="419a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="419a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="419a9-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="419a9-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="419a9-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle im Beispiel.</span><span class="sxs-lookup"><span data-stu-id="419a9-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="419a9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="419a9-109">Return value</span></span>

<span data-ttu-id="419a9-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="419a9-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="419a9-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="419a9-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="419a9-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="419a9-112">Return code</span></span>                                                                                  | <span data-ttu-id="419a9-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="419a9-113">Description</span></span>                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="419a9-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="419a9-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="419a9-115">Erfolg</span><span class="sxs-lookup"><span data-stu-id="419a9-115">Success</span></span><br/>          |
| <dl> <span data-ttu-id="419a9-116"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="419a9-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="419a9-117">Unerwarteter Fehler</span><span class="sxs-lookup"><span data-stu-id="419a9-117">Unexpected error</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="419a9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="419a9-118">Remarks</span></span>

<span data-ttu-id="419a9-119">Die Eingabe-PIN des Filters ruft diese Methode auf, wenn Sie ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="419a9-119">The filter's input pin calls this method when it receives a sample.</span></span> <span data-ttu-id="419a9-120">Der Filter Ruft die [**Transformations**](ctransinplacefilter-transform.md) Methode auf, die von der abgeleiteten Klasse implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="419a9-120">The filter calls the [**Transform**](ctransinplacefilter-transform.md) method, which the derived class must implement.</span></span> <span data-ttu-id="419a9-121">Die **Transformations** Methode verarbeitet die Daten.</span><span class="sxs-lookup"><span data-stu-id="419a9-121">The **Transform** method processes the data.</span></span> <span data-ttu-id="419a9-122">Wenn der Filter nur einen Zuweiser verwendet, übergibt er *psample* direkt an die **Transformations** Methode.</span><span class="sxs-lookup"><span data-stu-id="419a9-122">If the filter is using only one allocator, it passes *pSample* directly to the **Transform** method.</span></span> <span data-ttu-id="419a9-123">Andernfalls kopiert Sie *psample* und übergibt die Kopie.</span><span class="sxs-lookup"><span data-stu-id="419a9-123">Otherwise, it copies *pSample* and passes the copy.</span></span>

<span data-ttu-id="419a9-124">Wenn die **Transform** -Methode S \_ false zurückgibt, löscht die- `Receive` Methode das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="419a9-124">If the **Transform** method returns S\_FALSE, the `Receive` method drops the sample.</span></span> <span data-ttu-id="419a9-125">Im ersten gelöschten Beispiel sendet der Filter ein [**EC- \_ Qualitäts \_ Änderungs**](ec-quality-change.md) Ereignis an den Filter Graph-Manager.</span><span class="sxs-lookup"><span data-stu-id="419a9-125">On the first dropped sample, the filter sends an [**EC\_QUALITY\_CHANGE**](ec-quality-change.md) event to the filter graph manager.</span></span> <span data-ttu-id="419a9-126">Andernfalls liefert der  \_ Filter das Ausgabe Beispiel, wenn die Transform-Methode "S OK" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="419a9-126">Otherwise, if the **Transform** method returns S\_OK, the filter delivers the output sample.</span></span> <span data-ttu-id="419a9-127">Zu diesem Zweck wird die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die downstreameingabepin aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="419a9-127">To do so, it calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="419a9-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="419a9-128">Requirements</span></span>



| <span data-ttu-id="419a9-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="419a9-129">Requirement</span></span> | <span data-ttu-id="419a9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="419a9-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419a9-131">Header</span><span class="sxs-lookup"><span data-stu-id="419a9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="419a9-132"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="419a9-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="419a9-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="419a9-133">Library</span></span><br/> | <dl> <span data-ttu-id="419a9-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="419a9-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419a9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="419a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419a9-136">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="419a9-136">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




