---
description: Die sendnotifywindow-Methode benachrichtigt den upstreamfilter über das Videofenster handle.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Cbaserenderer. sendnotifywindow-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369625"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="c6052-103">Cbaserenderer. sendnotifywindow-Methode</span><span class="sxs-lookup"><span data-stu-id="c6052-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="c6052-104">Die- `SendNotifyWindow` Methode benachrichtigt den upstreamfilter über das Videofenster handle.</span><span class="sxs-lookup"><span data-stu-id="c6052-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6052-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6052-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="c6052-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6052-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6052-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="c6052-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c6052-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabepin des Upstream-Filters.</span><span class="sxs-lookup"><span data-stu-id="c6052-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="c6052-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="c6052-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c6052-110">Handle für das Videofenster oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c6052-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6052-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6052-111">Return value</span></span>

<span data-ttu-id="c6052-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c6052-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6052-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6052-113">Remarks</span></span>

<span data-ttu-id="c6052-114">Wenn die Ausgabe-PIN des Upstream-Filters die [**imediaeventsink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) -Schnittstelle unterstützt, sendet diese Methode den Ereignis Code des [**EC- \_ Benachrichtigungs \_ Fensters**](ec-notify-window.md) zusammen mit dem Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="c6052-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="c6052-115">Videorenderer können Ihre [**cbaserdenderer:: completeconnect**](cbaserenderer-completeconnect.md) -Methoden überschreiben, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6052-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="c6052-116">Es stellt einen Mechanismus bereit, mit dem der upstreamfilter des Fenster Handles informiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6052-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="c6052-117">Wenn Sie dies tun, überschreiben Sie auch die [**cbaserdenderer:: breakconnect**](cbaserenderer-breakconnect.md) -Methode, und wenden Sie `SendNotifyWindow` mit einem **null** -Handle an.</span><span class="sxs-lookup"><span data-stu-id="c6052-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6052-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6052-118">Requirements</span></span>



| <span data-ttu-id="c6052-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6052-119">Requirement</span></span> | <span data-ttu-id="c6052-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c6052-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6052-121">Header</span><span class="sxs-lookup"><span data-stu-id="c6052-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c6052-122"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6052-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6052-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c6052-123">Library</span></span><br/> | <dl> <span data-ttu-id="c6052-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c6052-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6052-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6052-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6052-126">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c6052-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




