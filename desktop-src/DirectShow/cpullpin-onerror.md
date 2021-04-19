---
description: Die OnError-Methode wird aufgerufen, wenn beim Streaming ein Fehler auftritt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Cpullpin. OnError-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371681"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="c178a-104">Cpullpin. OnError-Methode</span><span class="sxs-lookup"><span data-stu-id="c178a-104">CPullPin.OnError method</span></span>

<span data-ttu-id="c178a-105">Die- `OnError` Methode wird aufgerufen, wenn beim Streaming ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c178a-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="c178a-106">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c178a-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c178a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c178a-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c178a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c178a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c178a-109">*Std.*</span><span class="sxs-lookup"><span data-stu-id="c178a-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="c178a-110">Gibt den **HRESULT** -Wert an, der von der fehlerhaften Methode zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c178a-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c178a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c178a-111">Return value</span></span>

<span data-ttu-id="c178a-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c178a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c178a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c178a-113">Remarks</span></span>

<span data-ttu-id="c178a-114">Das-Objekt ruft diese Methode immer dann auf, wenn ein Fehler auftritt, der den datenzieh Thread stoppt.</span><span class="sxs-lookup"><span data-stu-id="c178a-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="c178a-115">Der Filter kann diese Methode verwenden, um Streamingfehler ordnungsgemäß wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c178a-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="c178a-116">In den meisten Fällen wird der Fehler vom upstreamfilter zurückgegeben, sodass der upstreamfilter dafür zuständig ist, ihn an den Filter Graph-Manager zu melden.</span><span class="sxs-lookup"><span data-stu-id="c178a-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="c178a-117">Wenn der Fehler innerhalb der [**cpullpin:: Receive**](cpullpin-receive.md) -Methode auftritt, sollte der Filter ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis senden.</span><span class="sxs-lookup"><span data-stu-id="c178a-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="c178a-118">(Weitere Informationen finden Sie unter [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span><span class="sxs-lookup"><span data-stu-id="c178a-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="c178a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c178a-119">Requirements</span></span>



| <span data-ttu-id="c178a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c178a-120">Requirement</span></span> | <span data-ttu-id="c178a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c178a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c178a-122">Header</span><span class="sxs-lookup"><span data-stu-id="c178a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c178a-123"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="c178a-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c178a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c178a-124">Library</span></span><br/> | <dl> <span data-ttu-id="c178a-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c178a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c178a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c178a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c178a-127">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c178a-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




