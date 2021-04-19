---
description: Die resetmediatime-Methode setzt die zwischengespeicherten Zeitstempel auf NULL zurück.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Crendererpospassthru. resetmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354131"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="b4adf-103">Crendererpospassthru. resetmediatime-Methode</span><span class="sxs-lookup"><span data-stu-id="b4adf-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="b4adf-104">Die- `ResetMediaTime` Methode setzt die zwischengespeicherten Zeitstempel auf NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="b4adf-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4adf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4adf-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="b4adf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4adf-106">Parameters</span></span>

<span data-ttu-id="b4adf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b4adf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4adf-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4adf-108">Return value</span></span>

<span data-ttu-id="b4adf-109">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="b4adf-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4adf-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4adf-110">Remarks</span></span>

<span data-ttu-id="b4adf-111">Der Filter sollte diese Methode immer dann aufrufen, wenn die Zeitstempel, die von der [**crendererpospassthru:: registermediatime**](crendererpospassthru-registermediatime.md) -Methode zwischengespeichert werden, ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="b4adf-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="b4adf-112">Insbesondere sollte diese Methode als Antwort auf die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode und die [**imediafilter::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) End-Methode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b4adf-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="b4adf-113">Nachdem diese Methode aufgerufen wurde, gibt die [**crendererpospassthru:: getmediatime**](crendererpospassthru-getmediatime.md) -Methode für die Start-und Endzeit 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b4adf-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4adf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4adf-114">Requirements</span></span>



| <span data-ttu-id="b4adf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4adf-115">Requirement</span></span> | <span data-ttu-id="b4adf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b4adf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4adf-117">Header</span><span class="sxs-lookup"><span data-stu-id="b4adf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b4adf-118"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4adf-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4adf-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4adf-119">Library</span></span><br/> | <dl> <span data-ttu-id="b4adf-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b4adf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




