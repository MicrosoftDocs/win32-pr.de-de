---
description: Die TimerCallback-Methode ist eine Rückruf Methode für das End-of-Stream-Timer-Ereignis.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Cbaserderderer. TimerCallback-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359805"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="fcb0e-103">Cbaserderderer. TimerCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="fcb0e-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="fcb0e-104">Die- `TimerCallback` Methode ist eine Rückruf Methode für das End-of-Stream-Timer-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fcb0e-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb0e-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="fcb0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb0e-106">Parameters</span></span>

<span data-ttu-id="fcb0e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fcb0e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fcb0e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcb0e-108">Return value</span></span>

<span data-ttu-id="fcb0e-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fcb0e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb0e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcb0e-110">Remarks</span></span>

<span data-ttu-id="fcb0e-111">Die [**cbaserderderer:: sendendofstream**](cbaserenderer-sendendofstream.md) -Methode verwendet ein Timer-Ereignis, um EC-Complete-Benachrichtigungen zu planen \_ .</span><span class="sxs-lookup"><span data-stu-id="fcb0e-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="fcb0e-112">Die **cbaserenderer:: TimerCallback** -Methode ist die Rückruffunktion für das Timer-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fcb0e-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="fcb0e-113">`TimerCallback`Von der-Methode wird " **sendendofstream** " erneut aufgerufen, und " **sendendofstream** " bestimmt, ob die ausführliche EC- \_ Benachrichtigung gesendet oder ein anderer Timer festgelegt</span><span class="sxs-lookup"><span data-stu-id="fcb0e-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="fcb0e-114">Die [**cbaserrederer:: rectendof Stream Timer**](cbaserenderer-resetendofstreamtimer.md) -Methode bricht das Timer-Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="fcb0e-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb0e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcb0e-115">Requirements</span></span>



| <span data-ttu-id="fcb0e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcb0e-116">Requirement</span></span> | <span data-ttu-id="fcb0e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fcb0e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb0e-118">Header</span><span class="sxs-lookup"><span data-stu-id="fcb0e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fcb0e-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb0e-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fcb0e-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fcb0e-120">Library</span></span><br/> | <dl> <span data-ttu-id="fcb0e-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb0e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb0e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcb0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb0e-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fcb0e-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




